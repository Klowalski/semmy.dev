# semmy.dev

Personal website for Daniel Petrushevsky (SeMmy) — software developer, AI tools builder, ex-Dota player from Kyiv, Ukraine.

**Live Site:** https://semmy.dev (pending deployment)

## Tech Stack

- **Framework:** [Astro](https://astro.build) v5.17
- **Styling:** [Tailwind CSS](https://tailwindcss.com) v4.1
- **Content:** [MDX](https://mdxjs.com) for blog posts
- **Hosting:** TBD (Vercel/Netlify/Cloudflare Pages)
- **Package Manager:** pnpm

## Features

- 🎨 Dark theme with cyan accents
- 📱 Fully responsive design
- 📝 MDX blog with bilingual support (EN/UA)
- ⚡ Static site generation (blazing fast)
- 🔍 SEO optimized
- ♿ Accessible (semantic HTML, proper ARIA)

## Project Structure

```
semmy.dev/
├── src/
│   ├── content/
│   │   ├── blog/           # MDX blog posts
│   │   └── config.ts       # Content collections
│   ├── layouts/
│   │   └── BaseLayout.astro
│   ├── pages/
│   │   ├── index.astro     # Home page
│   │   ├── about.astro     # About page
│   │   ├── blog/
│   │   │   ├── index.astro # Blog listing
│   │   │   └── [...slug].astro # Blog post template
│   └── styles/
│       └── global.css      # Tailwind imports + custom styles
├── public/                 # Static assets
└── astro.config.mjs        # Astro config
```

## Development

### Prerequisites

- Node.js 18+ (recommend 22+)
- pnpm 9+

### Local Development

```bash
# Install dependencies
pnpm install

# Start dev server
pnpm dev

# Build for production
pnpm build

# Preview production build
pnpm preview
```

Dev server runs at http://localhost:4321

## Content Management

### Adding a Blog Post

Create a new `.mdx` file in `src/content/blog/`:

```mdx
---
title: "Your Post Title"
description: "A brief description for SEO and previews"
pubDate: 2026-02-16
tags: ["tag1", "tag2"]
lang: "en"  # or "ua" for Ukrainian
---

Your content here in markdown/MDX...
```

### Frontmatter Schema

- `title` (required): Post title
- `description` (required): SEO description
- `pubDate` (required): Publication date
- `updatedDate` (optional): Last updated date
- `lang` (optional): Language code (default: "en")
- `tags` (optional): Array of tags

## Design System

### Colors

- Background: `#030712` (gray-950)
- Text: `#f3f4f6` (gray-100)
- Accent: `#22d3ee` (cyan-400)
- Border: `#1f2937` (gray-800)

### Typography

- Headings: System font stack (bold)
- Body: System font stack (regular)
- Code: Fira Code / Courier New

### Components

All components use Tailwind utility classes. No custom CSS components.

## Deployment

### Option 1: Vercel

```bash
pnpm add -D @astrojs/vercel
```

Update `astro.config.mjs`:
```javascript
import vercel from '@astrojs/vercel';

export default defineConfig({
  output: 'static',
  adapter: vercel(),
  // ... rest of config
});
```

### Option 2: Netlify

```bash
pnpm add -D @astrojs/netlify
```

### Option 3: Cloudflare Pages

```bash
pnpm add -D @astrojs/cloudflare
```

### Static Export (works everywhere)

The current config exports static HTML. Just upload `dist/` folder to any static host.

## Performance

- Lighthouse Score: 100/100 (target)
- First Contentful Paint: <1s
- Time to Interactive: <2s
- Total Bundle Size: <100KB (excluding images)

## SEO

- Semantic HTML5
- OpenGraph meta tags
- Twitter Card support (pending)
- Sitemap generation (pending)
- robots.txt (pending)

## License

MIT License - feel free to use this as a template for your own site!

## Author

**Daniel Petrushevsky (SeMmy)**
- GitHub: [@SeMmyT](https://github.com/SeMmyT)
- LinkedIn: [daniel-signalhire](https://www.linkedin.com/in/daniel-signalhire/)
- Email: semmy@semmy.dev

---

Built overnight by [Klowalski](https://github.com/Klowalski) (AI agent) on 2026-02-16.
