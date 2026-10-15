# Composition patterns

A library of patterns observed across a large sample of high-performing App Store and Play sets. It is a menu, not a checklist. A set that used everything here would be a mess.

## Contents

- [How to choose](#how-to-choose)
- [Headline placement](#headline-placement)
- [Headline scale](#headline-scale)
- [Headline structure](#headline-structure)
- [Emphasis techniques](#emphasis-techniques)
- [Layout alternatives](#layout-alternatives)
- [Scaling app screens](#scaling-app-screens)
- [Device handling](#device-handling)
- [Integrating photography and illustration](#integrating-photography-and-illustration)
- [Filling the gap between headline and interface](#filling-the-gap-between-headline-and-interface)
- [Bento sets](#bento-sets)
- [Fun sets: abstract shape backgrounds](#fun-sets-abstract-shape-backgrounds)
- [Minimalist sets](#minimalist-sets)
- [Overflow](#overflow)
- [Overlay layers](#overlay-layers)
- [Background and colour strategy](#background-and-colour-strategy)
- [Laying the set out](#laying-the-set-out)
- [The cover](#the-cover)
- [Variant sets](#variant-sets)
- [Credibility marks](#credibility-marks)
- [Social proof](#social-proof)
- [Third-party marks and numeric claims](#third-party-marks-and-numeric-claims)

## How to choose

Precedence runs: the brief first, then these patterns. Patterns fill silence; they never override a stated instruction.

When a reference image comes with the brief, read the reference first and pick the patterns that match what it is already doing. The reference tells you which family the set belongs to; this file tells you how that family is built properly. Do not import a pattern the reference clearly avoids.

When there is no reference, choose from the app's category and register:

- **Utility, backup, productivity.** Clean interface-forward layouts, one accent colour, real device frames, weight or colour contrast in the headline. Restraint reads as competence here.
- **Social, dating, chat.** Loud display type, saturated flat colours changing per screen, frameless content floating in space, photographic people.
- **Learning, journalling, reading, premium content.** Serif or mixed serif and sans, centred alignment, editorial page furniture, light grounds, illustration over photography.
- **Fitness, gaming, anime-adjacent.** Dark grounds, neon accent, glow outlines on the device, character art bleeding past frame edges, rank and level UI.
- **Wellness, sleep, calm.** Deep gradient grounds spanning the set, soft type, one warm accent, imagery of place rather than interface.
- **Screen-time, habit, blocker.** Cream or bright pastel ground, heavy geometric sans, mascot, handwritten annotation over the interface.

Pick two or three techniques and hold them across the set. Consistency is what makes a set look designed; variety within a single screen makes it look panicked.

## Headline placement

**Top-aligned is the common default**, sitting near the top edge rather than floating in a wide margin. Editorial heavy-type sets push it nearly flush.

**But placement can alternate across a set on purpose.** Several strong sets put the headline at the top on one screen and at the bottom on the next, so the gallery has rhythm when swiped. If you do this, alternate deliberately in a pattern, not at random.

**A single screen can carry copy at both ends**: headline at the top, a secondary claim pinned to the bottom. This works when the middle is occupied by a device or a single strong image.

**Left-aligned by default.** Centre alignment belongs to two registers: the premium serif set, and a cover whose headline is itself the social proof. If neither applies, left-align.

## Headline scale

**Set the cover headline as a masthead.** It should be clearly the largest type in the set — sized to the widest line that still holds on two lines inside the margins. If the cover headline is the same size as the feature headlines, the set has no front door.

**Hold a floor for the feature headlines.** On a 1242 px wide frame, 120 px is the minimum; scale proportionally for other frame sizes. Anything smaller survives at full size and disappears in the gallery strip, and the gallery strip is where people decide.

**The subline has a floor too: 65 px on a 1242 px wide frame.** A subline set small enough to look elegant on the canvas usually vanishes in the gallery. If it will not fit at 65 px, cut words rather than points — a subline is a qualifier, not a paragraph, and one line that survives beats two that do not.

**Re-flow whatever sits below after any type change.** Raising a subline by ten points can push it from one line to two, which moves everything under it. Position the following element from the measured bottom of the block above, not from a remembered number, and screenshot afterwards.

**Keep the feature headlines at one size.** The cover varies; screens two to N do not. Equal headline size across the feature screens is a large part of what makes a set look like a set.

## Headline structure

**Two or three lines, two to five words per line.** Break on meaning, not on width. A short line that keeps a phrase intact beats a full measure that splits one.

**A one-line subhead under the headline**, lighter weight, sentence case, is common and useful. It carries the qualifier the headline cannot: "No swiping. No scrolling. Just connection."

## Emphasis techniques

Almost every strong set uses at least one. A headline in a single uniform treatment is the most common reason a set feels flat. Pick one technique and repeat it across the set.

1. **Weight contrast.** Split the sentence between two weights: "Log sets" heavy, "with ease." light. Or emphasise one word inside an even line.
2. **Italic contrast.** One word or connector in italic: "Sleep better *with* white noise", "Restore *anything* instantly", "Chronicle *your* Reading".
3. **Colour split.** Two words in two different colours within the same sentence. Effective on black grounds, where a single accent word carries a lot.
4. **Filled block behind a word.** The emphasised word sits in a solid rectangle in the inverse colour. Reads as a stamp; works with condensed heavy sans.
5. **Sticker outline around a word.** The word gets a contrasting outline or halo, as if it were a sticker laid on the artwork. Suits playful, pastel, mascot-led sets.
6. **Handwritten accent.** One word in a script or handwritten face, often in an accent colour, inserted into an otherwise typographic headline.
7. **Icon set inline in the headline.** A small glyph replaces or joins a word: "Restore anything ⏱ instantly". Keeps a long headline scannable.

## Layout alternatives

**Interface placement, four approaches.** Pick one and hold it:

- Frameless card sitting directly on the ground, no device chrome.
- Real device frame, upright.
- Interface bleeding off an edge, cropped by the frame boundary.
- No device at all: the content itself is the composition. Chat bubbles floating in space, a full-bleed photograph, a character card. This is a strong choice for social and dating, where the product is the conversation rather than the screen.

**Align the tops of the devices across the whole set.** Whatever size each screen is, the top edge of the interface sits on the same horizontal line on every screen. When someone swipes the gallery the device should look like it is holding still while the content behind it changes; tops at different heights make the set jitter. Pick one y for the device top, apply it everywhere, and let the headline block above it be the thing that varies.

**Size can vary, position cannot drift.** Pulling one screen closer or pushing another further back is a legitimate way to give a set rhythm, and a smaller device can be centred horizontally with more ground around it. What must not vary is the top line and the horizontal centring. Vary the scale, keep the anchor.

**Do not over-crop.** A device cut off so that only a sliver of interface survives tells the viewer nothing. Show enough of the screen that the feature in the headline is visible and legible at thumbnail size, then let the rest run off the bottom.

### Elements that span two screens

A strong set sometimes runs one element across the boundary between two neighbouring screens — a badge, a ribbon, a shape, a gradient, the edge of a device. Half of it sits at the right edge of screen N, the other half at the left edge of screen N+1, and the pair reads as one continuous picture when the store shows them in a row. It is one of the cheapest ways to make a set look designed rather than assembled.

**Build it against the gap, not flush.** This is the part that is got wrong almost every time. The stores display screenshots with a gap between them. If you align the two halves while the frames are touching on the Figma canvas, the element breaks the moment that gap appears: the halves no longer meet and the seam reads as a mistake.

The correct construction is the opposite. Lay the frames out with the gap already between them — 50 px in the convention this skill uses — draw the crossing element as ONE object across that whole span, and let the gap occlude its middle. Each frame then carries its own half, cropped at its own edge, and the slice of the object that falls into the gap is simply never drawn.

The consequence looks wrong until you understand it: **pushed flush, the element will show a missing slice.** That is correct. The arrangement is built for the spaced view, which is the only view anyone outside Figma ever sees. So verify it that way — export both frames, place them side by side with the gap, and look at the join. Never judge it from the canvas with the frames adjacent.

**These connections are the first thing a resize or a translation destroys, and the loss is silent** — each frame still looks fine on its own, and only the strip shows that the join is gone. Before rebuilding a set at another size or in another language, export the frames, lay them out in order and look at the seams; anything cut off at a frame edge and continuing on the next is one of these, and it has to be carried across and recomputed. The gap does not scale with the frame, so the proportion of the element that disappears into it changes with the frame size: recompute both halves from the new frame width and the gap rather than reusing the source's crop.

### Where the device meets the frame edge

This is the single most common defect in generated sets, and it is immediately visible to anyone looking. There are exactly two correct relationships. Pick one, and use the same one on every screen in the set.

**CONTAINED.** The whole device sits inside the frame, all four corners visible and complete, nothing cropped. **THREE margins are equal: left, right and bottom.** The top margin is the odd one out and it is deliberately larger, because that is where the headline block lives. The device is therefore NOT centred vertically in the frame — it sits low, anchored to the bottom margin, with the type above it.

Four equal margins is a different thing and it is wrong: it centres the device in the frame and leaves no room for a headline. If you find yourself with equal space above and below the device, you have squeezed the copy out of the screen.

The check: `margin_left == margin_right == margin_bottom`, and `margin_top` is comfortably larger than all three. Use the same three-margin value on every screen in the set so the devices sit on one line.

**BLED.** The device runs off the bottom edge of the frame (or the top, on an interface-first screen). The crop lands on the **straight** part of the bezel, above the point where the corner arc begins. At the frame's edge the device outline reads as two parallel vertical lines.

**THE DEFECT.** The device overhangs the frame edge by less than its own corner radius, so the corner arc starts, curves, and is then chopped by the frame boundary. The result is a device that looks like it is melting out of the bottom of the picture. It is wrong every time.

**The measurable test.** Let `R` be the device body's corner radius and `D` the distance the device's bottom edge sits below the frame's bottom edge.

- `D <= 0` → CONTAINED. Correct.
- `D >= R` → BLED, the cut is on the straight bezel. Correct.
- `0 < D < R` → the frame edge is crossing the arc. **Wrong.** Fix it by moving the device up until `D <= 0`, or down until `D >= R`.

In practice give yourself margin: push to `D >= R * 1.25` rather than sitting exactly on `R`, because the arc's visual start is slightly inside its geometric start. At storefront scale `R` is usually 60–90 px, so an overhang of roughly 80–115 px clears it.

**How to check it.** Export the frame and look at its bottom edge. If you can see any part of a curve there, it is wrong. You should see either no device at all (contained) or two straight vertical lines (bled). The same test applies to the top edge whenever the device bleeds upward.

**Zebra is exempt.** A zebra set alternates the interface between overflowing the top and overflowing the bottom; overflow is the point of the style, and the contained option does not apply to it. The straight-cut principle still gives a cleaner edge there, but zebra is not bound by the choice above.

**Contained and bled are both legitimate; a half-cropped corner is not.** The two relationships below are the only ones allowed, and the choice holds for the whole set. What is never allowed is the frame edge cutting through the device's corner radius.

**Editorial page furniture.** One screen in a set can drop the interface entirely and become a magazine page: a contents list, page numbers in the corner, an illustration. It works because it breaks the rhythm and signals craft. Use it once per set at most.

## Scaling app screens

Product files are built at 1x. When a 375 px screen is placed at 1000 px in a storefront it is being magnified nearly three times, and every detail tuned for the small size is magnified with it. Check these after scaling:

- **Status bar.** Low-opacity battery outlines vanish and their solid fill reads as a blob. Repaint the indicators solid, or hide the bar. Play requires battery, wifi and signal to appear full.
- **Hairlines and dividers.** A 1 px rule becomes a 3 px band and starts competing with real content. Thin them back.
- **Small icons and vector caps.** Rounded caps and joins that looked crisp at 1x turn soft. Replace anything that matters at the larger size.
- **Body copy.** Text that was deliberately small in the product becomes prominent in the storefront and can pull attention away from the headline.

None of this means the screen is wrong. It means it was drawn for a different size, and the storefront is a different medium.

## Device handling

- **Keep the device upright.** No tilt. A rotated screen looks careless rather than dynamic, and it makes the interface inside harder to read at gallery size. Rotation belongs only to the photographed-object treatment below, where the whole set commits to it; it is never a way to add interest to an otherwise flat layout.
- **Photographed as a real object.** The device held in a hand, lying on a wooden table, hanging from a rope, tilted at an angle in a real environment. This makes a minimal app feel tangible and is very effective for games and utilities with sparse interfaces.
- **Multiple devices stacked in perspective.** Two or three screens layered receding into depth, showing a flow rather than a single state.
- **Glow outline on the frame.** A neon contour in the accent colour around the device. Suits dark, gaming and anime registers.
- **A mascot or character breaking the device boundary.** The figure overlaps and passes outside the frame edge, which creates depth and gives the mascot agency.
- **Floating labels ringing the device.** Small capsules naming features, positioned around the device and pointing at it.

## Integrating photography and illustration

**Never drop an image in as a bare rectangle.** A hard-edged photo or illustration sitting in the middle of a frame reads as a placeholder someone forgot to finish. Artwork has to be bound into the composition, and there are only a few ways that actually work.

**Full bleed is the default.** Let the artwork fill the whole frame and run off all four edges, then lay a gradient over it and set the type on the gradient. This is the strongest treatment and the one to reach for first. A contained image needs a reason.

**The gradient is what makes the type readable, so build it deliberately.** One flat dark overlay across the whole image kills the artwork. Use a stack instead: a moderate scrim at the end where a wordmark or small label sits, and a much heavier one at the end carrying the headline, each fading to fully transparent in the middle so the artwork breathes. Three or four stops beat two — a straight linear fade looks mechanical.

**Put the type where the artwork is quiet, and check the subject.** Before fixing the headline position, look at where the focal point of the image actually lands. If the headline covers a face or the main subject, move the type, not the picture. Scaling artwork to dodge a headline usually means zooming far enough to wreck the composition; moving the headline to the other end costs nothing. A cover with the subject in the upper half and the type in the lower third is a reliable arrangement.

**If the artwork cannot be full bleed, bind it in another way.** Bleed it off at least one edge so it is never a floating rectangle. Fade one edge into the ground with a gradient mask. Let a foreground element or the type overlap it. Or give it a deliberate container — generous rounded corners, a hairline edge, a shadow — so it reads as an intentional card rather than an unfinished crop.

**Match the slot to the artwork's real aspect ratio.** Measure the source and size the slot to it, so nothing is squashed and nobody has to re-crop later. Name the layer `ASSET SLOT / ...` with the pixel dimensions in the name when the artwork is going to be filled in by someone else.

**Tie the artwork to the palette.** If the illustration is built on one dominant colour, use that colour as the set's accent rather than fighting it with an unrelated one. An image that shares no colour with the type looks pasted on however well it is masked.

## Filling the gap between headline and interface

Aligning the device tops across a set means the screens with shorter headlines end up with a band of bare ground. Left alone it reads as a mistake — the eye sees a hole, not breathing room. Anything past roughly a fifth of the frame height needs something in it.

**Measure before you place.** The gap is not always between the headline and the interface, and assuming it is will put the filler in the wrong place. List every empty band on the screen: above the first element, between each pair of elements, and below the last one. Take the tallest and centre the filler in it. On a screen where the interface bleeds off the top edge and the copy sits directly under it, the largest band is usually the run of ground below the subline, not the narrow slot between the interface and the headline.

**Then even out the spacing around it.** Placing the row in the right band is only half the job; the gaps on either side of it have to match. Take the free region left by the interface, subtract the text block height and the icon row height, and divide what remains by three. That gives one value for all three gaps: edge to text, text to icons, icons to the interface or the far edge. Never eyeball it — a difference of forty or fifty pixels is invisible while you are working and obvious in the finished strip.

Two things make this go wrong. Moving the interface to make the arithmetic easier breaks the alignment line the set depends on, so hold it still and move the type and the icons instead. And positioning the headline lines and the subline separately lets their internal spacing drift; treat the text as one block, measure from its top to its bottom, and move the whole thing.

**Different screens in one set can fill different bands.** That is fine and it is not the same as breaking the set's consistency: the tiles keep the same size, spacing, style and accent logic everywhere, and only their vertical position follows the space. What must not happen is a row jammed into a thin slot while a much larger emptiness sits untouched further down.

**Icon tiles are the reliable filler.** Three small rounded tiles, one glyph each, sitting in a row in the gap. They earn their place because each glyph names a capability the headline is claiming, so the band carries meaning instead of decoration.

- Three is the working number. Two looks unfinished, four starts competing with the interface.
- Keep them small relative to the device — roughly a sixth of the frame width.
- Space them evenly and hold the same size, so the row reads as deliberate. A couple of degrees of rotation on alternating tiles keeps it from looking like a toolbar; more than that and it looks careless.
- Colour one of the three in the accent and leave the others neutral, and move which one is accented from screen to screen. That gives the set rhythm without adding elements.
- Glyphs, not words. If the same idea has to be spelled out in text, it belongs in the subline instead.

**The filler has to belong to the set, not just sit in it.** Anything dropped into the gap is read as part of the design, so it inherits every decision the set has already made. Work through them before drawing:

- **Meaning first.** Each glyph answers the headline directly above it. A screen headlined about charts gets a candle, a clock and a layers mark. A screen about drills gets a tick, a cross and a lightbulb. If a glyph would fit equally well on any screen in the set, it is decoration and does not belong.
- **Drawing style follows the interface.** Look at the icons inside the app screen and match them. Line icons in the product mean line icons in the gap, at a stroke weight that reads the same at that size. Filled and rounded product icons mean filled and rounded fillers. A hairline outline set next to chunky filled product icons looks borrowed from another project.
- **Colour comes from the palette, never from outside it.** Neutral glyphs take the set's text colour; the accented one takes the set's accent. If the set runs a hue per screen, the accented glyph takes that screen's hue, which is also the cleanest way to make the spectrum legible across the strip.
- **Container matches the set's surfaces.** The tile takes the same corner radius language, the same fill and border treatment, and the same shadow as the cards and buttons elsewhere in the set. If the set uses translucent glass panels, the tiles are translucent glass panels. If it uses solid pills, they are solid pills.
- **Weight sits between the headline and the interface.** The tiles should be quieter than the headline and quieter than the screen. If your eye lands on them first, reduce the contrast — usually by dropping the fill opacity rather than by shrinking them.
- **Alignment follows the text, not the frame.** Left-aligned copy means the row starts on the same left margin as the headline. Centred copy means a centred row. A centred row under a left-aligned headline is the most common way this goes wrong.
- **Light and dark grounds need different handling.** On a dark ground a translucent white tile with a hairline edge works; the same recipe on a light ground disappears, and needs a tinted fill or a soft shadow instead.

**Other things that work in the gap.** A single oversized glyph or numeral behind the interface at low opacity. A short row of avatars. One floating card tucked behind the device edge so only part of it shows. Whatever goes there should sit visually between the headline and the interface in weight — quieter than both.

**What does not work.** Stretching the headline to fill the space, which breaks the size consistency across the set. Enlarging the device on that one screen, which breaks the top alignment. Scattering elements at random positions and angles, which reads as clutter rather than composition.

## Bento sets

The screen is not one composition; it is a grid of rounded panels with the ground showing between them. Each panel holds one idea. The repetition of radius and gutter is what makes it read as a system rather than as scattered boxes.

**Set the grid once and never break it.** One outer margin, one gutter between panels, one corner radius on every panel. The gutter and the margin are usually close in size. Once those three numbers are fixed, every screen in the set is built from them.

**Panel heights vary; panel widths snap to the grid.** A panel is either full width or half width, with two halves sharing a row. Height is whatever the content needs. That variation in height is the rhythm of the style, so avoid making every panel the same depth.

**The ground must stay visible.** The gaps between panels are the design. If panels touch or the gutter shrinks to a hairline, the whole thing collapses back into an ordinary layout.

**One idea per panel.** A headline with its subline. A single statistic. An award mark. A cropped piece of interface. Two unrelated ideas in one panel defeats the point.

**Interface is cropped by the panel, not shown as a phone.** No device frame; the app screen is scaled to the panel width and the panel clips it. Crop deliberately: land the cut cleanly above or below the status bar, never through it, and show the part of the screen the headline is about.

**Vary the composition screen to screen.** Headline panel on top with interface below; two stat panels then a headline; interface on top with the headline beneath; a full-bleed accent panel carrying a number. The panels stay consistent while their arrangement changes — that is what stops a bento set feeling repetitive.

**One accent panel at most per screen.** Most panels are white or near-white on a tinted ground. A single panel filled with the accent colour or a gradient, carrying white type, gives the screen its focal point. Two accent panels on one screen fight each other.

**Statistics are the natural content for small panels.** A large numeral with a small caption underneath. Only ever a figure the brief supplies; see the numeric claims section.

**Ease off on the cover.** The grid applies there too, but at a lower count. Where a feature screen runs four, five or six panels, the cover runs two or three and no more. The cover's job is a single clear message, and a busy grid competes with the masthead for the one look most people give it.

Fewer panels must not mean a weaker cover. Keep the same margin, the same gutter and the same radius, so it still reads as part of the set, and let the panels be larger: a tall masthead panel carrying the wordmark, the headline and the supporting line, then one or two panels under it — a cropped interface, an award or rating, a short row of what is inside. Full-width panels suit the cover better than halves, because a half-width panel makes the cover look like a dashboard.

The failure to avoid is a cover that has quietly become a feature screen with more boxes. If you cannot tell within a second which panel carries the message, there are too many.

**Where bento sets fail.** Uneven gutters. Different radii on different panels. Panels so tall they become a single-panel screen. Interface cropped through the status bar. Every screen using the same panel arrangement.

## Fun sets: abstract shape backgrounds

A light, energetic register built on a moving background rather than a flat one. It reads as playful without becoming childish, provided the shapes stay in their place.

**Build one shape language and reuse it.** Pick four or five element types and no more — a large soft blob, an arc or partial ring, a wave, a dot grid, a triangle is a workable set. Every screen draws from the same five. What changes between screens is the arrangement, not the vocabulary.

**Rearrange, do not redraw.** Blob left and arc right on one screen, reversed on the next; the wave high on one, low on another. This is where the movement comes from. If each screen invents new shapes the set stops looking designed.

**Three or four shapes per screen.** Enough for life, few enough to stay quiet. The cover can carry five or six because it is doing more work.

**Large blobs are colour fields, not objects.** Give them a heavy layer blur and an opacity around a fifth. Blurred, they read as light on the ground; sharp, they read as shapes competing with the phone.

**Line elements stay thin and few.** One wave or one arc per screen, at a stroke weight that reads at gallery size without becoming a bar across the composition.

**Shapes never enter the type block.** This is the rule that keeps the style from collapsing. A wave crossing a subline or a dot grid behind a headline destroys legibility, and it is the easiest mistake to make because the shapes are placed before the type. Place the shapes, place the type, then look again and move any shape that has ended up under words.

**Shapes go behind the device, never over it.** The interface is the product; the background is decoration. Nothing overlaps the phone.

**Pull the type accent from the shape palette.** Colouring the second line of each headline in one of the background colours ties the two layers together. Rotate which colour is used, screen to screen.

**Use a rounded, friendly typeface.** A geometric grotesque fights the shapes; something with soft terminals agrees with them.

**Where fun sets fail.** Shapes over the interface. A wave through the copy. Six different shape types across five screens. Blobs left sharp so they look like stray circles. Every screen using the same arrangement, which throws away the one thing the style is for.

## Minimalist sets

A recognisable family, and a demanding one: with almost nothing on the screen, every remaining decision is visible. What follows is what the strong examples share.

**Minimalist does not mean black and white.** This is the most common misreading. The discipline is about how few colours are used and how little is on the screen, not about which colours they are. A deep navy ground with a pale blue mark, a warm sand ground with dark brown type, or a soft green ground with near-black type are all minimalist. Take the ground and the ink from whatever palette the brief specifies and apply the restraint to how they are used.

**One ground, held across the whole set.** A single flat colour, usually low in saturation and high or low enough in value to carry text comfortably. If the palette is neutral, avoid pure white, which looks unfinished next to the store's own chrome; a warm off-white or cream sits better. No gradients, no glows, no texture. Rhythm comes from the artwork changing, not the ground.

**Count the colours and keep the count low.** A ground, an ink, and at most one muted secondary for a panel or a subline. Everything else on the composition is one of those three. Whatever appears inside the app screen is exempt — that is the product, not the design. What breaks the style is a fourth colour introduced for emphasis: a coloured word in the headline, an accent glow, a bright badge. Where a louder set reaches for colour, a minimalist set reaches for weight.

**One mark above the headline.** A small drawing or a single solid glyph, centred, sitting above the type, in the ink colour. It does the job that icon tiles do elsewhere — naming the feature — but there is one of it, not three, and it is drawn rather than boxed. Line art with a consistent stroke weight, or a solid silhouette; not both in one set.

**Two type sizes and nothing else.** A large heavy display line, and a smaller regular subline. No kickers, no labels, no mono captions, no third size. The headline is usually a plain noun phrase — "Live charts", "Family calendar" — with no verb and no claim.

**Emphasis by weight, never by colour.** If one word needs to stand out, set it in a heavier cut of the same face, or in the italic. This is the one place these sets allow themselves a flourish.

**Symmetry.** Centred type, centred mark, centred device, equal margins left and right. The few left-aligned examples still hold a strong vertical axis. A minimalist set with ragged alignment reads as unfinished rather than restrained.

**Emptiness is the material.** Expect half the frame to be ground. The instinct to fill it is the main way these sets get ruined — resist adding a badge, a sticker, a floating card or a second illustration. If a screen feels empty, the fix is usually to enlarge the artwork and re-space, not to add another element.

**The device is plain.** Upright, a simple black or white bezel, bleeding off the bottom edge. No rotation, no glass, no glow, at most a very soft shadow. Some sets drop the device entirely on one screen and show a tinted panel of app content instead.

**The cover follows the same rules, only bigger.** Wordmark at the top, the largest headline in the set, the largest drawing, one supporting line, and a single quiet row at the bottom — press marks, a rating, or simply the names of what is inside. That bottom row is the only place these sets put credibility, and it stays in the ink colour rather than introducing a new one.

**Where minimalist sets fail.** Reading the style as "make it grey" and throwing away the brand palette. Three type sizes instead of two. A fourth colour introduced on one screen for emphasis. Filling the empty half with decoration. Artwork in two incompatible drawing styles across the set. A neutral ground set to pure white so it reads as a missing background.

## Overflow

Let the interface break out past the edges of the device. Done properly this is the strongest device in storefront design; done as a card dropped on top of a phone it looks like a sticker.

**What overflows is the interface itself, not a separate card.** Rebuild the relevant part of the screen at a larger scale and place it over the device. The phone stops being a container and becomes a silhouette behind the content. A white card floating in front of the phone, with its own shadow, covering the screen underneath, is the failure mode — it has no relationship with the device, it just hides it.

**Measured from real sets, the numbers are consistent:**

- **Width: about 118% of the device width.** The observed range is 110–124%. The content is deliberately wider than the phone.
- **Break out on both sides, evenly.** Twenty-nine of thirty examples were centred exactly on the device's vertical axis, with the left and right overflow equal at roughly 9% of the device width per side. Single-sided break-out is not used at this scale.
- **Stay inside vertically.** The overflowing block sits well within the top and bottom of the device — a few hundred pixels of inset at each end is normal. The break is horizontal; it does not also spill over the top or the bottom.
- **Small emphasis elements are the exception.** Badges, buttons and labels around half the device width do break out on one side only, by roughly 10–12% of the device width. Two techniques, two scales: large content breaks symmetrically, a small accent escapes on one side.

A representative example: a 895 px device with three stacked cards at 1055 px wide over it, starting 57 px below the top of the phone and ending 57 px above the bottom, overflowing 80 px on each side.

**Why the technique exists.** Three reasons, and they are worth keeping in mind because they tell you when it is worth using.

- *Legibility.* At gallery size a screenshot is tiny. Interface scaled to fit inside a phone becomes unreadable; at 118% it reads, and the device still supplies the context.
- *Hierarchy.* Everything inside the phone has equal weight. The element that crosses the boundary marks itself as the subject of the screen.
- *Depth.* Breaking the silhouette turns a flat screenshot into a composition. A shadow does not achieve this; crossing the boundary does.

**How to build it.** Take the part of the interface the headline is about, scale it to 115–120% of the device width, centre it on the device's vertical axis so both overflows are equal, and inset it top and bottom so it stays within the device vertically. For a small accent instead, take one element at around half the device width and let it cross a single edge by 10–12%.

**What must not happen.** Content visible twice, once inside the device and once in the overflow — scroll the screen behind it or rebuild it so the overflowing part is the only copy. Overflow narrower than the device, which reads as a pasted card. Uneven left and right overflow when the block is symmetric. Overflow that also spills past the top or bottom of the device without reason. Rotation.

**On flat exports.** This needs interface you can rebuild or re-lay out. If all you have is a flat image of a finished screen, you cannot enlarge one region of it without cropping the rest badly. Say so and propose a different treatment rather than delivering a ragged crop.

## Overlay layers

- **Handwritten annotation over the interface.** Green arrows, a circled figure, a note reading "Healed!". This directs the eye to the proof point and reads as human rather than corporate. Very effective over charts and numbers.
- **Rotated star-shaped sticker badge** carrying a short claim.
- **A row of avatars or icons along the bottom edge**, showing community or supported services.
- **Two to four floating elements**, slightly rotated, clustered in the middle-to-lower region and overlapping the device edge. They never intrude on the headline area; the top of the frame stays typographic.

## Background and colour strategy

Four strategies. They are mutually exclusive; mixing them makes a set look unplanned.

1. **One image or gradient spanning the whole set.** A sky, a map, a forest, a single deep gradient. The gallery reads as a panorama when swiped.
2. **A different flat colour per screen.** Rhythm comes from the colour change rather than the artwork.
3. **Alternating light and dark.** Black, white, white, black. The contrast itself becomes the rhythm and makes each screen feel like a new statement.
4. **One ground colour held across the set**, with variety carried entirely by the interface and the artwork.

Palette families that recur in the sample:

- A single vivid gradient across the set: hot red, deep blue.
- Vivid flat colours changing per screen: blue, black, turquoise, purple.
- Cream ground, black type, one pink or pastel accent.
- Deep navy or near-black ground with a neon cyan or electric accent.
- Black ground with multi-coloured type accents, one accent colour per screen.
- Light lavender or pale blue ground with a saturated blue accent and illustration.

## Laying the set out

Space the frames 50 px apart on the canvas and give each frame a 75 px corner radius. These two are defaults rather than preferences: apply them whenever the brief is silent, and override them only when the brief names a different value. They are not something to raise or ask about.

 Reviewing a set with wide gutters flatters it: each screen gets judged on its own, and the problems that only appear in sequence — a headline that jumps size, a device that shifts height, three screens sharing one silhouette — stay invisible until the listing is live. A tight gutter reproduces the strip the store actually shows, so those faults surface while they are still cheap to fix.

## The cover

**Every set must have a cover, and it must be built differently from the rest.** This is a requirement, not a preference. In the gallery the cover is the only screen a large share of people will ever look at, and a cover that repeats the feature-screen template throws away the most valuable slot in the listing.

A feature screen answers "what does it do". The cover answers "why should I care". Those need different layouts.

Build a cover to this shape:

- **Headline-heavy.** The type is the composition. Larger than any other screen in the set, usually filling the upper or middle third on its own.
- **A message, not a feature.** Motivational, or a sharp claim about the reader's situation. "Learn the market before it teaches you" belongs on a cover; "Read candles in seconds" belongs on screen two.
- **No device, or a device reduced to a fragment.** If every screen in the set carries a phone, the cover is where the phone comes out.
- **Its own furniture.** A wordmark, a rule, a footer line, a short index of what is inside — elements that appear nowhere else in the set.
- **Check the vertical balance.** A headline-only cover leaves a large empty region by default. Either move the type block to the optical centre, or add a second element in the lower third. Empty bottom thirds are the usual failure.
- **The app name, on every cover.** House rule. Set it as a wordmark, normally at the top of the frame, in the set's own typeface and one of its colours. Keep it small — a fraction of the headline size — because its job is identification, not persuasion. Letter-spacing it slightly and setting it in caps or lowercase to suit the set both work; what does not work is pasting in a logo file that shares nothing with the typography around it. Use the exact name given in the brief.
- **A "#1 App" badge, on every cover.** House rule. Build it as a laurel pair flanking a large #1 with a short qualifier beneath — the category, or whatever the claim actually is — and style it to the set: gold on a dark ground, ink on a light one, the accent hue on a colourful one. Draw the laurel leaves alternating on both sides of the stem and tapering toward the tip, or they read as wheat rather than laurel.
- **Two conditions travel with that badge.** It needs a real, current ranking behind it, and the wording should narrow to whatever is genuinely true — a category, a country, a period — rather than an unqualified claim. It also comes off any set going to Google Play, which prohibits ranking and award motifs in screenshots outright. Note in the delivery summary that the badge is present and needs verifying.

If the brief asks for five screens, that means a cover plus four feature screens unless the brief says otherwise. Confirm rather than silently producing five feature screens.

**The rest of the set holds one template.** Consistency across screens two to N is what makes the set read as designed; the cover breaking that pattern is what gives it a front door.

**Feature lists appear as a vertical stack of pills or chips**, beside or below the interface, rather than as prose.

**Do not clone a screen to make the next one.** Vary silhouette, composition and colour temperature between consecutive screens.

## Variant sets

To produce A/B variants, hold the composition and swap the surface. The same set can ship as a bright pastel version and a cream version with identical layout, headline positions and interface placement, changing only ground colour and type colour. This isolates the variable being tested and costs a fraction of a redesign.

When asked for variants, ask what is being tested. If it is colour, change only colour. If it is the message, keep the visual system fixed and change only the copy.

## Credibility marks

- **Press logo row** beneath the cover headline, with a small "As seen on" or similar label.
- **A research or source line** above the headline, naming an institution or study.

Both need to be true and permitted. See the section below.

## Social proof

**It appears on the cover only** in almost every set, either directly under the headline or pinned to the bottom edge. Repeating it across screens dilutes it and burns space features need. The exception is a brief that names a particular screen for it; then it goes on that screen and not on the cover.

Common forms: a star rating, award and laurel motifs, and a large number used as the headline itself.

**A user review is different from the rest and is never added on your own initiative.** Include one only when the brief asks for it. A rating or a count is a figure that can be checked and corrected later; a review is a sentence attributed to a person, and inventing one is prohibited outright by both stores. When the brief does ask, use the real review text and keep whatever attribution the store requires.

## Third-party marks and numeric claims

These patterns are widely used and commercially effective, and each carries risk that belongs to the person briefing the work, not to the designer quietly deciding alone. Use them when the brief asks, and say in the delivery summary that they were used and why.

**Third-party app icons and logos.** Showing Instagram, TikTok, Snapchat, Reddit, X, Pinterest or Facebook marks — for example crossed out in a blocker app — is common in that category. Both stores prohibit using third-party trademarks without permission, so this needs the brief to confirm rights or accept the risk.

**Institutional logos and research citations.** A university or publisher logo implies endorsement. It needs permission, and the claim it supports needs to be accurate. In health-adjacent categories a research citation also has to avoid becoming a medical claim.

**Awards, editorial badges and rankings.** Laurels, "Editors' Choice", "App of the year", "#1 in category". Standard on the App Store when genuinely earned and current. Google Play prohibits ranking, award and store-performance motifs in screenshots outright.

**Numeric claims.** Download counts, user counts, rating averages, ratings volume, "trusted by 1M". Fine when the brief supplies the figure and it is current. Never invent one, never round up, and never draw five stars when the live rating is lower.

See `store-policies.md` for the underlying rules and the pre-delivery checklist.
