# Heritage at Stonebridge Homes

Real estate landing page for Summerlin's premier gated community. Built with Next.js 14, Tailwind CSS, and TypeScript.

**Agent:** Dr. Jan Duffy | **Brokerage:** Berkshire Hathaway HomeServices Nevada Properties

## About

Heritage at Stonebridge Homes showcases luxury real estate in Heritage at Stonebridge, a premium gated community in Summerlin, Las Vegas. The site supports lead capture, community information, and contact for buyers and sellers.

## Features

### Technical Stack

- [Next.js](https://nextjs.org) 14 for static site generation
- [Tailwind CSS](https://tailwindcss.com) for styling
- [TypeScript](https://www.typescriptlang.org) for type safety
- PostCSS with `styled-jsx`
- ESLint and Prettier
- Husky and lint-staged for Git hooks

### Heritage-Specific

- LocalBusiness / RealEstateAgent JSON-LD schema
- FAQ schema (FAQPage) for common Heritage at Stonebridge questions
- Lead capture form with API route (`/api/leads/submit`)
- Google Business Profile support: NAP (Name, Address, Phone), Call, Directions, Reviews links
- `robots.txt` and `sitemap.xml`
- Security headers (X-Content-Type-Options, X-Frame-Options, X-XSS-Protection, Referrer-Policy)

### Next.js Built-in

- Minify HTML & CSS
- Live reload in development
- Cache busting

## Project Structure

```
.
├── README.md
├── next.config.js
├── public
│   ├── assets/images
│   ├── robots.txt
│   └── sitemap.xml
├── src
│   ├── background
│   ├── button
│   ├── components      # FAQSection, LeadCaptureForm, MapEmbed, CommunityHighlights
│   ├── cta
│   ├── feature
│   ├── footer
│   ├── hero
│   ├── layout
│   ├── navigation
│   ├── pages
│   │   └── api/leads    # Lead submission endpoint
│   ├── styles
│   ├── templates
│   └── utils
├── tailwind.config.js
└── tsconfig.json
```

## Requirements

- Node.js and npm

## Getting Started

```bash
cd heritageatstonebridgehomes
npm install
npm run dev
```

Open http://localhost:3000

## Customization

Update NAP and site settings in `src/utils/AppConfig.ts`:

- `business.phone`, `business.address`, `business.email`
- `googleBusinessProfileUrl`, `googleReviewsUrl`, `googleMapsEmbedUrl`

**Important:** NAP (Name, Address, Phone) must exactly match your Google Business Profile. Verify monthly.

Other customization:

- `public/favicon.ico`, `public/apple-touch-icon.png`: favicon
- `src/styles/global.css`: global CSS
- `src/templates/*`: page sections (Hero, Footer, Banner, etc.)

## Deploy

### Local production build

```bash
npm run build
npm run start
```

### Netlify

`netlify.toml` is configured. Connect the repo to Netlify for one-click deploy.

### Vercel

Import the project in [Vercel](https://vercel.com) and deploy.

## VSCode (optional)

Suggested extensions in `.vscode/extension.json`. Debug config included for frontend development.

## License

MIT License. See [LICENSE](LICENSE).

Based on [Next-JS-Landing-Page-Starter-Template](https://github.com/ixartz/Next-JS-Landing-Page-Starter-Template).
