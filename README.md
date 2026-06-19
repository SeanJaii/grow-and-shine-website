# Grow and Shine Childminding Website

## Production Files
The production static site is now available in this folder:

- `index.html` - homepage
- `gallery.html` - photo gallery with accessible lightbox
- `styles.css` - shared responsive styling
- `site.js` - mobile menu, scroll animation, and lightbox behaviour
- `privacy.html` and `terms.html` - basic information pages
- `images/optimized/` - resized web images used by the production pages

The original `.dc.html` files remain as design handoff references only.

---

# Handoff: Grow and Shine Childminding Website

## Overview
A two-page marketing website for **Grow and Shine Childminding**, a registered childminder / nursery service based in Dagenham, London. The site is aimed at parents and families looking for childcare. The design is playful, warm, and colourful — appropriate for a childminding setting.

## About the Design Files
The files in this bundle (`Grown and Shine Homepage.dc.html` and `Grow and Shine Gallery.dc.html`) are **high-fidelity design references built in HTML**. They are prototypes showing the intended look, layout, animations, and interactive behaviour — not production code to copy directly.

The task is to **recreate these designs in a real web stack** (e.g. Next.js + Tailwind, or plain HTML/CSS/JS if no framework is required) following best practices: semantic HTML, accessible markup, optimised images, real routing, and a contact form backend.

## Fidelity
**High-fidelity.** The prototypes use final colours, typography, spacing, imagery, copy, and interactions. Recreate as close to pixel-perfect as your stack allows.

---

## Pages

### 1. Homepage (`Grown and Shine Homepage.dc.html`)

**Purpose:** Marketing landing page. Introduces the childminder, showcases programs, displays a gallery teaser, and drives enquiries via email/phone.

#### Sections (top → bottom)

---

#### NAV
- Sticky, `z-index: 100`, background `#FFF8EE`
- Box shadow: `0 1px 8px rgba(0,0,0,0.04)`
- Padding: `16px 48px` desktop / `12px 20px` mobile
- **Left:** Logo image (`images/logo.png`) — height `64px`, auto width
- **Right:** Nav links + CTA button
  - "Gallery" link → `/gallery` — `font-size: 15px; font-weight: 600; color: #2D2A32` — hidden on mobile
  - "Book a Visit" button → `mailto:hello@grownandshine.co.uk?subject=Nursery%20Tour`
    - Background: `#FFD166`, color: `#2D2A32`, padding: `10px 24px`, border-radius: `28px`, font-size: `14px`, font-weight: `700`
    - Hover: `translateY(-2px)`, enhanced box-shadow

---

#### HERO
- Background: `linear-gradient(135deg, #4EBFA5 0%, #3AAF94 50%, #45B89E 100%)`
- Padding: `80px 48px 64px` desktop / `40px 20px 36px` mobile
- Floating decorative shapes (circles + toy SVGs — see animations section)
- **Layout:** Two-column flex, `gap: 56px`, stacks to column on mobile

**Left column (text):**
- Badge pill: `background: rgba(255,255,255,0.18)`, `backdrop-filter: blur(8px)`, `padding: 8px 18px`, `border-radius: 24px`
  - Text: ⭐ "Ofsted Outstanding Nursery" — `font-size: 14px; font-weight: 600; color: #fff`
- `<h1>` "Little hands, big adventures" — Baloo 2, `58px` / `36px` mobile / `30px` small, weight `800`, `color: #fff`, `line-height: 1.08`
- Subtext: `18px / 15px mobile`, `color: rgba(255,255,255,0.88)`, max-width `460px`
  - Copy: *"A warm, caring childminding setting where every child is celebrated for who they are. Ages 6 months to 5 years."*

**Right column (image):**
- Container: `width: 480px; height: 480px` desktop → `width: 100%; height: 240px` mobile
- `border-radius: 24px`, `overflow: hidden`, `box-shadow: 0 8px 32px rgba(0,0,0,0.15)`
- Image: `images/hero-main.jpg` — `object-fit: cover`
- Two accent dots (absolute positioned): yellow `#FFD166` circle top-right, coral `#EF767A` circle bottom-left

---

#### TRUST STRIP
- Background: `#fff`, `border-bottom: 1px solid #f0ede6`
- Three equal flex columns, each `border-right: 1px solid #f0ede6` (last has none)
- Padding per item: `32px 20px`
- Stat value: Baloo 2, `36px`, weight `800`; Label: `14px`, weight `600`, color `#999`, uppercase, `letter-spacing: 1px`

| Stat | Colour | Label |
|------|--------|-------|
| 15+ | `#4EBFA5` | Years |
| RN | `#FFD166` | Qualified Nurse |
| NCMA | `#7B9FE0` | Registered |

---

#### PROGRAMS
- Background: `#FFFCF7`, padding `80px 48px` / `48px 20px` mobile
- Heading: `font-size: 14px; color: #4EBFA5; text-transform: uppercase; letter-spacing: 2px` — "Our Programs"
- `<h2>` "How we grow together" — Baloo 2, `42px`, weight `800`
- Sub: "Three rooms, one big family" — `17px`, `color: #888`
- **Three cards flex** (`gap: 24px`), stacks to column on mobile

| Card | BG | Border | Number colour | Age badge BG/text |
|------|----|--------|---------------|-------------------|
| Seedlings | `#FFFBF0` | `#FFE8A3` | `#FFD166` | `#FFF0C2` / `#C9960A` |
| Sprouts | `#F0FAF7` | `#A8E0D0` | `#4EBFA5` | `#D4F0E7` / `#2E8B6E` |
| Blossoms | `#FFF0F0` | `#F5B0B3` | `#EF767A` | `#FCE0E0` / `#C0392B` |

Each card: `border-radius: 24px`, `padding: 36px 32px`, `border: 2px solid`
- Large number (01/02/03): Baloo 2, `52px`, weight `800`, opacity `0.6`
- Title: Baloo 2, `26px`, weight `700`
- Age badge: `font-size: 12px`, `border-radius: 12px`, `padding: 4px 12px`
- Description: `15px`, `color: #666`, `line-height: 1.7`
- Photo: `height: 130px`, `border-radius: 14px`, `object-fit: cover`
  - Seedlings → `images/program-baby.jpg`
  - Sprouts → `images/program-toddler.jpg`
  - Blossoms → `images/program-preschool.jpg`
- Hover: `translateY(-6px)` + coloured box shadow

---

#### OUR STORY
- Background: `#fff`, `border-top: 1px solid #f0ede6`, `border-bottom: 1px solid #f0ede6`
- Padding: `72px 48px` / `48px 20px` mobile — centred, `max-width: 680px`
- Label: `14px`, `color: #EF767A`, uppercase, `letter-spacing: 2px` — "Our Story"
- `<h2>` "A home away from home" — Baloo 2, `38px`, weight `800`
- Body copy (`17px`, `color: #666`, `line-height: 1.8`):
  > *"I am a registered childminder and a qualified nurse with over 15+ years of experience caring for children in both hospital and community settings. I have extensive experience supporting children with special care needs. As a mother of four, I understand the importance of a safe, nurturing environment for every child."*

---

#### GALLERY (teaser)
- Background: `#FFFCF7`, padding `80px 48px` / `48px 20px` mobile
- Header row: heading left, "See all photos →" link right (→ `/gallery`)
- Label: `14px`, `color: #7B9FE0`, uppercase, `letter-spacing: 2px`
- `<h2>` "A peek inside our day" — Baloo 2, `38px`, weight `800`
- **Grid:** `grid-template-columns: 2fr 1fr 1fr`, `grid-template-rows: 180px 180px`, `gap: 16px`
  - On mobile ≤768px: `1fr 1fr`, auto rows `140px`
  - On mobile ≤480px: `1fr`, auto rows `180px`
- Feature image (spans 2 rows): `images/gallery-feature.jpg`
- Small images: `images/gallery-art.jpg`, `images/gallery-play.jpg`, `images/gallery-sleep.jpg`, `images/gallery-music.jpg`
- All: `border-radius: 20px`, `object-fit: cover`

---

#### TESTIMONIALS
- Background: `#FFF8EE`, `border-top: 1px solid #f0ede6`
- Padding: `80px 48px` / `48px 20px` mobile
- Label: `14px`, `color: #FFD166`, uppercase — "Testimonials"
- `<h2>` "What parents say" — Baloo 2, `38px`, weight `800`, centred
- **Three cards flex** (`gap: 24px`), stacks to column on mobile
- Card: `background: #fff`, `border-radius: 20px`, `padding: 32px`, `box-shadow: 0 2px 16px rgba(0,0,0,0.04)`
- Hover: `translateY(-4px)`, `box-shadow: 0 8px 32px rgba(0,0,0,0.08)`
- Stars: `color: #FFD166`, `font-size: 20px`
- Quote text: `16px`, `color: #555`, `line-height: 1.7`, italic
- Avatar: `44px` circle, gradient background, initial letter `font-size: 16px`, `font-weight: 700`

| Quote | Name | Since | Avatar gradient |
|-------|------|-------|----------------|
| "The best decision we ever made for our son..." | James K. | 2022 | `#FFD166 → #FFE8A3` / `color: #A37700` |
| "Wonderful, caring staff..." | Priya T. | 2021 | `#4EBFA5 → #A8E0D0` / `color: #1A6B54` |
| "The daily photo updates make my day..." | Fatima A. | 2023 | `#EF767A → #F5B0B3` / `color: #8B2E30` |

> **Note:** These are placeholder testimonials. Replace with real ones when available.

---

#### CTA + CONTACT (split panel)
- Two equal flex columns, stacks to column on mobile (dark on top)

**Left — Dark CTA:**
- Background: `#2D2A32`, `color: #fff`, padding `72px 56px` / `44px 24px` mobile
- `<h2>` "Ready to start the adventure?" — Baloo 2, `40px`, weight `800`
- Sub: `17px`, `color: rgba(255,255,255,0.7)`
- Buttons row (`gap: 14px`):
  - "Book a Tour" → `mailto:hello@grownandshine.co.uk?subject=Nursery%20Tour`
    - Background: `#FFD166`, color: `#2D2A32`, `border-radius: 32px`, `padding: 15px 32px`, `font-size: 16px`, weight `700`
  - "Call Us" → `tel:07912343431`
    - `border: 2px solid rgba(255,255,255,0.4)`, `color: #fff`, `border-radius: 32px`, `padding: 15px 32px`

**Right — Contact info:**
- Background: `#fff`, padding `72px 56px` / `44px 24px` mobile
- `<h3>` "Find us" — Baloo 2, `28px`, weight `700`
- Three contact rows (icon + text):
  - 📍 Address: 465 Valence Avenue, Dagenham, RM8 3RD
  - 📞 Phone: 07912 343 431 (hours: Mon–Fri, 7:30am – 6pm)
  - ✉ Email: hello@grownandshine.co.uk
- Icon containers: `40px` square, `border-radius: 12px`, tinted backgrounds
- Google Maps embed: `iframe` for "465 Valence Avenue, Dagenham, RM8 3RD", height `160px`, `border-radius: 16px`

---

#### FOOTER
- Background: `#2D2A32`, `color: #fff`
- `border-top: 4px solid #4EBFA5`
- Padding: `48px 56px 36px` / `32px 20px 20px` mobile
- **Left:** Logo in white rounded card (`border-radius: 10px`), tagline below in `color: rgba(255,255,255,0.5)`
- **Right links (two columns flex, `gap: 56px`):**
  - "Explore": Programs, Gallery, About Us, Contact
  - "Contact": phone, email
- **Bottom bar** (border-top `rgba(255,255,255,0.08)`): copyright left, Privacy + Terms right

---

### 2. Gallery Page (`Grow and Shine Gallery.dc.html`)

**Purpose:** Full-page photo gallery showing the nursery environment with a lightbox viewer.

#### Sections

**NAV** — identical to homepage

**HERO**
- Same teal gradient, padding `64px 48px 52px`, text centred
- Label "Gallery" + `<h1>` "A peek inside our day" (Baloo 2, `52px`)
- Subtext: "A glimpse into the warm, creative and joyful space..."
- Floating toy SVG animations (same as homepage)

**MASONRY GALLERY**
- Padding: `64px 48px`
- CSS columns: `column-count: 3` / `2` at ≤768px / `1` at ≤480px, `column-gap: 16px`
- 15 images, all with `break-inside: avoid`, `border-radius: 16px`, `margin-bottom: 16px`
- Hover: `scale(1.02)` + `box-shadow: 0 12px 40px rgba(0,0,0,0.18)`
- Click → lightbox (full-screen overlay, click outside or Escape to close)

**Image list (in order):**
`hero-room.jpg`, `gallery-feature.jpg`, `gallery-2.jpg`, `program-toddler.jpg`, `gallery-art.jpg`, `gallery-3.jpg`, `gallery-play.jpg`, `gallery-4.jpg`, `program-baby.jpg`, `gallery-sleep.jpg`, `gallery-5.jpg`, `program-preschool.jpg`, `gallery-music.jpg`, `gallery-6.jpg`, `hero-main.jpg`

**CTA + CONTACT** — identical structure to homepage version

**FOOTER** — simplified single-row version

---

## Interactions & Behaviour

### Scroll Animations (IntersectionObserver)
All major sections animate in when they enter the viewport (`threshold: 0.12`, `rootMargin: 0px 0px -40px 0px`). Elements start `opacity: 0` and animate to `opacity: 1` with a `transform` reset over `0.75s cubic-bezier(0.22, 1, 0.36, 1)`.

| Element | Animation type | Delay |
|---------|---------------|-------|
| Hero badge | slide-up | 0ms |
| Hero h1 | slide-up | 150ms |
| Hero p | slide-up | 300ms |
| Hero image | scale (0.9 → 1) | 200ms |
| Trust stats | slide-up | 0 / 120 / 240ms stagger |
| Programs heading | slide-up | 0ms |
| Program card 1 | slide-up | 0ms |
| Program card 2 | slide-up | 150ms |
| Program card 3 | slide-up | 300ms |
| Our Story content | slide-up | 0ms |
| Gallery heading | slide-up | 0ms |
| Gallery grid | slide-up | 100ms |
| Testimonial quotes | fade | 0 / 150 / 300ms stagger |
| CTA left panel | slide-left | 0ms |
| CTA right panel | slide-right | 0ms |

### Floating Hero Animations (continuous)
Seven decorative SVG elements float continuously in the hero section using CSS keyframe animations at varying speeds (5–9s) and delays:

- ⭐ Star — top-left, `float3` (tilting float), 7s, delay 0.5s
- 🎈 Balloon — left-middle, `float1`, 8s, delay 1.2s
- ☁️ Cloud — top-centre, `float2`, 9s, delay 0s
- 🎵 Music note — top-right, `float1`, 6.5s, delay 2s
- 💛 Heart — lower-centre, `float3`, 8s, delay 0.8s
- 🟦 Building block "A" — bottom-right, `float2`, 7.5s, delay 1.6s
- ⭐ Small star — far-right, `sway` (rotation), 5s, delay 0.3s

All at `opacity: 0.25–0.4` so they are subtle background decoration.

### Lightbox (Gallery page only)
- Clicking any gallery image opens a full-screen overlay (`background: rgba(0,0,0,0.88)`)
- Image is displayed centred with `max-width: 90vw; max-height: 90vh`
- Click outside image or press `Escape` to close
- `document.body` overflow is set to `hidden` while open

### CTA Buttons
| Button | Action |
|--------|--------|
| Book a Visit / Book a Tour | `mailto:hello@grownandshine.co.uk?subject=Nursery%20Tour` |
| Call Us | `tel:07912343431` |

---

## Responsive Breakpoints

| Breakpoint | Changes |
|------------|---------|
| ≤768px | Nav text links hidden; hero stacks vertically; programs/testimonials stack; CTA split stacks; section padding → `48px 20px`; hero h1 → 36px; gallery grid → 2 columns; masonry → 2 columns |
| ≤480px | Hero h1 → 30px; gallery grid → 1 column; masonry → 1 column |

---

## Design Tokens

### Colours
| Token | Hex | Usage |
|-------|-----|-------|
| Teal (primary) | `#4EBFA5` | Hero bg, nav accent, trust stat, footer border, Sprouts card |
| Teal dark | `#3AAF94` | Hero gradient midpoint |
| Golden yellow | `#FFD166` | CTA buttons, stars, trust stat, heart SVG |
| Coral | `#EF767A` | Blossoms card, balloon SVG |
| Blue | `#7B9FE0` | Trust stat (NCMA) |
| Dark | `#2D2A32` | Body text, CTA panel bg, footer bg |
| Cream (page bg) | `#FFFCF7` | Page background, program section bg |
| Warm cream (nav) | `#FFF8EE` | Nav background, testimonials section bg |
| Card border | `#f0ede6` | Dividers, section borders |
| White | `#ffffff` | Card backgrounds |

### Typography
| Role | Font | Size | Weight | Notes |
|------|------|------|--------|-------|
| Display / headings | Baloo 2 | 52–58px | 800 | Hero h1 |
| Section headings | Baloo 2 | 38–42px | 800 | h2 |
| Card headings | Baloo 2 | 26–28px | 700 | h3 |
| Stat values | Baloo 2 | 36px | 800 | Trust strip |
| Large numbers | Baloo 2 | 52px | 800 | Program card numbers |
| Nav / labels | Nunito | 13–15px | 600–700 | |
| Body | Nunito | 15–18px | 400–600 | |
| Labels / overlines | Nunito | 14px | 700 | Uppercase, letter-spacing 2px |

Google Fonts import: `https://fonts.googleapis.com/css2?family=Baloo+2:wght@400;500;600;700;800&family=Nunito:wght@400;500;600;700&display=swap`

### Spacing
- Section padding (desktop): `80px 48px`
- Section padding (mobile): `48px 20px`
- CTA panel padding (desktop): `72px 56px`
- Footer padding: `48px 56px 36px`
- Card gap: `24px`
- Gallery gap: `16px`
- Nav height: ~64px

### Border Radius
| Element | Radius |
|---------|--------|
| Hero image | 24px |
| Program cards | 24px |
| Buttons | 28–32px |
| Testimonial cards | 20px |
| Gallery images | 16–20px |
| Icon containers | 12px |
| Map embed | 16px |
| Footer logo card | 10px |
| Age badge pills | 12px |

### Shadows
| Element | Shadow |
|---------|--------|
| Testimonial cards (default) | `0 2px 16px rgba(0,0,0,0.04)` |
| Testimonial cards (hover) | `0 8px 32px rgba(0,0,0,0.08)` |
| Yellow buttons | `0 4px 16px rgba(255,209,102,0.25)` |
| Hero image | `0 8px 32px rgba(0,0,0,0.15)` |
| Gallery images (hover) | `0 12px 40px rgba(0,0,0,0.18)` |

---

## Assets

All assets are included in the `images/` folder:

| File | Used in |
|------|---------|
| `logo.png` | Nav + footer on both pages |
| `hero-main.jpg` | Homepage hero |
| `hero-room.jpg` | Gallery page (first photo) |
| `program-baby.jpg` | Seedlings card + gallery |
| `program-toddler.jpg` | Sprouts card + gallery |
| `program-preschool.jpg` | Blossoms card + gallery |
| `gallery-feature.jpg` | Homepage gallery (feature / large image) |
| `gallery-art.jpg` | Homepage gallery + full gallery |
| `gallery-play.jpg` | Homepage gallery + full gallery |
| `gallery-sleep.jpg` | Homepage gallery + full gallery |
| `gallery-music.jpg` | Homepage gallery + full gallery |
| `gallery-2.jpg` through `gallery-6.jpg` | Full gallery page only |

---

## Contact Details (live)
- **Address:** 465 Valence Avenue, Dagenham, RM8 3RD
- **Phone:** 07912 343 431
- **Email:** hello@grownandshine.co.uk
- **Hours:** Mon–Fri, 7:30am – 6:00pm

---

## Files in This Bundle
```
design_handoff_grow_and_shine/
├── README.md                          ← This file
├── Grown and Shine Homepage.dc.html   ← Homepage design reference
├── Grow and Shine Gallery.dc.html     ← Gallery page design reference
└── images/
    ├── logo.png
    ├── hero-main.jpg
    ├── hero-room.jpg
    ├── program-baby.jpg
    ├── program-toddler.jpg
    ├── program-preschool.jpg
    ├── gallery-feature.jpg
    ├── gallery-art.jpg
    ├── gallery-play.jpg
    ├── gallery-sleep.jpg
    ├── gallery-music.jpg
    ├── gallery-2.jpg
    ├── gallery-3.jpg
    ├── gallery-4.jpg
    ├── gallery-5.jpg
    └── gallery-6.jpg
```

To open the design references locally, open either `.dc.html` file in a browser — they work as standalone HTML files. Note that the `.dc.html` extension is specific to this design tool; a developer can rename them to `.html` if needed.
