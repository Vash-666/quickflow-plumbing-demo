# Local Service Business Template

**Professional website template for plumbers, electricians, HVAC, cleaners, and other local service businesses.**

Built with Next.js, optimized for AI discovery (LLM SEO), mobile responsive, and ready to customize.

---

## Quick Start

```bash
# Install dependencies
npm install

# Run development server
npm run dev

# Open http://localhost:3000
```

## Customize for Your Business

Edit `src/config/site.ts` with your business details:

```typescript
export const siteConfig = {
  businessName: "Your Business Name",
  tagline: "Your Tagline",
  phone: "(555) 123-4567",
  email: "hello@yourbusiness.com",
  // ... more options
}
```

**All customization in one file.** No coding required.

---

## Pages Included

| Page | Purpose |
|------|---------|
| **Home** | Hero, services preview, testimonials, FAQ, CTA |
| **Services** | Detailed service listings, pricing, FAQ |
| **About** | Business story, team, credentials, trust signals |
| **Contact** | Functional form, hours, map, emergency info |

---

## LLM SEO Features

This template includes **Generative Engine Optimization (GEO)** — designed to be recommended by AI assistants like ChatGPT, Claude, and Grok.

**What's included:**
- ✅ JSON-LD structured data (LocalBusiness, Service, FAQPage)
- ✅ Answer-first content structure
- ✅ FAQ schema markup
- ✅ Clear entity signals (business, location, services)
- ✅ Semantic HTML for AI parsing

---

## Tech Stack

- **Framework:** Next.js 16 (App Router)
- **Language:** TypeScript
- **Styling:** Tailwind CSS
- **Components:** shadcn/ui
- **Forms:** React Hook Form + Zod
- **Icons:** Lucide React

---

## Build for Production

```bash
npm run build
```

Static files output to `out/` directory. Deploy to Vercel, Netlify, or any static host.

---

## Template Configuration

### Business Info

```typescript
businessName: "Your Business Name",
tagline: "Your Tagline",
serviceType: "Plumbing", // or "Electrical", "HVAC", etc.
phone: "(555) 123-4567",
emergencyPhone: "(555) 123-4567",
email: "hello@yourbusiness.com",
```

### Address & Service Area

```typescript
address: {
  street: "123 Main St",
  city: "Your City",
  state: "ST",
  zip: "12345",
},
serviceArea: "Your Metro Area",
serviceAreaList: ["City1", "City2", "City3"],
```

### Services

```typescript
services: [
  {
    name: "Service Name",
    shortDescription: "Brief description",
    description: "Full description",
    features: ["Feature 1", "Feature 2"],
  },
  // Add more services...
],
```

### Branding

```typescript
primaryColor: "#0066cc",
siteUrl: "https://yourbusiness.com",
yearEstablished: "2010",
yearsInBusiness: 15,
licenseNumber: "Your License #",
```

### Business Hours

```typescript
businessHours: {
  "Monday": "8:00 AM – 6:00 PM",
  "Tuesday": "8:00 AM – 6:00 PM",
  // ... etc
  "Sunday": "Closed",
},
```

### Testimonials

```typescript
testimonials: [
  {
    quote: "Best service ever!",
    name: "John D.",
    location: "Your City, ST",
  },
  // Add more...
],
```

---

## Images

Replace placeholder images in `public/`:

| File | Usage |
|------|-------|
| `hero.jpg` | Home page hero background |
| `about-owner.jpg` | About page team photo |
| `logo.png` | Site logo |

**Recommended sizes:**
- Hero: 1920x1080px
- About photo: 800x600px
- Logo: 200x200px (transparent PNG)

---

## Deployment

### Vercel (Recommended)

1. Push to GitHub
2. Import to Vercel
3. Set framework preset to "Next.js"
4. Deploy

### Netlify

1. Build: `npm run build`
2. Publish directory: `out`
3. Deploy

### Static Hosting

Upload `out/` directory to any static host (Cloudflare Pages, AWS S3, etc.)

---

## Contact Form

The contact form uses React Hook Form with Zod validation.

**To connect to a backend:**

1. Create API route at `src/app/api/contact/route.ts`
2. Use EmailJS, Formspree, or custom backend
3. Update form submission handler in `src/components/sections/contact-form.tsx`

**Example with Formspree:**
```typescript
const onSubmit = async (data) => {
  await fetch("https://formspree.io/f/YOUR_FORM_ID", {
    method: "POST",
    headers: { "Content-Type": "application/json" },
    body: JSON.stringify(data),
  });
}
```

---

## Customization Tips

### Change Colors

Edit `primaryColor` in `site.ts` — updates buttons, links, accents throughout.

### Add/Remove Services

Add to `services` array in `site.ts`. Icons auto-match based on service name keywords.

### Modify FAQ

Edit `homeFAQ` and `serviceFAQs` arrays in page files. Keep questions relevant to your business.

### SEO Meta Tags

Edit in `src/lib/metadata.ts` — page titles, descriptions, OG tags.

---

## Support

Questions? [Open an issue](https://github.com/Vash-666/ai-website-studio/issues)

---

**Built with AI Website Studio** — Professional websites in minutes.
