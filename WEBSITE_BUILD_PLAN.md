# Website Build Plan: Security Consulting Income Guide

## Executive Summary

Build a professional knowledge base website from 470 markdown files with monetization capabilities.

---

## Option Comparison

| Option              | Build Time | Cost      | Monetization  | Best For            |
| ------------------- | ---------- | --------- | ------------- | ------------------- |
| **MkDocs Material** | 2-4 hours  | Free      | Gumroad embed | Simple, fast launch |
| **Docusaurus**      | 4-8 hours  | Free      | Full custom   | React ecosystem     |
| **Hugo + Docsy**    | 4-6 hours  | Free      | Custom        | Speed, SEO          |
| **Nextra**          | 3-5 hours  | Free      | Easy          | Next.js/Vercel      |
| **GitBook**         | 1-2 hours  | $0-$99/mo | Built-in      | Easiest, paid tiers |

---

## Recommended: MkDocs Material Theme

**Why MkDocs Material:**

- Perfect for markdown documentation
- Beautiful, professional design out of the box
- Built-in search
- Easy monetization integration
- Works with GitHub Pages (already enabled)
- 470 files = no problem

---

## Implementation Plan

### Phase 1: Setup (30 minutes)

```bash
# Install MkDocs and Material theme
pip install mkdocs mkdocs-material mkdocs-awesome-pages-plugin

# Initialize in your repo
cd /home/aadel/projects/security-consulting-income-guide
mkdocs new .
```

### Phase 2: Configuration

Create `mkdocs.yml`:

```yaml
site_name: Security Consulting Income Guide
site_url: https://ahmed-adelb.github.io/security-consulting-income-guide/
site_description: The most comprehensive guide to building a $50K-$100K/month cybersecurity consulting practice

theme:
  name: material
  palette:
    - scheme: slate
      primary: deep purple
      accent: amber
      toggle:
        icon: material/brightness-4
        name: Switch to light mode
    - scheme: default
      primary: deep purple
      accent: amber
      toggle:
        icon: material/brightness-7
        name: Switch to dark mode
  features:
    - navigation.instant
    - navigation.tracking
    - navigation.tabs
    - navigation.sections
    - navigation.expand
    - navigation.top
    - search.suggest
    - search.highlight
    - content.tabs.link
    - content.code.copy
  icon:
    repo: fontawesome/brands/github

repo_url: https://github.com/Ahmed-AdelB/security-consulting-income-guide
repo_name: Ahmed-AdelB/security-consulting-income-guide

plugins:
  - search
  - awesome-pages

extra:
  social:
    - icon: fontawesome/brands/github
      link: https://github.com/Ahmed-AdelB
    - icon: fontawesome/brands/linkedin
      link: https://linkedin.com/in/yourprofile
  analytics:
    provider: google
    property: G-XXXXXXXXXX

nav:
  - Home: index.md
  - Platforms:
      - Expert Networks: 01-platforms/expert-networks/
      - Bug Bounty: 01-platforms/bug-bounty/
      - vCISO: 01-platforms/vciso/
      - Expert Witness: 01-platforms/expert-witness/
      - Web3 Audit: 01-platforms/web3-audit/
  - Domains: 02-domains/
  - Industries: 03-industries/
  - Income Streams: 04-income-streams/
  - Getting Started: 05-getting-started/
  - Market Research:
      - Salary Benchmarks: 06-market-research/salary-benchmarks/
      - Platform Reviews: 06-market-research/platform-reviews/
      - Community Insights: 06-market-research/community-insights/
      - Rate Guides: 06-market-research/rate-guides/
  - Raw Data: 07-raw-data/

markdown_extensions:
  - pymdownx.highlight:
      anchor_linenums: true
  - pymdownx.superfences
  - pymdownx.tabbed:
      alternate_style: true
  - admonition
  - pymdownx.details
  - attr_list
  - md_in_html
  - tables
  - toc:
      permalink: true

extra_css:
  - stylesheets/extra.css
```

### Phase 3: Directory Structure

```
security-consulting-income-guide/
├── docs/                    # MkDocs expects content here
│   ├── index.md            # Homepage
│   ├── 01-platforms/       # Move content here
│   ├── 02-domains/
│   ├── 03-industries/
│   ├── 04-income-streams/
│   ├── 05-getting-started/
│   ├── 06-market-research/
│   ├── 07-raw-data/
│   └── stylesheets/
│       └── extra.css       # Custom styles
├── mkdocs.yml
└── README.md
```

### Phase 4: Monetization Integration

#### 4.1 Gumroad Embed (in docs/index.md or dedicated page)

```html
<!-- Gumroad Product Embed -->
<div class="gumroad-product-embed">
  <a href="https://yourusername.gumroad.com/l/security-playbook">
    <img src="assets/ebook-cover.png" alt="Security Consulting Playbook" />
  </a>
  <script src="https://gumroad.com/js/gumroad.js"></script>
  <a
    class="gumroad-button"
    href="https://yourusername.gumroad.com/l/security-playbook"
  >
    Get the Premium Playbook - $29
  </a>
</div>
```

#### 4.2 Email Capture (ConvertKit)

```html
<!-- ConvertKit Form Embed -->
<script
  async
  data-uid="YOUR_FORM_ID"
  src="https://your-account.ck.page/YOUR_FORM_ID/index.js"
></script>
```

#### 4.3 GitHub Sponsors Button

Already configured via `.github/FUNDING.yml`

### Phase 5: Custom Styling

Create `docs/stylesheets/extra.css`:

```css
/* Monetization callout boxes */
.md-typeset .admonition.premium {
  border-color: #ffd700;
}

.md-typeset .admonition.premium > .admonition-title {
  background-color: rgba(255, 215, 0, 0.1);
}

/* CTA buttons */
.cta-button {
  display: inline-block;
  padding: 12px 24px;
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white !important;
  border-radius: 8px;
  text-decoration: none;
  font-weight: bold;
  margin: 10px 0;
}

.cta-button:hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(102, 126, 234, 0.4);
}

/* Premium content teaser */
.premium-teaser {
  background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
  border: 1px solid #ffd700;
  border-radius: 8px;
  padding: 20px;
  margin: 20px 0;
}
```

### Phase 6: Build & Deploy

```bash
# Build the site locally
mkdocs build

# Preview locally
mkdocs serve

# Deploy to GitHub Pages
mkdocs gh-deploy
```

### Phase 7: GitHub Actions (Auto-deploy)

Create `.github/workflows/deploy.yml`:

```yaml
name: Deploy MkDocs

on:
  push:
    branches:
      - master

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - name: Setup Python
        uses: actions/setup-python@v5
        with:
          python-version: "3.x"

      - name: Install dependencies
        run: |
          pip install mkdocs-material mkdocs-awesome-pages-plugin

      - name: Deploy
        run: mkdocs gh-deploy --force
```

---

## Alternative: Docusaurus (If you want React)

### Setup

```bash
npx create-docusaurus@latest website classic
cd website
```

### Benefits

- MDX support (React components in Markdown)
- Built-in versioning
- i18n ready
- Algolia DocSearch integration

### Drawbacks

- Heavier (Node.js ecosystem)
- More complex configuration
- Slower builds for 470 files

---

## Alternative: Hugo + Docsy Theme

### Setup

```bash
hugo new site website
cd website
git submodule add https://github.com/google/docsy.git themes/docsy
```

### Benefits

- Fastest build times (<1 second for 470 files)
- Best SEO out of the box
- Very flexible

### Drawbacks

- Go templating learning curve
- Theme customization complex

---

## Monetization Strategy Integration

### Free Tier (GitHub/Website)

- All 470 guides freely accessible
- Build audience and trust
- SEO traffic generation

### Paid Products

| Product        | Platform          | Price       | Integration  |
| -------------- | ----------------- | ----------- | ------------ |
| eBook PDF      | Gumroad           | $29-$49     | Embed button |
| Templates Pack | Gumroad           | $19         | Embed button |
| Newsletter     | ConvertKit        | Free/$10/mo | Popup/embed  |
| Coaching       | Calendly + Stripe | $250/hr     | Link         |
| Course         | Teachable/Gumroad | $297        | Link         |

### Conversion Funnel

```
Free Content (Website)
        ↓
Email Capture (Newsletter)
        ↓
Low-ticket ($29 eBook)
        ↓
Mid-ticket ($297 Course)
        ↓
High-ticket ($250/hr Coaching)
```

---

## SEO Optimization

### Meta Tags (in mkdocs.yml)

```yaml
extra:
  meta:
    - name: keywords
      content: cybersecurity consulting, security income, vciso, bug bounty, expert networks
    - name: author
      content: Security Consulting Income Guide
    - property: og:type
      content: website
    - property: og:image
      content: /assets/og-image.png
```

### Sitemap

MkDocs Material generates sitemap automatically.

### Google Analytics

```yaml
extra:
  analytics:
    provider: google
    property: G-XXXXXXXXXX
```

---

## Implementation Timeline

| Day | Task                                   |
| --- | -------------------------------------- |
| 1   | Install MkDocs, configure mkdocs.yml   |
| 1   | Reorganize files into docs/ directory  |
| 1   | Test local build                       |
| 2   | Add custom CSS and monetization embeds |
| 2   | Create landing page (index.md)         |
| 2   | Set up GitHub Actions                  |
| 3   | Deploy to GitHub Pages                 |
| 3   | Set up Google Analytics                |
| 3   | Create Gumroad product                 |
| 4   | Set up ConvertKit email capture        |
| 4   | Test all integrations                  |
| 5   | Announce on LinkedIn/Reddit/HN         |

---

## Commands Quick Reference

```bash
# Install
pip install mkdocs-material mkdocs-awesome-pages-plugin

# Serve locally (live reload)
mkdocs serve

# Build static site
mkdocs build

# Deploy to GitHub Pages
mkdocs gh-deploy

# Check for broken links
pip install mkdocs-linkcheck
mkdocs build --strict
```

---

## Next Steps

1. [ ] Run setup commands
2. [ ] Move content to docs/ directory
3. [ ] Create mkdocs.yml configuration
4. [ ] Build and test locally
5. [ ] Deploy to GitHub Pages
6. [ ] Add monetization embeds
7. [ ] Launch announcements

---

## Resources

- [MkDocs Material Documentation](https://squidfunk.github.io/mkdocs-material/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)
- [Gumroad Embed Guide](https://help.gumroad.com/article/44-embedding-gumroad)
- [ConvertKit Forms](https://help.convertkit.com/en/articles/2502494-creating-a-form)
- [Pageclip for Forms](https://github.com/marketplace/pageclip)
