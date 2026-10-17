# BeeZee app identity

Each BeeZee web app has its own icon, logos and Open Graph image: DEX, Staking, Burner, Factory, Communities and Explorer. The family is one dark BZE disc with an app-coloured ring. Inside it sits an app glyph, slanted 10° like the BeeZee b-mark. Every logo carries the "by beezee" endorsement.

All text in the SVGs is converted to outlines (Barlow, SIL Open Font License), so no font has to be installed.

## Files per app

```
<app>/
  icon/svg/icon.svg                  full icon, for 48 px and up
  icon/svg/icon-on-dark.svg          same, lighter disc for dark backgrounds
  icon/svg/icon-small.svg            small cut for 16–32 px (thicker ring, no inner details)
  icon/svg/icon-small-on-dark.svg
  icon/svg/app-tile.svg              square tile (apple-touch / maskable), full bleed
  icon/png/icon-512.png, icon-192.png, icon-on-dark-512.png
  icon/png/favicon-16.png, favicon-32.png     (small cut)
  icon/png/apple-touch-icon.png      180 × 180 tile
  icon/png/maskable-512.png          512 × 512 tile; the glyph and ring sit inside the 80 % safe zone
  icon/favicon.ico                   16 + 32 (small cut) + 48
  landscape/svg/landscape-light.svg, landscape-dark.svg   icon + name + "by beezee"
  compact/svg/compact-light.svg, compact-dark.svg         icon + name (mobile navbar)
  portrait/svg/portrait-light.svg, portrait-dark.svg      stacked
  */png/*@3x.png                     PNG renders of the lockups at 3×
  og/og-image.png, og-image.svg      1200 × 630, for openGraph and twitter:summary_large_image
endorsement/svg/by-beezee-wordmark-light.svg, -dark.svg   the endorsement wordmark on its own
```

"light" and "dark" name the background the file is meant for.

## Which lockup where

| Lockup | Use |
| --- | --- |
| Landscape | Desktop navbar and anything wider than tall. Icon 32 px or larger. |
| Compact | Mobile navbar. Icon 24–32 px. |
| Portrait | Splash and loading screens, docs, avatars with a caption. |
| Icon | Favicon (small cut at 16 and 32 px), wallet-connect icon, token lists, PWA icons. |

Keep a quarter of the icon's height clear on every side. The gap between icon and name is the same quarter.

## The endorsement wordmark

"by beezee" uses the official wordmark with the b filled solid: the inner cut-out of the b is removed, so only its outer silhouette is drawn. The outlined b of the original wordmark disappears at small sizes. The original wordmark (`../landscape`, `../portrait`) is unchanged and stays the BeeZee logo on its own.

## Colours

| App | Light end | Dark end | Ink (text and buttons on light) | On dark |
| --- | --- | --- | --- | --- |
| DEX | `#12C1E1` | `#1694D2` | `#0E74AD` | `#12C1E1` |
| Staking | `#B57EDC` | `#8E44AD` | `#8E44AD` | `#B57EDC` |
| Burner | `#FF8A1F` | `#E85A00` | `#C24A00` | `#FF8A1F` |
| Factory | `#FFC933` | `#E09B00` | `#9A6A00` | `#FFC933` |
| Communities | `#3DD07A` | `#1E9150` | `#1A7A43` | `#3DD07A` |
| Explorer | `#22C4E2` | `#1694D2` | `#0B74A8` | `#22C4E2` |

- Glyph and ring run from the light end to the dark end: the glyph top to bottom, the ring diagonally.
- The ink colours keep white button text at a contrast of 4.5:1 or better.
- The Explorer keeps the accent of its own interface, which sits close to the DEX cyan. Its magnifier glyph tells the two apart.
- Shared colours: disc `#0F1318` (on light) or `#1B2128` (on dark), text `#14171C`.
- Type: Barlow 700 for the app name, Barlow 500 for "by".

## Keep it intact

- No glyph without its disc and ring.
- No recolouring: each glyph keeps its app colours.
- No stretching, rotating or added effects.
- Below 32 px use the small cut.
- No outlined b in the endorsement.
- Never set the app name in another typeface.
