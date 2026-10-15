# Store policies for screenshots

Read this before designing, and again before delivery. Everything here comes from Apple's App Review Guidelines and Google Play's Metadata, Store Listing and Preview Asset policies. Where the two stores disagree, the stricter rule is the safe default, because one set of artwork usually ships to both.

Policies change. If a set is going to a real submission, verify the current text in App Store Connect and Play Console rather than trusting this file.

## Contents

- [Never put these on a screenshot](#never-put-these-on-a-screenshot)
- [Apple](#apple)
- [Google Play](#google-play)
- [Dimensions](#dimensions)
- [Localisation](#localisation)
- [Rights and trademarks](#rights-and-trademarks)
- [Pre-delivery checklist](#pre-delivery-checklist)

## Never put these on a screenshot

These are hard prohibitions, not style preferences. Each one is an established rejection reason.

**Ranking, award and store-performance claims.** No "#1", "App of the year", "Best of Play 20XX", "Popular", "Top", "Editor's choice", no award icons, no laurel wreaths implying a prize. Google Play bans these explicitly in text and image form. Apple treats unverifiable superlatives as inaccurate metadata. If a client insists on a ranking claim, it needs a documented, current source and it still should not ship to Play.

**Price and promotional wording.** No "Free", "10% off", "$50 cash back", "free for a limited time only", "Discount", "Sale". Google Play bans these in screenshots and taglines. Apple bans pricing information in metadata under 2.3.7. This catches common CTA copy: "Start free" and "Try free" are promotional price claims. Prefer "Get started" or "Begin".

**Call-to-action overlays.** Google Play advises against "Download now", "Install now", "Play now", "Try now" in screenshot copy. The user is already on the listing; the button is the store's job.

**Store badges.** No Google Play badge, no App Store badge, no other store's icon or badge inside a screenshot. Google bans this outright. Apple separately bans imagery of other mobile platforms in its metadata, so an Android or Play reference on an App Store screenshot is a 2.3.10 rejection.

**Unattributed testimonials.** No invented quotes, no anonymous "This app changed my life". If a quote is used it needs an attributed, real source.

**Fabricated social proof.** Only use a rating, a review count or a user count that the person briefing you supplies and can evidence. Never invent one, never round one up, and never draw five stars when the live rating is lower — that specific dark pattern is named in Play's enforcement.

**Content unsuitable for a general audience.** Both stores require store listings to suit a general audience regardless of the app's age rating. No sexually suggestive imagery, no fetishised anatomy, no graphic violence, no depictions of drug use, no profanity. Apple requires screenshots to hold to a 4+ rating even when the app is rated higher.

**Fingers on the device.** Google Play says not to show people interacting with the device unless the core usage is genuinely off-device.

**Fake or aspirational UI.** Both stores require screenshots to reflect the app as it actually is. Do not invent a feature, a screen or a state that the build does not have.

## Apple

- **2.3, accurate metadata.** Screenshots must accurately reflect the app's core experience and stay current with new versions.
- **2.3.3.** Screenshots must show the app in use. Marketing or promotional material that does not reflect the app's UI is not appropriate. The majority of screenshots should highlight the app's main features and functionality. This is the rule that catches sets which are mostly typography and artwork with a token slice of interface.
- **Device frames must match the device.** iPhone screenshots are taken on iPhone, iPad screenshots on iPad. Showing an iPhone-shaped frame in an iPad slot is a documented rejection.
- **2.3.7.** No trademarked terms, popular app names, pricing information or irrelevant phrases stuffed into metadata to game search. App names are capped at 30 characters.
- **2.3.8.** Screenshots must suit a 4+ audience even if the app is rated higher. "For Kids" and "For Children" are reserved for the Kids Category.
- **2.3.9.** You are responsible for securing rights to every element in icons, screenshots and previews.
- **2.3.10.** No names, icons or imagery of other mobile platforms.

## Google Play

- **Metadata policy.** No misleading, non-descriptive, irrelevant, excessive or inappropriate metadata, and screenshots are named as metadata. Everything in this file applies to every localisation of the listing, not only English.
- **Taglines are capped.** Add a tagline only if it is needed to convey a key characteristic, and it must not take up more than 20 percent of the image. A set built around a large headline on every screen will breach this if the headline dominates.
- **Interface first.** Screenshots must demonstrate the actual in-app experience. Stylised sets that break a single UI across several images are allowed, but the first three screenshots should prioritise interface as much as possible.
- **Device imagery is discouraged.** Play advises against device frames in screenshots because they date quickly and can alienate users on other hardware. This is guidance rather than a hard ban, but it means a phone-mockup composition is a worse default on Play than on the App Store.
- **Status bar hygiene.** If a real capture is used, clean the notification bar. No carrier name, no notifications; battery, wifi and signal should read full.
- **Quality.** No blurry, stretched, compressed, rotated or skewed images.
- **Time-sensitive content.** Avoid copy that dates, and swap seasonal artwork out when the season ends.
- **Alt text.** Recommended for every asset, 140 characters or fewer, describing what the screen shows. Do not begin with "image of".
- **Licence note.** Publishing on Play grants Google a licence to use the app's assets, including screenshots, for promotion. Assume anything delivered may appear in Google's own marketing.

## Dimensions

**Apple, portrait iPhone and iPad.** 6.5 inch is 1242×2688, 6.9 inch is 1320×2868, 13 inch iPad is 2048×2732. Apple's required set changes; confirm in App Store Connect before delivery.

**Google Play, phone.** JPEG or 24-bit PNG with no alpha channel. Minimum edge 320 px, maximum edge 3840 px, and the long edge must not exceed twice the short edge. Between two and eight screenshots per device type. To be eligible for Play's recommendation formats, supply at least four screenshots at 1080 px or more, 9:16 portrait at a minimum of 1080×1920 or 16:9 landscape at a minimum of 1920×1080.

**This is a trap worth remembering.** Apple's portrait phone sizes fail Play's aspect rule. 1320×2868 is 2.17:1 and 1242×2688 is 2.16:1, both beyond the two-to-one limit. iPhone artwork cannot simply be re-uploaded to Play. Build Play portrait assets at 1080×1920, or reflow the design rather than letterboxing it.

**Feature graphic, Play only.** 1024×500, JPEG or 24-bit PNG without alpha. Keep the focal point central because the edges get cropped in some placements. Avoid pure white, black and dark grey, which blend into Play's background. No device imagery, no store badges.

**Play app icon.** 512×512, 32-bit PNG with alpha, under 1024 KB, and no badges or text implying ranking or price.

## Localisation

- Any screenshot containing text needs a separate version per supported language. Both stores require this.
- Every rule in this file applies to every translation. A banned phrase is still banned in Turkish, Spanish or German.
- Apple additionally requires that the app looks and behaves identically across languages and supported devices.
- German and Turkish headlines run long; Japanese and Korean run short. Keep the layout fixed and adjust line breaks, then check that no headline reflows into artwork.
- Right-to-left languages mirror alignment and icon direction.

## Rights and trademarks

- Secure rights for every element that is not original work: photography, illustration, typefaces, icons, music in a preview video.
- No third-party trademarked characters or logos without written permission. No celebrity name or likeness without permission.
- Do not imply endorsement by, or a relationship with, another company or entity where none exists, and do not claim to be the "official" app of an organisation unless you are.
- Scripture, poetry, song lyrics and literary text carry copyright unless the specific translation or edition is in the public domain. For scripture, KJV is public domain; NIV, ESV, NLT and most modern translations are not. Quote exactly, name the translation, and confirm the licence before setting the text.

## Pre-delivery checklist

Run this before handing a set over, and report the result.

1. Does any screen contain a ranking, award, "#1" or laurel motif? Remove it.
2. Does any copy contain a price or promotional word, including "free"? Rewrite it.
3. Does any copy read as a call to action to install? Rewrite it.
4. Is there a store badge anywhere? Remove it.
5. Are all ratings, review counts and user numbers supplied and evidenced by the brief? If not, remove them.
6. Would every screen pass a 4+ audience check?
7. Does the set show real interface, and do the first three screens lead with interface?
8. On Play sets, does the tagline stay under a fifth of the image?
9. Do the dimensions match the destination store, including Play's two-to-one aspect limit?
10. Is every text-bearing screen produced for each target language?
11. Is every non-original element cleared for use?

Report anything you removed or refused, and say why. A quiet omission is worse than a flagged one, because nobody learns the rule.
