[![SATUS](https://assets.darkroom.engineering/satus/banner.gif)](https://github.com/darkroomengineering/satus)

# Satūs

A modern, high-performance React application starter with Next.js 15, React 19, Tailwind CSS v4, and advanced WebGL capabilities. Satūs means "start" or "beginning" in Latin, serving as a foundation for new projects.

## Quick Start

```bash
# Install dependencies
bun install

# Setup environment variables
cp .env.example .env.local

# Start development server with Turbopack
bun dev

# Build for production
bun build

# Start production server
bun start
```

## 🛠 Tech Stack

- **[Next.js 15.3.2](https://nextjs.org)** - React framework with App Router and Turbopack
- **[React 19.1.0](https://react.dev)** - Latest React with simplified ref handling
- **[TypeScript](https://www.typescriptlang.org)** - Type-safe development
- **[Tailwind CSS 4.1.7](https://tailwindcss.com)** - CSS-first configuration
- **[React Three Fiber](https://docs.pmnd.rs/react-three-fiber)** - React renderer for Three.js
- **[GSAP 3.13.0](https://greensock.com/gsap/)** - Timeline-based animations
- **[Biome 1.9.4](https://biomejs.dev)** - Fast formatter and linter
- **[Bun](https://bun.sh)** - All-in-one JavaScript runtime

## 📁 Project Structure

```
satus/
├── app/                    # Next.js App Router pages and layouts
├── components/             # Reusable UI components
├── hooks/                  # Custom React hooks
├── integrations/           # Third-party service integrations
│   ├── hubspot/           # HubSpot forms integration
│   ├── shopify/           # E-commerce functionality
│   └── storyblok/         # Headless CMS
├── libs/                   # Utility functions and helpers
├── orchestra/              # Debug and development tools
│   ├── grid/              # Grid overlay
│   ├── minimap/           # Page minimap
│   ├── stats/             # Performance stats
│   └── theatre/           # Animation tools
├── styles/                 # Global styles and configuration
├── webgl/                  # 3D graphics and WebGL components
└── public/                 # Static assets
```

## Key Features

### Performance Optimized
- **Turbopack** for lightning-fast HMR in development
- **React Server Components** by default
- **Dynamic imports** for code splitting
- **Image optimization** with a custom thin wrapper around Next.js Image
- **Font optimization** with Next.js Font

### Modern Styling
- **Tailwind CSS v4** with CSS-first configuration
- **CSS Modules** for component styles
- **Custom viewport units** (`mobile-vw`, `desktop-vw`)
- **Theme support** with CSS variables

### Advanced Graphics
- **WebGL/Three.js** integration with React Three Fiber
- **Post-processing effects** pipeline
- **Shader support** with GLSL
- **Theatre.js** for animation debugging
- **Optimized 3D performance**

### Developer Experience
- **TypeScript** with strict mode
- **Biome** for consistent code style
- **Hot Module Replacement** with Turbopack
- **Git hooks** with Lefthook
- **Debug tools** accessible with `CMD+O`

### Third-Party Integrations boilerplate
- **Storyblok** - Headless CMS for content management
- **Shopify** - E-commerce with cart functionality
- **HubSpot** - Forms and marketing automation

## 🎨 Styling System

### CSS Modules
Components use CSS modules with the `s` import convention:

```tsx
import s from './component.module.css'

function Component() {
  return <div className={s.wrapper} />
}
```

### Responsive Design
Custom viewport functions for responsive sizing:

```css
.element {
  width: mobile-vw(150);    /* 150px at mobile viewport */
  height: desktop-vh(100);  /* 100px at desktop viewport */
}
```

### Theme Variables
CSS variables for consistent theming:

```css
.element {
  color: var(--color-text);
  background-color: var(--color-background);
}
```

## 🔧 Development Tools

### Debug Panel (CMD+O)
- **Theatre.js Studio** - Visual animation editor
- **FPS Meter** - Performance monitoring
- **Grid Overlay** - Layout debugging
- **Minimap** - Page overview

### Available Scripts

```bash
# Development
bun dev              # Start dev server with Turbopack
bun dev:https        # Start with HTTPS

# Building
bun build            # Production build
bun analyze          # Bundle analysis

# Code Quality
bun lint             # Run Biome linter
bun typecheck        # TypeScript checking

# Styling
bun setup:styles     # Generate style files
bun watch:styles     # Watch style changes
```

## 🌐 Environment Variables

Create a `.env.local` file based on `.env.example`:

```env
# Storyblok CMS
STORYBLOK_ACCESS_TOKEN=your_token_here

# Shopify
SHOPIFY_DOMAIN=your-store.myshopify.com
SHOPIFY_STOREFRONT_TOKEN=your_token_here

# HubSpot
HUBSPOT_ACCESS_TOKEN=your_token_here
```

## 📚 Documentation

- [Component Guidelines](/.cursor/rules/components.mdc)
- [Styling Guidelines](/.cursor/rules/styling.mdc)
- [WebGL Development](/.cursor/rules/webgl.mdc)
- [Integration Guide](/.cursor/rules/integrations.mdc)
- [Tailwind CSS v4 Reference](/.cursor/rules/tailwind-css-v4.mdc)

## Deployment

### Vercel (Recommended)
```bash
vercel
```

## Git Workflow

### Automated Git Hooks (via Lefthook)
- **Pre-commit**: Runs Biome to check and format staged files
- **Post-merge**: Automatically pulls latest environment variables from Vercel

### Other Platforms
The project supports deployment to any platform that supports Next.js:
- Netlify
- AWS Amplify
- Google Cloud Run
- Self-hosted with Node.js

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/fix-everything`)
3. Commit your changes (`git commit -m 'Add fix everything feature'`)
4. Push to the branch (`git push origin feature/fix-everything`)
5. Open a Pull Request

## 📄 License

MIT © [darkroom.engineering](https://github.com/darkroomengineering)