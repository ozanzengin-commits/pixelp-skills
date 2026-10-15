---
name: storefront-screenshots
description: Designs App Store and Google Play screenshot sets ("storefronts") directly in Figma — composition patterns, store policy limits, and the Figma Plugin API failure modes that waste the most time. Use this skill whenever the prompt contains "Run Screenshots Skills", and also whenever someone asks for storefront screenshots, App Store screenshots, Play Store screenshots, store visuals, an ASO creative set, a screenshot set for an app, localised screenshot variants, or asks to lay out marketing screens for a mobile app — even if they never say "skill", "Figma" or "screenshot" explicitly. Prefer this skill over improvising, because it encodes failure modes that are otherwise repeated on every job.
---

# Storefront screenshots

This skill exists because designing a store set in Figma involves three kinds of knowledge that are easy to lose: what the two stores prohibit, how strong sets are actually composed, and the specific ways the Figma Plugin API bites you. The third costs the most time. Read the production rules before writing anything.

## Before writing anything

0. Read `references/store-policies.md`. It lists what the two stores prohibit outright, and several of those prohibitions are things designers add by habit — ranking badges, the word "free", store badges, invented star ratings. Catching them before drawing costs nothing; catching them at submission costs a resubmission.
1. Load the Figma usage guide for the file you are working in. Do not start writing nodes from memory.
2. Confirm the target: which Figma page, which app, which format, how many screens. If any of these is missing, ask rather than guess — a set built at the wrong frame size is a total rewrite.
3. Establish the visual direction. If the brief gives colours, typefaces and a voice, use them. If it does not, ask, or say plainly in the delivery summary that you chose them. Never present an invented palette as if it came from the brand.
4. Read `references/composition.md`. It is a pattern library, not a checklist. Precedence runs brief first, then patterns. If the brief includes a reference image, read the reference first and pick the patterns that match what it is already doing — the reference says which family the set belongs to, the library says how that family is built properly. With no reference, choose from the app's category and register using the selection section at the top of that file. Pick two or three techniques and hold them across the set.
5. Inspect the file first. Read the existing variable collections, published components and available fonts. If the file already has tokens, use them instead of creating new ones.

## Frame conventions

- Frame sizes: 6.5" is 1242×2688, 6.9" is 1320×2868, iPad 13" is 2048×2732, 9:16 is 1080×1920, 16:9 is 1920×1080. Apple's required sizes change; if the request looks like a real delivery, remind the person to verify in App Store Connect.
- **Two defaults that hold unless the brief says otherwise: 50 px between frames, and a 75 px corner radius on the frames themselves.** Both are house values. If the brief specifies a different gap or corner, follow the brief; if it says nothing about either, use these and do not ask.
- Name frames `01 Hero`, `02 ...`, `03 ...` and lay them left to right with 50 px between them. A tight gutter lets you judge the set the way the store shows it, as a strip; wide gaps make screens look better in isolation than they will side by side.
- The first screen is the cover. Later screens are SS2, SS3 and so on. When the brief lists elements per screen, put each element only on the screen it was assigned to.
- Leave 140 px of clear space top and bottom when the brief asks for a safe area, so headlines are not swallowed by store chrome.

## Production rules

These are the actual failure modes, in the order they usually bite.

**Text layers.** Set the width before assigning characters. A text node created without a width collapses and lays one character per line. After any `resize()` on a text node, set `textAutoResize` back to `'HEIGHT'` — `resize()` silently switches it off, and the layer then reports a stale height while its content overflows. Do not rely on `layoutSizingHorizontal = 'FILL'` for text inside auto-layout; it frequently resolves to zero width. Use `'FIXED'` plus an explicit `resize()` to the parent's inner width.

**Resizing a set: the subject keeps its scale, the image does not.** Carrying a set to another frame size fails in a specific, quiet way — the original artwork is dropped into the new frame, Figma fits it, and the subject ends up filling a smaller share of the frame than it did in the source. The person shrinks, background opens up around them, and the screen reads as weaker than the original with nothing obviously broken. Measure anchors in the source as fractions of the frame (subject width ÷ frame width; eye line or chin ÷ frame height; the top edge of whatever sits over the artwork ÷ frame height) and match them on the result within a couple of percent. Scale the artwork to COVER and crop, never to FIT: a proportionally shorter frame means cropping more off the top and bottom, not scaling the picture down. Crop around the subject rather than the image's centre. When cropping runs out of image, re-crop from the layers if it is still layered, then extend the scene, then regenerate from the original prompt — in that order, decided per image.

**Grid auto-layout manages itself, and fights you if you forget that.** On a frame with `layoutMode = 'GRID'`, several properties are computed rather than settable. `gridRowCount` throws while `gridAutoTracks` is `'ROWS'` — set `gridAutoTracks = 'NONE'` first, or change the count by adding and removing children. `setGridChildPosition(row, column)` throws while `gridItemsPositioning` is `'ROW_AUTO_FLOW'`, because Figma is placing the children — reorder with `parent.insertChild(index, child)` instead; `appendChild` drops a node into the first free cell. `gridRowCount` also cannot go below 1 or shrink past a row that still holds a child. And do not assign to `gridRowSizes` / `gridColumnSizes`: that is *no setter for property*, because you are meant to use the setters on the `GridTrackSize` objects those arrays return. Check `layoutMode` before writing any of this.

**A lookup that found nothing returns null.** `getNodeByIdAsync`, `findOne` and friends return `null` rather than throwing, so the error surfaces one line later as *cannot read property 'id' of null*. Check every lookup and stop with the name of what you were looking for — this error is usually the second wave of an earlier call that failed quietly.

**Absolutely positioned children cannot fill.** Setting `layoutPositioning = 'ABSOLUTE'` takes a layer out of the auto-layout flow, so `layoutSizingHorizontal`/`layoutSizingVertical` can only be `'FIXED'` on it — asking for `'FILL'` throws *FILL cannot be set on absolute positioned auto-layout children*. Give it a fixed size with `resize()`, or leave it in the flow. The usual cause is pinning a badge or a glow over a card and then trying to stretch it to the card's height.

**Reading other pages.** With `documentAccess: "dynamic-page"` only the open page is loaded, and touching any other page's `.children` — including merely walking `figma.root.children` to look around — throws *Cannot access property `children` on a page that has not been explicitly loaded*. Call `await figma.loadAllPagesAsync()` once before you scan, or `await page.loadAsync()` for the single page you need. Everything on `figma.currentPage` is already available.

**Fixed-size boxes inside auto-layout.** Setting `layoutMode` after `resize()` makes a frame hug its contents, so a 104×104 icon holder becomes a 40 px sliver. Set `layoutSizingHorizontal` and `layoutSizingVertical` to `'FIXED'`, then resize.

**Font style names differ per family.** Montserrat uses `ExtraBold` and `SemiBold` with no space; Inter uses `Extra Bold` and `Semi Bold`. Never guess — read the available styles first and load every style you intend to use.

**Rotation.** Rotation pivots around the node's origin, so a rotated card lands away from where the numbers say. Set the rotation, then set x and y, then screenshot and correct.

**Selectors.** Layer-name queries choke on spaces. Use `findAllWithCriteria` and filter in code rather than building a selector string.

**Gradients.** Every gradient stop needs an alpha channel. A stop without one throws and takes the whole script with it.

**Scripts are atomic.** One syntax error rolls back everything the script would have done. Keep each script to a handful of operations so a failure costs one step, not a whole screen.

**App screens are drawn at 1x; storefronts are not.** A product file's screens are usually 375 px wide, and a storefront places them two to three times larger. Everything the designer tuned for 1x gets magnified with them: hairline strokes, low-opacity outlines, tiny icons. The status bar is the usual casualty — an iOS battery is drawn with a 35% outline and a solid fill, which reads correctly at 375 px and as a black blob at 1000 px. After scaling any app screen, look at the status bar and any hairline detail, and repaint what broke. Google Play separately requires the battery, wifi and signal indicators to read full, so setting them solid fixes both problems at once. Hiding the status bar entirely is also acceptable.

**Space the interface, the text block and the icon row evenly.** Once you know where the filler goes, the three gaps around it should be equal: edge to text, text to icons, icons to the interface (or to the far edge). Do this arithmetically, not by eye. Keep the interface where it is, because its top line is shared across the set; take the free region it leaves, subtract the height of the text block and the height of the icon row, and divide the remainder by three. Treat the text block as one object — headline lines and subline keep their internal spacing and move together. Uneven gaps are the difference between a screen that looks composed and one that looks assembled.

**Measure the empty bands on every screen and fill the largest one.** Screens end up with bare ground wherever the copy is short, and it is easy to fix three screens and miss the fourth. For each screen, list every empty band — above the first element, between elements, and below the last one — and take the tallest. The filler does not belong between the headline and the interface by default; it belongs wherever the space actually is. On a screen where the interface bleeds off the top and the copy sits high, the biggest band is usually at the bottom of the frame, and squeezing the row into a narrow slot higher up while leaving that space open is the common mistake. Any band past roughly a fifth of the frame height needs filling, and the filler is glyph tiles carrying meaning from that screen's headline — not a decorative shape, and not a plain colour bar. A bar is filler; a glyph names a capability. Do this before the final screenshot pass, and name the screens you checked in the delivery summary.

**Verify visually.** Screenshot every frame after building it and fix overflow, misalignment and overlap before moving on. Numbers that look right in code are regularly wrong on the canvas. This single habit catches most defects.

## Layout quality

`references/composition.md` carries the compositional patterns: where the headline sits, how weight contrast works inside it, the three ways interface is placed, background strategy, floating elements, and how the cover differs from the rest. Read it before laying anything out.

The mechanical rules that are easy to get wrong regardless of style:

- **The cover headline is a masthead and must be visibly larger than any other headline in the set.** Not a little larger — large enough that the hierarchy is obvious at thumbnail size. Size it as big as will hold on two lines within the margins, then set the rest of the set well below it.
- **Feature headlines do not go below 120 px on a 1242 px wide frame** (scale that floor with the frame width). Below that they stop reading in the gallery, which is where the decision is actually made.
- **Sublines do not go below 65 px on the same frame.** A subline that is legible in Figma at 100% is often unreadable in the store strip. If the copy will not fit at 65 px, shorten the copy rather than shrinking the type.
- Give headings a real line height. A line height at or below the font size lets glyphs escape their box, and anything clipping that box cuts the text.
- When a headline may run to one or two lines across a set, reserve the taller height on every screen so the artwork below starts at the same place, and centre a single-line headline inside that reserved space.
- Do not clone a screen to make the next one. Vary the silhouette, the composition and the colour temperature between consecutive screens, or the set reads as one screen repeated.
- Prefer auto-layout for anything that will be edited later, and lock the boxes that must keep their size.
- **Where the device meets the frame edge there are exactly two correct answers, and a third that is always wrong.** Either the whole device sits inside the frame with all four corners complete and THREE equal margins — left, right and bottom, with a deliberately larger top margin for the headline (contained; four equal margins is wrong, it leaves no room for copy) — or it runs off the bottom edge with the cut landing on the straight part of the bezel, above where the corner arc begins (bled). What is never allowed is overhanging the edge by less than the device's own corner radius, so the corner curve starts and is then chopped by the frame boundary — the device then looks like it is melting out of the picture. The arithmetic: with corner radius `R` and overhang `D`, `D <= 0` or `D >= R` are correct, `0 < D < R` is wrong. Aim for `D >= R * 1.25`. Verify by exporting each frame and looking at its bottom edge: you should see either no device or two straight vertical lines, never a curve. Zebra sets are exempt, since alternating overflow is the point of that style. Full rules in `references/composition.md`.
- **Fill the gap between the headline and the interface.** Aligning the device tops leaves a band of empty ground on the screens with shorter headlines. Put a small run of icon tiles or floating elements in it rather than leaving a hole. See the gap rule in `references/composition.md`.
- **Devices stay upright and their tops align across the set.** No tilted screens. Scale may vary between screens; the top edge of the interface and its horizontal centring may not.
- **Never drop artwork in as a bare rectangle.** Photography and illustration bleed off at least one edge, sit under a purpose-built gradient, and share a colour with the palette. See the integration rules in `references/composition.md`.
- **Every cover shows the app name.** House rule: the name appears on the cover as a wordmark, normally at the top, set in the set's own type and colour rather than dropped in as a logo file. It is a small element, well below the headline in size — it identifies the app, it does not compete with the message. If the brief names the app, use that name exactly.
- **Every cover carries a "#1 App" badge.** House rule: a laurel-flanked #1 mark on the cover of every set, styled to that set's palette and type. Two things travel with it. The claim has to be substantiable — hold a current, documented ranking before it ships, and change the wording if the honest claim is narrower, such as a specific category or country. And it comes off any set going to Google Play, which prohibits ranking and award motifs in screenshots outright.
- **Every set needs a cover, and the cover is a different kind of screen.** Not the same template with different words. See the cover rule in `references/composition.md`; it is the most commonly skipped step and the most expensive one to skip, because the cover is the only screen most people ever see.

## Assets

- Name every layer that will receive artwork `ASSET SLOT / <what goes here>` and give it the real aspect ratio of the intended image, so the file can be dropped in without cropping.
- Do not attempt to draw illustrations, 3D characters or photographic scenes with vector primitives. Build the slot, name it, and say what belongs there.
- Uploads are capped around 10 MB. Trim transparent padding and downscale before uploading; a cutout PNG usually has a large empty border that wastes the budget.
- For a cutout figure, measure its real aspect ratio and lock the slot to it. A character placed in a slot of the wrong ratio gets squashed and nobody notices until review.

## Copy

- Headlines are short, in the second person, and lead with a verb where the app's voice allows it. Three to five words is the working range.
- Keep the case consistent across a set. If the brief specifies upper case, title case or lower case, apply it to every headline.
- For a multi-language set, keep the layout identical and adjust only line breaks. German and Turkish run long; Japanese and Korean run short. Check that no headline reflows into the artwork.
- Right-to-left sets mirror alignment and icon direction.

## Compliance

`references/store-policies.md` is the authority. The short version, because these are the ones that come up constantly:

- No ranking or award claims. "#1", "App of the year", laurel wreaths, award icons. Google Play bans these in screenshots outright.
- No price or promotional wording, which includes the word "free". "Start free" is a price claim, not a CTA. Use "Get started".
- No install call-to-action overlays, no store badges of any kind.
- Ratings, review counts and user numbers only when the brief supplies them with evidence. Never invent or round them up.
- Screenshots must show the real interface. Both stores reject sets that are marketing artwork with no app in them, and Play wants interface prioritised in the first three screens.
- Everything must suit a general audience, whatever the app's age rating.
- Apple portrait phone sizes break Play's two-to-one aspect limit, so the same file cannot serve both stores. Build Play portrait at 1080×1920.

If the brief asks for something on this list, do not quietly comply and do not quietly refuse. Say which rule it hits, offer the compliant alternative, and let the person decide.

### Category-specific care

Named by category, not by product, because the risk follows the subject matter.

- **Scripture, poetry, lyrics, literary text.** Quote exactly and name the edition or translation. Never paraphrase or invent. Confirm the licence: many modern translations are under copyright even when the underlying work is not.
- **Health, fitness, nutrition, sleep, medication tracking.** No medical claims, no promised outcomes, no dosing guidance. Describe what the app does, not what the user's body will do. Google Play names misleading health functionality as deceptive behaviour.
- **Finance, trading, investing.** Nothing that implies returns. Keep the copy on simulation, tracking or education. Real tickers, company names and logos are third-party marks; confirm the data licence covers them or use generic instruments in the artwork.
- **Generative AI output.** Do not show output the app cannot actually produce, and do not present a generated result as a real photograph of a real person.
- **Anything aimed at, or attractive to, children.** Both stores hold the listing to a general-audience standard regardless of the app's rating, and Play will ask you to declare child age groups if the artwork appeals to children.

**A promise the interface cannot show is a defect, not a headline.** If the brief's lead claim has no corresponding screen — a set promising AI with no AI anywhere in the UI, for example — raise it. Both stores require screenshots to reflect the app's real experience, and the claim is also the weakest part of the set commercially.

## Delivery

Finish with a short summary. Confirm explicitly that every screen was checked for the gap between the headline and the interface, and say what fills it on each; if a screen needed nothing, say why. Then: which frames were created, which `ASSET SLOT` layers need filling, and anything you had to assume. If you assumed a value that the brief did not specify, say which one — silent assumptions are what get discovered at review.
