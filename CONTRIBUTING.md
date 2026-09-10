# Contributing to Design-Systems

First off, thank you for considering contributing to **Design-Systems**! 🎉 

This project aims to be the most comprehensive, accessible, and high-fidelity collection of production-grade design systems on the web. Every design system is built with pure, modern web standards—semantic **HTML5**, **CSS3 custom properties (design tokens)**, and lightweight vanilla JavaScript—requiring zero compilation steps or external runtime dependencies.

Whether you're fixing a bug, adding a new design system, refining documentation, or polishing CSS tokens, we welcome your contributions.

---

## 📑 Table of Contents

- [Code of Conduct](#-code-of-conduct)
- [How to Contribute](#-how-to-contribute)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Enhancements](#suggesting-enhancements)
  - [Contributing Code or Design Systems](#contributing-code-or-design-systems)
- [Design System Standards & Architecture](#-design-system-standards--architecture)
  - [Directory Structure](#directory-structure)
  - [DESIGN.md Guidelines](#designmd-guidelines)
  - [HTML Showcase Guidelines](#html-showcase-guidelines)
- [Code Style & Conventions](#-code-style--conventions)
- [Pull Request Process](#-pull-request-process)
- [Commit Message Guidelines](#-commit-message-guidelines)

---

## 📜 Code of Conduct

This project and everyone participating in it is governed by our [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. Please report any unacceptable behavior according to our reporting guidelines.

---

## 🚀 How to Contribute

### Reporting Bugs

Before creating a bug report, please check existing issues to ensure it hasn't already been reported.

When opening a bug report via [GitHub Issues](https://github.com/H0NEYP0T-466/Design-Systems/issues):
- Use the **Bug Report** issue template.
- Provide a clear, descriptive title.
- Detail the exact steps to reproduce the issue.
- Describe the expected vs. actual behavior.
- Specify browser, operating system, and viewport/device details.
- Include screenshots or screen recordings where applicable.

### Suggesting Enhancements

Feature requests and design system suggestions are highly valued!
- Use the **Feature Request** issue template on GitHub.
- Clearly describe the purpose, source inspiration (e.g., brand, aesthetic, application), and target visual characteristics.
- Include reference links, screenshots, or design tokens if proposing a new brand/system.

---

## 🎨 Contributing Code or Design Systems

### Forking and Setting Up Locally

1. **Fork** the repository on GitHub:
   ```bash
   # Navigate to your fork
   git clone https://github.com/<your-username>/Design-Systems.git
   cd Design-Systems
   ```

2. **Create a dedicated feature branch**:
   ```bash
   git checkout -b feature/add-new-design-system
   ```

3. **Preview locally** using any lightweight static HTTP server:
   ```bash
   # Using Python 3
   python3 -m http.server 8000

   # Or using Node.js
   npx serve .
   ```
   Open `http://localhost:8000` in your web browser.

---

## 🏛 Design System Standards & Architecture

Every design system in this repository resides in its own isolated folder named with `kebab-case` (e.g., `modern-minimal`, `linear-app`).

### Directory Structure

```text
Design-Systems/
├── <system-name>/
│   ├── DESIGN.md              # Complete design token specification & documentation
│   └── <system-name>.html     # Interactive standalone showcase & component library
```

### `DESIGN.md` Guidelines

The `DESIGN.md` file serves as the canonical token specification. It must include:
1. **Title & Category Header**:
   ```markdown
   # Design System Inspired by [Brand / Concept]

   > Category: [Category Name]
   > [One-line concise summary of aesthetic and core characteristics]
   ```
2. **Visual Theme & Atmosphere**: High-level creative direction, lighting, mood, materials, and philosophy.
3. **Color Palette & Roles**:
   - Primary, secondary, accent, and semantic colors (HEX/RGBA).
   - Surface colors, borders, and text contrasts (meeting WCAG AA contrast ratios).
4. **Typography & Hierarchy**:
   - Primary display and body font families (prefer Google Fonts or standard fallbacks).
   - Font scale (display, h1-h4, body, small, code) with sizes, weights, and letter-spacings.
5. **Elevation & Spacing**:
   - 4px or 8px baseline spacing scale.
   - Shadow/elevation hierarchy (whisper shadows, ambient glows, or flat borders).
6. **Component Specifications**:
   - Buttons (variants, hover/active states, border-radii).
   - Cards, inputs, navigation, badges, and modals.
7. **Do's and Don'ts**: Concrete implementation tips for developers and designers.

### HTML Showcase Guidelines

The `<system-name>.html` file must:
- Be a **standalone, self-contained HTML5** document.
- Define all design tokens inside the `:root` pseudo-class as CSS custom properties (`--color-*`, `--font-*`, `--space-*`, `--radius-*`, `--shadow-*`).
- Include Google Fonts or font CDN imports in the `<head>` if specific web fonts are required.
- Provide a rich, responsive, interactive showcase featuring:
  - Header & Brand Navigation
  - Hero Section demonstrating typography and primary CTA
  - Component Showcase (buttons, input forms, cards, badges, status indicators)
  - Color Swatches & Typography Specimen table or grid
  - Interactive elements (e.g., state toggles, modal triggers, or tab switchers) using lightweight vanilla JavaScript.
- Avoid bulky third-party JS frameworks or CSS libraries (No Bootstrap, Tailwind CDN, or React build step—keep it pure, portable, and blazing fast).

---

## 📐 Code Style & Conventions

- **HTML**:
  - Valid HTML5 with semantic tags (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`).
  - 2-space indentation.
  - Double quotes for HTML attributes (`class="btn btn-primary"`).
- **CSS**:
  - CSS Custom Properties for all colors, radii, shadows, and fonts.
  - Mobile-first or fully responsive layouts using Flexbox and CSS Grid.
  - Clear section comments grouping tokens, resets, layouts, components, and utilities.
- **JavaScript**:
  - Modern ES6+ vanilla JavaScript.
  - Zero console errors or unhandled exceptions.

---

## 🔄 Pull Request Process

1. **Keep PRs focused**: Each pull request should address a single feature, design system, or bug fix.
2. **Update Documentation**: If you add a new design system or update existing tokens, ensure both `DESIGN.md` and the root `README.md` are updated.
3. **Self-Review**: Verify your code against multiple screen sizes (mobile, tablet, desktop) and ensure dark/light modes render correctly.
4. **Link Related Issues**: In your pull request description, reference any related issue (e.g., `Closes #12`).
5. **Submit PR**: Open the pull request against the `master` branch using our [Pull Request Template](.github/pull_request_template.md).

---

## 💬 Commit Message Guidelines

We follow [Conventional Commits](https://www.conventionalcommits.org/):

- `feat: add vercel-inspired dark mode design system`
- `fix: resolve contrast ratio on button tokens in linear-app`
- `docs: update typography hierarchy in kraken/DESIGN.md`
- `style: format css custom properties in stripe showcase`
- `refactor: optimize component grid in bento design system`

Thank you for helping make the open-source web more beautiful! ✨
