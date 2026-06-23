# Sarah Requina — Portfolio Website

Premium personal portfolio for Sarah Requina, Senior Project Manager, Dubai UAE.

## Tech Stack

- **Framework**: Next.js 14 (App Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS with custom design tokens
- **Animation**: Framer Motion + GSAP with ScrollTrigger
- **Fonts**: Cormorant Garamond (display) + DM Sans (body) + DM Mono (utility)
- **Images**: Next.js Image optimization + Unsplash (contextual) + personal portrait

## Sections

1. **Navigation** — Fixed header with scroll spy, mobile menu, CV download
2. **Hero** — Split layout with portrait, animated headline, floating stat badges
3. **About** — Editorial layout with industry tags and working principles
4. **Career Timeline** — Interactive accordion with GSAP-animated timeline line
5. **Case Studies** — Grid cards + full dossier modal (F1, Theme Parks, Consulate, Mena Labs)
6. **PM Framework** — 5-phase process on dark background with scroll-triggered progress
7. **Skills Ecosystem** — Tabbed category browser + tool grid
8. **Achievements Dashboard** — Animated stat counters + achievement cards
9. **Contact** — Cinematic Dubai skyline background + contact form + links

## Setup & Development

```bash
npm install
npm run dev
```

Open [http://localhost:3000](http://localhost:3000)

## Deployment (Vercel)

1. Push this folder to a GitHub repo
2. Connect the repo to [vercel.com](https://vercel.com)
3. Deploy — zero configuration needed

Or via Vercel CLI:
```bash
npx vercel --prod
```

## Customisation Checklist

- [ ] **Hero portrait**: Replace `/public/sarah-portrait.jpg` with your actual photo
  - Recommended: Navy blazer, neutral background, editorial pose
  - Size: 768×1024px minimum, 3:4 ratio
- [ ] **Email**: Update `email` in `src/lib/data.ts`
- [ ] **LinkedIn**: Update `linkedin` in `src/lib/data.ts`
- [ ] **Phone**: Update `phone` in `src/lib/data.ts`
- [ ] **CV file**: Add your CV as `/public/sarah-requina-cv.pdf`
- [ ] **OG image**: Add `/public/og-image.jpg` (1200×630) for social sharing
- [ ] **Domain**: Configure `sarahrequina.com` in Vercel dashboard
- [ ] **Contact form**: Replace the simulated form submission with a real service
  (Recommended: [Resend](https://resend.com), [EmailJS](https://emailjs.com), or [Formspree](https://formspree.io))

## Design Tokens

| Token | Value | Usage |
|-------|-------|-------|
| `parchment` | `#F7F6F2` | Page background |
| `charcoal` | `#1A1A2E` | Primary text, dark sections |
| `gold` | `#C9A96E` | Accent, highlights, CTAs |
| `slate` | `#3D5A80` | Events industry accent |
| `sage` | `#8BAF9A` | Healthcare/diplomatic accent |
| Display font | Cormorant Garamond | Headlines, hero text |
| Body font | DM Sans | Body copy, UI |
| Mono font | DM Mono | Labels, eyebrows, stats |

## Contact Form Integration

The form currently uses a simulated submission. To make it functional, replace the `handleSubmit` function in `src/components/sections/Contact.tsx`:

### Option 1: Resend (recommended)
```bash
npm install resend
```
Create `/src/app/api/contact/route.ts` with a POST handler using the Resend SDK.

### Option 2: Formspree
Change the form action to `https://formspree.io/f/{your-id}`.

### Option 3: EmailJS
```bash
npm install @emailjs/browser
```
Call `emailjs.send()` in the submit handler.
