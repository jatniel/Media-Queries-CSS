# Media Queries CSS

> A comprehensive collection of CSS media queries for real-world devices — phones, tablets, laptops, and wearables. Uses **modern, standards-compliant syntax** (`width`, `height`, `resolution`) with zero vendor prefixes.

## Why this exists

Writing responsive CSS for specific devices means hunting down viewport sizes, pixel ratios, and the right media query syntax. This repo gives you **ready-to-use, copy-paste snippets** for 100+ devices, kept up to date with current hardware.

All queries follow the modern CSS spec:

```css
/* Modern (what we use) */
@media only screen and (min-width: 393px) and (max-width: 852px) and (resolution: 3dppx) { }

/* Deprecated (what we replaced) */
@media only screen and (min-device-width: 393px) and (-webkit-min-device-pixel-ratio: 3) { }
```

## Quick start

```bash
# Clone the repo
git clone https://github.com/AJGuzman/Media-Queries-CSS.git

# Or just grab the file you need
curl -O https://raw.githubusercontent.com/AJGuzman/Media-Queries-CSS/master/Phones/iPhones.css
```

Import only what you need:

```css
@import url('Phones/iPhones.css');
@import url('Tablets/iPad.css');
@import url('Laptops/Laptops.css');
```

## Device coverage

### Phones

| File | Devices | Notes |
|------|---------|-------|
| [`iPhones.css`](Phones/iPhones.css) | iPhone 4/4S through iPhone 17 Pro Max, iPhone 17 Air | Grouped by shared viewport dimensions |
| [`Samsung-Galaxy.css`](Phones/Samsung-Galaxy.css) | Galaxy S21–S25 (Standard/Plus/Ultra), Z Flip 4–6, Z Fold 4–6, A54–A56 | Foldables include cover + unfolded queries |
| [`Google-Pixel.css`](Phones/Google-Pixel.css) | Pixel 6–9, 6a–8a, Pro/Pro XL variants, Pixel Fold, 9 Pro Fold | Foldables include cover + unfolded queries |
| [`OnePlus.css`](Phones/OnePlus.css) | OnePlus 12/13, 12R/13R, Nord 4/CE 4, OnePlus Open | New |
| [`Xiaomi.css`](Phones/Xiaomi.css) | Xiaomi 14/15 Pro/Ultra, MIX Fold 4, Redmi Note 13/14, POCO F6/X6 | New |
| [`HTC.css`](Phones/HTC.css) | HTC One | Legacy — historical reference |
| [`Windows-Phone.css`](Phones/Windows-Phone.css) | Windows Phone | Legacy — historical reference |

### Tablets

| File | Devices | Notes |
|------|---------|-------|
| [`iPad.css`](Tablets/iPad.css) | iPad 1–10th gen, Mini 1–7th gen, Air 1–5th gen (M1–M2), Pro 9.7"–13" (M1–M5) | Includes Ultra Retina XDR OLED tandem displays |
| [`Samsung-Galaxy-Tablet.css`](Tablets/Samsung-Galaxy-Tablet.css) | Galaxy Tab 2, Tab 3, Tab 4 | |
| [`Nexus-Tablet.css`](Tablets/Nexus-Tablet.css) | Nexus 7, Nexus 9 | |
| [`Kindle-Fire.css`](Tablets/Kindle-Fire.css) | Kindle Fire HD 7", 8.9" | |

### Laptops

| File | Ranges | Notes |
|------|--------|-------|
| [`Laptops.css`](Laptops/Laptops.css) | HD (1366px) through 4K/UHD (3840px) — 7 breakpoint ranges | Non-retina and HiDPI variants |

### Wearables

| File | Devices |
|------|---------|
| [`Apple-Watch.css`](Wearables/Apple-Watch.css) | Apple Watch |
| [`Moto-360-Watch.css`](Wearables/Moto-360-Watch.css) | Moto 360 Watch |

## Project structure

```
Media-Queries-CSS/
├── Phones/
│   ├── iPhones.css
│   ├── Samsung-Galaxy.css
│   ├── Google-Pixel.css
│   ├── OnePlus.css          ← new
│   ├── Xiaomi.css           ← new
│   ├── HTC.css              ← legacy
│   └── Windows-Phone.css    ← legacy
├── Tablets/
│   ├── iPad.css
│   ├── Samsung-Galaxy-Tablet.css
│   ├── Nexus-Tablet.css
│   └── Kindle-Fire.css
├── Laptops/
│   └── Laptops.css
└── Wearables/
    ├── Apple-Watch.css
    └── Moto-360-Watch.css
```

## What changed (v2.0)

The entire codebase was modernized to use **standard CSS media features**:

| Deprecated | Modern replacement |
|---|---|
| `device-width` / `device-height` | `width` / `height` |
| `-webkit-device-pixel-ratio` | `resolution` (dppx) |
| `-webkit-min-device-pixel-ratio` | `min-resolution` (dppx) |

**Phones** — Added 50+ current models (iPhone 14–17 series, Galaxy S21–S25, Pixel 6–9, OnePlus, Xiaomi). Removed discontinued devices (Galaxy S3–S6, Pixel 1/XL). Foldables have both cover and unfolded screen queries.

**Tablets** — Added iPad mini 6–7th gen, iPad 10th gen, iPad Air M1–M2, iPad Pro M1–M5 including 13" Ultra Retina XDR OLED tandem displays.

**Laptops** — Expanded from 2 ranges to 7, covering HD (1366px) through 4K/UHD (3840px) with HiDPI support.

## Contributing

Found a missing device or incorrect viewport? PRs welcome.

1. Fork it
2. Create your branch (`git checkout -b add-device-name`)
3. Use modern syntax — no vendor prefixes
4. Submit a PR

## License

[MIT](LICENSE) — Jatniel Guzmán
