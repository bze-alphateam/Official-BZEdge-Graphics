# BeePocket identity

BeePocket is the BeeZee browser-extension wallet. Its logo is a plump bee whose striped body tapers into the sting, with swept wings. It belongs to the BeeZee app family: a dark disc, a gradient ring, and a glyph slanted 10°. All text is converted to outlines (Barlow, SIL Open Font License).

The `icon/`, `landscape/`, `compact/`, `portrait/` and `og/` folders follow the same layout and rules as the other BeeZee apps (see `../README.md`). The small cut (`icon-small*.svg`, 16–32 px) keeps one wide stripe and drops the others.

## Chrome extension

```
extension/icon-16.png, icon-32.png        small cut, for light toolbars
extension/icon-16-on-dark.png, -32-…      small cut on the lighter disc, for dark toolbars
extension/icon-48.png, icon-128.png       full icon (extensions page, install dialog)
extension/store/store-icon-128.png        Web Store icon: 96 px artwork inside 16 px transparent padding
extension/store/promo-small-440x280.png   Web Store small promo tile
```

```json
"icons": { "16": "icons/icon-16.png", "32": "icons/icon-32.png", "48": "icons/icon-48.png", "128": "icons/icon-128.png" },
"action": { "default_icon": { "16": "icons/icon-16.png", "32": "icons/icon-32.png" } }
```

The toolbar and store icons always use the default colours. Inside the wallet, the icon is a chameleon: the disc stays dark while the ring, the glyph and the background glow take the colours of the selected token's kit.

## Colours

| | Light end | Dark end | Ink (text and buttons on light) | On dark |
| --- | --- | --- | --- | --- |
| BeePocket (BZE kit) | `#33C3E0` | `#0094C5` | `#0B74A8` | `#33C3E0` |
