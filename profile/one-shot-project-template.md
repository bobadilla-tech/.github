# One-Shot Project Template: Ad-Optimized Web Tool Generator

This is a comprehensive prompt template for creating complete, production-ready web tools optimized for Google Ads passive income. Adapt this template for any CLI tool, generator, or utility web app.

---

## 📋 Master Prompt Template

~~~
I want to build a modern, ad-optimized [TOOL_NAME] web application that's better than existing alternatives. The goal is to create a high-quality tool that can generate passive income through Google AdSense while providing genuine value to users.

### Project Requirements

**Core Tool**:
- Build a [DESCRIPTION OF MAIN FUNCTIONALITY]
- Should include [LIST KEY FEATURES]
- Must be better than existing tools like [COMPETITOR_1], [COMPETITOR_2]
- Needs multiple output options (e.g., different formats, variations, etc.)

**Tech Stack Preferences**:
- Use Astro 5.x (for SEO and performance)
- TypeScript (strict mode)
- pnpm as package manager (NOT npm)
- Client-side heavy to minimize hosting costs
- Deploy to Cloudflare Pages (free tier)

**Design Requirements**:
- Modern glassmorphism UI design
- Dark mode with system preference detection
- Fully responsive (mobile-first)
- Smooth animations and transitions
- Professional color scheme that works for both themes

**Monetization**:
- Google AdSense integration with 4 strategic placements:
  1. Leaderboard (728x90) - Between tool and content
  2. Sticky sidebar (300x250) - Desktop only
  3. In-content rectangle (300x250) - Between sections
  4. Mobile anchor - Bottom banner (dismissible)
- Ads should be balanced - not intrusive but maximizing viewability
- Target: ~$400-500/month passive income at 10K monthly visitors

**SEO Optimization**:
- Comprehensive meta tags (title, description, keywords)
- Open Graph tags for social sharing
- Twitter Cards
- Schema.org structured data (JSON-LD)
- Auto-generated XML sitemap with proper priorities
- robots.txt
- 5-7 content-rich pages for backlinks:
  1. Homepage with tool + educational content
  2. [RELEVANT CONTENT PAGE 1]
  3. [RELEVANT CONTENT PAGE 2]
  4. [RELEVANT CONTENT PAGE 3]
  5. Privacy Policy
  6. Terms of Service
  7. Contact

**Features**:
- Keyboard shortcuts for common actions
- Copy to clipboard functionality
- Preset buttons for quick generation
- Real-time character/word counts (if applicable)
- Multiple output formats
- Local storage for preferences

**Branding**:
- Integrate [COMPANY_NAME] branding
- Link to related projects: [PROJECT_1], [PROJECT_2]
- Professional footer with company info
- "For Developers" section linking to [RELEVANT_LIBRARY]
- Social links: GitHub, LinkedIn, Website

### Implementation Steps

**Phase 1: Foundation**
1. Set up Astro 5 project with TypeScript
2. Configure for static site generation
3. Set up pnpm package manager
4. Create directory structure

**Phase 2: Core Tool**
1. Implement main generation algorithm/logic
2. Create utility functions
3. Add error handling
4. Write unit tests (if needed)

**Phase 3: UI Components**
1. BaseHead component (SEO meta tags)
2. Header with navigation and dark mode toggle
3. Footer with branding and links
4. Tool controls component
5. Output display component
6. AdSense container component (reusable)

**Phase 4: Interactivity**
1. Client-side script for tool functionality
2. Keyboard shortcuts
3. Copy to clipboard
4. Dark mode toggle with localStorage
5. Preset buttons

**Phase 5: Content Pages**
1. Homepage with tool + SEO content
2. Educational/informational pages
3. Legal pages (privacy, terms)
4. Contact page

**Phase 6: SEO & Performance**
1. Meta tags and structured data
2. Sitemap configuration with priorities
3. robots.txt
4. Image optimization (OG image as PNG 1200x630)
5. Performance optimization (Lighthouse > 95)

**Phase 7: Monetization**
1. AdSense placeholder components
2. Strategic ad placement
3. ads.txt preparation (for when approved)

**Phase 8: Deployment**
1. Configure for Cloudflare Pages
2. Set up domain
3. Deploy
4. Test all functionality

### Design System

**Colors** (provide or let AI suggest):
- Primary accent: [COLOR_HEX]
- Backgrounds: Light and dark variants
- Text colors: High contrast for accessibility
- Borders and shadows

**Typography**:
- System fonts for performance
- Clear hierarchy
- Readable font sizes (16px base minimum)

**Layout**:
- Max content width: 1200px
- Generous whitespace
- Glass-card effects for sections
- Smooth hover states

### SEO Content Strategy

**Target Keywords**:
- [PRIMARY_KEYWORD_1]
- [PRIMARY_KEYWORD_2]
- [PRIMARY_KEYWORD_3]
- [LONG_TAIL_KEYWORD_1]
- [LONG_TAIL_KEYWORD_2]

**Content Pages**:
Each page should be 500-1500 words, naturally incorporating keywords

1. **Homepage**: Tool + "What is [TOPIC]" section
2. **[CONTENT_PAGE_1]**: Deep dive into [SUBTOPIC_1]
3. **[CONTENT_PAGE_2]**: [SUBTOPIC_2] guide
4. **Alternatives**: Compare with other tools (link to them for backlinks)

### Performance Targets

- Lighthouse Score: > 95/100
- Page Load Time: < 2 seconds
- Core Web Vitals: All "Good"
  - LCP < 2.5s
  - FID < 100ms
  - CLS < 0.1
- Mobile Usability: 100%

### Important Technical Decisions

**Always use pnpm** (never npm or yarn)
- `pnpm install`
- `pnpm dev`
- `pnpm build`

**Astro Configuration**:
- Static output mode
- Sitemap integration with custom priorities
- Image optimization
- Compression enabled

**Git Practices**:
- .gitignore includes `.astro/` and `dist/`
- Commit messages with co-authorship
- Clear, descriptive commits

**Image Requirements**:
- OG image MUST be PNG (1200x630) - social media doesn't support SVG
- Favicon can be SVG
- Optimize all images

### Deployment Configuration

**Cloudflare Pages**:
- Build command: `pnpm build`
- Build output directory: `dist`
- Deploy command: (leave blank - automatic)
- Node version: 18 or 20
- Environment variables: (none needed for static site)

**No wrangler.toml needed** - Cloudflare Pages handles deployment automatically from GitHub

### Project Files Structure

```
project-name/
├── public/
│   ├── images/
│   │   └── og-image.png (1200x630)
│   ├── favicon.svg
│   └── robots.txt
├── src/
│   ├── components/
│   │   ├── layout/
│   │   │   ├── BaseHead.astro
│   │   │   ├── Header.astro
│   │   │   ├── Footer.astro
│   │   │   └── AdContainer.astro
│   │   └── [tool-name]/
│   │       ├── Controls.astro
│   │       └── Output.astro
│   ├── layouts/
│   │   └── BaseLayout.astro
│   ├── lib/
│   │   ├── [tool-logic].ts
│   │   └── [utilities].ts
│   ├── pages/
│   │   ├── index.astro
│   │   ├── [content-1].astro
│   │   ├── [content-2].astro
│   │   ├── privacy.astro
│   │   ├── terms.astro
│   │   └── contact.astro
│   ├── scripts/
│   │   └── [interactive].ts
│   └── styles/
│       └── global.css
├── astro.config.mjs
├── package.json
├── tsconfig.json
├── README.md
├── CHANGELOG.md
└── .gitignore
```

### README Template

Include:
- Project description
- Live demo link
- Features list
- Quick start guide
- Installation instructions
- Project structure
- Core algorithm explanation
- AdSense setup instructions
- SEO optimization details
- Deployment guide
- Performance targets
- Troubleshooting
- Acknowledgments
- Company branding and links

### Deliverables Checklist

- [ ] Fully functional tool with all features
- [ ] 5-7 complete pages with SEO content
- [ ] Google AdSense integration (placeholder IDs)
- [ ] Responsive design (mobile, tablet, desktop)
- [ ] Dark mode with toggle
- [ ] Keyboard shortcuts
- [ ] Copy to clipboard
- [ ] XML sitemap with priorities
- [ ] robots.txt
- [ ] OG image (PNG 1200x630)
- [ ] Structured data (JSON-LD)
- [ ] README.md with full documentation
- [ ] CHANGELOG.md
- [ ] Working deployment on Cloudflare Pages
- [ ] Lighthouse score > 95
- [ ] No build errors or TypeScript warnings
- [ ] All pages indexed in Google Search Console

### Post-Launch Tasks

- [ ] Submit sitemap to Google Search Console
- [ ] Submit sitemap to Bing Webmaster Tools
- [ ] Test social media sharing previews
- [ ] Apply for Google AdSense (if not already approved)
- [ ] Set up analytics (Google Analytics 4)
- [ ] Monitor Core Web Vitals
- [ ] Track rankings for target keywords
~~~

---

## 🎯 Example Adaptations

### Example 1: Password Generator
```
Tool Name: "Ultimate Password Generator"
Main Functionality: Generate secure, random passwords
Key Features: Length control, character type toggles, strength meter, passphrase option
Content Pages: Password security guide, common password mistakes, password manager comparison
Target Keywords: password generator, secure password, random password, strong password
```

### Example 2: Color Palette Generator
```
Tool Name: "Designer's Color Palette Generator"
Main Functionality: Generate harmonious color palettes
Key Features: Multiple harmony types, export formats, accessibility checker, favorites
Content Pages: Color theory basics, using color in design, accessibility guidelines
Target Keywords: color palette generator, color scheme, design colors, harmonious colors
```

### Example 3: JSON Formatter
```
Tool Name: "JSON Formatter & Validator"
Main Functionality: Format, validate, and minify JSON
Key Features: Syntax highlighting, error detection, minify/beautify, tree view
Content Pages: JSON tutorial, common JSON errors, JSON vs XML, API testing guide
Target Keywords: json formatter, json validator, format json, json beautifier
```

### Example 4: Markdown Editor
```
Tool Name: "Live Markdown Editor & Previewer"
Main Functionality: Real-time markdown editing and preview
Key Features: Live preview, export HTML, syntax guide, templates
Content Pages: Markdown syntax guide, markdown vs rich text, documentation writing tips
Target Keywords: markdown editor, markdown preview, markdown to html, online markdown
```

### Example 5: Unit Converter
```
Tool Name: "Universal Unit Converter"
Main Functionality: Convert between various units
Key Features: Length, weight, temperature, currency, speed, area, volume
Content Pages: Metric vs imperial, conversion formulas, unit history, scientific units
Target Keywords: unit converter, convert units, metric conversion, measurement converter
```

---

## 🚀 Quick Start Instructions

1. **Copy this entire template**
2. **Fill in the bracketed placeholders** with your specific tool details
3. **Paste the customized prompt** to Claude in a new conversation
4. **Use pnpm** for all package management
5. **Deploy to Cloudflare Pages** via GitHub
6. **Submit sitemap** to search engines after launch

---

## 💡 Success Formula

```
Great Tool Algorithm + Modern UI + Excellent SEO + Strategic Ads = Passive Income
```

**Expected Timeline**: 1-2 weeks from prompt to deployed site
**Expected Monthly Revenue**: $400-$2,000 at 10K-50K monthly visitors
**Required Investment**: $0 (free hosting, free tools)
**Maintenance**: Minimal (static site, no backend)

---

## 📊 Revenue Projection Model

```
Monthly Visitors × Average Pages per Visit × RPM × Ad Placements = Monthly Revenue

Example:
10,000 visitors × 2.5 pages × $5 RPM × 3.5 ads = $437/month
50,000 visitors × 2.5 pages × $5 RPM × 3.5 ads = $2,187/month
```

**Variables**:
- RPM (Revenue per 1000 impressions): $3-7 typical for utility tools
- Pages per visit: 2-3 for good content
- Ad placements: 3-4 strategic spots (not all visible at once)

---

## ✅ Quality Checklist

**Before Deployment**:
- [ ] Tool works perfectly in all browsers
- [ ] Mobile responsive (test on real devices)
- [ ] Dark mode works correctly
- [ ] All keyboard shortcuts function
- [ ] Copy to clipboard has visual feedback
- [ ] No console errors or warnings
- [ ] Build succeeds without errors
- [ ] TypeScript strict mode passes
- [ ] Lighthouse score > 95

**After Deployment**:
- [ ] All pages load correctly
- [ ] Sitemap is accessible
- [ ] robots.txt is correct
- [ ] OG image shows in social media previews
- [ ] Analytics tracking works
- [ ] Ad placeholders don't cause layout shift
- [ ] SSL certificate active
- [ ] Domain configured correctly

---

## 🎨 Design Principles

1. **Simplicity**: User should understand tool immediately
2. **Speed**: Load in < 2 seconds, instant interaction feedback
3. **Clarity**: No confusing options, clear labels
4. **Accessibility**: High contrast, keyboard navigation, screen reader friendly
5. **Professionalism**: Looks trustworthy, not spammy despite ads
6. **Mobile-first**: Most users will be on mobile

---

## 🔑 Key Success Factors

1. **Better Tool**: Must genuinely be better than competitors
2. **Great SEO**: Rich content, proper structure, fast loading
3. **Strategic Ads**: High viewability without hurting UX
4. **Quality Content**: 1500+ words per major content page
5. **Backlinks**: Reach out to bloggers, list in directories
6. **Performance**: Fast load times keep users happy and boost rankings
7. **Regular Updates**: Keep content fresh, update copyright year

---

**Use this template for**: Generators, converters, formatters, calculators, validators, visualizers, analyzers, and any web-based utility tool.

**Best niches**: Developer tools, design tools, content creation, productivity, education, business utilities.

**Avoid**: Highly competitive keywords without differentiation, tools that need frequent updates, anything requiring authentication/database.

---
