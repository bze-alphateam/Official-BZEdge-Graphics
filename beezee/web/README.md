# BeeZee website icons

Favicons and install icons for getbze.com and any other site that speaks for BeeZee itself rather than for one app. They are made from the round BZ mark (`../alternative/bz-logo.svg`). The apps have their own icons in `../apps`.

Copy the files next to the site's `index.html`. The PNG and ICO files sit at the top of the folder for that reason.

## Files

```
favicon.ico            16 + 32 (small cut) + 48
favicon-16.png         small cut
favicon-32.png         small cut
apple-touch-icon.png   180 × 180 tile on solid black
icon-192.png           the mark, transparent corners
icon-512.png           the mark, transparent corners
maskable-512.png       512 × 512 tile; the mark sits inside the 80 % safe zone
svg/icon.svg           the mark, unchanged
svg/icon-small.svg     small cut for 16 and 32 px
svg/app-tile.svg       the tile used for apple-touch and maskable
```

## Small cut

At 16 and 32 px the outlined b of the mark disappears. The small cut fills the b solid by dropping its inner cut-out, as the "by beezee" endorsement wordmark does. From 48 px up the mark is used unchanged.

## Tile

The mark's disc is pure black, so the tile is pure black (`#000000`) and the two read as one surface. Use the tile wherever a platform needs a square, opaque icon.

## HTML

```html
<link rel="icon" href="/favicon.ico" sizes="48x48">
<link rel="icon" href="/favicon-32.png" type="image/png" sizes="32x32">
<link rel="icon" href="/favicon-16.png" type="image/png" sizes="16x16">
<link rel="apple-touch-icon" href="/apple-touch-icon.png">
```

In the web manifest, list `icon-192.png` and `icon-512.png`, plus `maskable-512.png` with `"purpose": "maskable"`, one size per entry.
