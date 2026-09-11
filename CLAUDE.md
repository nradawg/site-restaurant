# Tier 1: Quick Landing Page

## Stack
- Single index.html + style.css
- Tailwind CSS via CDN: `<script src="https://cdn.tailwindcss.com"></script>`
- No framework, no build step
- Deploy as static files to Vercel

## Structure
- Hero section with headline + CTA button
- Features/services section (3-4 items with icons)
- About or social proof section
- Contact info (address, phone, hours, Google Maps embed if local)
- Footer with links and social icons

## Rules
- Read `user_config.json` — all business info (name, colors, phone, address, social links) comes from there. Inline the values into the HTML.
- Images: use https://images.unsplash.com for relevant stock photos. Use descriptive alt text.
- Mobile-first responsive design. Test at 375px and 1440px widths.
- SEO: proper `<title>`, `<meta description>`, Open Graph tags, semantic HTML (`<header>`, `<main>`, `<section>`, `<footer>`)
- Accessibility: proper heading hierarchy (one h1), alt text on all images, sufficient color contrast
- No JavaScript unless absolutely needed (smooth scroll is fine)
- Keep it under 3 files total: index.html, style.css (if needed beyond Tailwind), and user_config.json

## Quality Bar
- Looks like a $1,000+ website on mobile AND desktop
- Lighthouse score > 90 on Performance and Accessibility
- No console errors
- Loads in under 2 seconds
- Deploy command: `vercel --prod`
