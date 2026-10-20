# Hive Glow: the BeeZee apps UI theme

Hive Glow is the shared look of the BeeZee web apps: DEX, Staking, Burner, Factory and Communities. The rule is **one layout, five colours**. Every app uses the same ground, cards, type, buttons and hero. Only the app gradient changes, and it comes from the app icons in `../<app>/`.

The theme is brand-wide. Neutrals, type, buttons, cards and the glow apply to getbze.com and any other BeeZee interface too. The five app gradients belong to their apps.

Dark mode is the default. Light mode swaps the neutrals and uses each app's Ink colour wherever you read or press something.

## Files

```
tokens.json                      every token, dark and light (design-tokens format: $type / $value)
tokens.css                       the same as CSS variables (--hg-*)
gradients/<app>.svg, png/<app>.png   the app gradient with its hex stops
glow/<app>-hero-glow-dark.svg    the hero glow background, 1440 × 720
glow/<app>-hero-glow-light.svg
specimen/hive-glow-dark.svg/.png the whole system on one sheet, per mode
specimen/hive-glow-light.svg/.png
```

All files are generated. Don't edit them by hand: change the source values and export again.

## Using tokens.css

Put `data-app="dex"` (or `staking`, `burner`, `factory`, `communities`) on `<html>` or `<body>`. For light mode add `data-theme="light"` or the class `light`. Then use the semantic variables:

| Variable | What it is |
| --- | --- |
| `--hg-ground`, `--hg-card`, `--hg-inset`, `--hg-hairline` | page, card, input/inset surface, card edge |
| `--hg-text`, `--hg-text-muted`, `--hg-text-faint` | text tones |
| `--hg-primary-bg`, `--hg-primary-text`, `--hg-primary-shadow` | the primary button: gradient on dark, Ink on light |
| `--hg-link`, `--hg-eyebrow` | links and the hero eyebrow in the app colour |
| `--hg-gradient`, `--hg-gradient-word` | the app gradient; the hero word gradient |
| `--hg-glow`, `--hg-glow-inner` | the hero glow for home pages; half strength for inner pages |
| `--hg-featured-edge`, `--hg-featured-shadow` | the 1 px edge and glow of the one featured card |
| `--hg-up`, `--hg-down`, `--hg-info`, `--hg-warning`, `--hg-danger`, `--hg-success` | data and status colours |

The raw per-app values (`--hg-app-1`, `--hg-app-ink`, …) are there too, for anything the semantic set does not cover.

## The rules

**The gradient goes in five places, and nowhere else:**
1. the hero glow behind the top of the page,
2. one word of the hero title,
3. the primary button,
4. icon tiles,
5. the edge of the one featured card on a page.

Everything else is neutral. Secondary buttons, cards, inputs and tables never take the gradient. Tinted hairlines, focus rings, a selected chip and the active nav underline may use the app colour.

**Page structure**
- **Header:** the app's landscape lockup, the app's own nav items, and a gradient wallet button. TESTNET is a separate red pill next to the logo, and testnet builds also show the ribbon at the bottom of the screen.
- **Hero:** an eyebrow (the app icon plus its name in the app colour), a 52 px title with one gradient word, an 18 px subtitle, then one primary and one secondary action. Inner pages use a compact 36 px hero with no gradient word.
- **Stat strip:** three or four numbers in plain cards, in one row. Icons, if any, sit on inset tiles in the app colour.
- **Width:** a 1200 px container on every page, with 24 px gutters (16 px on phones).
- **Cards:** card fill, 8 % white hairline (10 % ink in light mode), 16 px radius, 20–24 px padding. Only one card per page is featured.

**Numbers are never in the app colour.** Use neutral text, or the data colours for change: green up, red down.

**Trading data** uses the data colours as trade sides in every app: buy and bid are green, sell and ask are red (order book, buy/sell forms, BUY/SELL badges, candles). Price impact is green up to 0.5 %, amber above 0.5 % and red above 1 %.

**Amber means "needs care".** The warning amber marks mintable supply, a "No with veto" vote, and lock-up or unbonding periods. Never use orange for this: orange reads as Burner.

**Notices** share one frame: the status colour at 8 % fill, its 30 % edge, a 12 px radius and a 16 px icon. Body text stays muted. They never take the app colour, so a halted asset looks the same in every app.

**Links to other BeeZee apps** are ghost links: no border and no fill. They show the target app's small icon, its name in the target app's colour, and an external-link mark.

**Light mode**
- Buttons are the app Ink with white text.
- Links and the eyebrow use the Ink colour.
- The hero word runs from Ink to a darker Ink.
- The glow drops to about 60 % strength.
- Cards are white with a 1 px shadow.
- Factory exception: small text and links on the light ground use `#8A5F00`, because Factory's Ink is just under 4.5:1 there.

**Staking** keeps a deeper button pair, `#9D5BD2 → #7B3AA6`, with white text, because its icon pair is too light for white text. The glow, hero word, icon tiles and featured edge keep the icon pair.

**Factory** keeps a deeper button pair too, `#D9A62E → #B07C08` (hover `#E4B444 → #C08B12`), because its bright icon yellow glares as a filled button on the dark ground. The dark button text still reads at 5:1 or better. The glow, hero word, icon tiles and featured edge keep the icon pair.

**Communities token pages** don't use the Communities green. They apply Hive Glow with the token's own brand kit:
- the gradient runs from the kit's primary colour to that primary 25 % darker;
- the glow is the primary at 18 % plus the secondary at 10 %;
- the surfaces are derived from the kit.

Status colours stay the shared ones.

**DEX:** Swap is the AMM and Exchange is the order book. Keep them visibly distinct wherever both appear.

**Voice:** personality comes from the copy and the glow, not from emoji or extra fonts. Use one font: Inter, plus JetBrains Mono for fees, denoms and heights.

## Colours

| App | Gradient | Button text (dark) | Ink (light) | Accent text (dark) |
| --- | --- | --- | --- | --- |
| DEX | `#12C1E1 → #1694D2` | `#04131C` | `#0E74AD` | `#7FD8EE` |
| Staking | `#B57EDC → #8E44AD` (button `#9D5BD2 → #7B3AA6`) | `#FFFFFF` | `#8E44AD` | `#D2AEEC` |
| Burner | `#FF8A1F → #E85A00` | `#1A0A00` | `#C24A00` | `#FFB27A` |
| Factory | `#FFC933 → #E09B00` (button `#D9A62E → #B07C08`) | `#1A1200` | `#9A6A00` (small text on ground `#8A5F00`) | `#FFD970` |
| Communities | `#3DD07A → #1E9150` | `#03170B` | `#1A7A43` | `#7FE3A8` |

| Shared | Dark | Light |
| --- | --- | --- |
| Ground | `#0A0C10` | `#F5F7FA` |
| Card | `#12151B` | `#FFFFFF` |
| Inset / input | `#1B2128` | `#EEF1F5` |
| Text / muted / faint | `#E8ECF2` / `#A3ACB9` / `#8A94A3` | `#14171C` / `#5B6472` / `#6B7482` |
| Up / down | `#34D399` / `#F87171` | `#0E8A5A` / `#C93636` |
| Info / warning / danger | `#60A5FA` / `#FBBF24` / `#F87171` | `#2563EB` / `#B45309` / `#C93636` |

Every other value (type scale, radii, spacing, control heights, overlays, testnet colours) is in `tokens.json`.

## Fonts

Inter and JetBrains Mono are both under the SIL Open Font License. The SVG specimens have their text converted to outlines, so they don't need either font installed.
