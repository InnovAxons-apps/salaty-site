# salaty-site

Public website and privacy policy for the **Salaty** mobile app (`com.innovaxons.salaty`), hosted on GitHub Pages at [https://salaty.innovaxons.com](https://salaty.innovaxons.com).

## 1. Hosting Architecture

- **Hosting Platform**: GitHub Pages served from the `main` branch of this public repository (`InnovAxons-apps/salaty-site`).
- **Domain & DNS**: `salaty.innovaxons.com` configured via custom domain file `CNAME`.
- **Cloudflare DNS**: CNAME record pointing `salaty` to `innovaxons-apps.github.io` with proxy disabled (**DNS only**, Grey cloud) so GitHub Pages manages SSL/TLS certificates and HTTPS enforcement directly.
- **HTTPS**: Enforced via GitHub Pages settings.
- **Publishing Workflow**: Simply edit, commit, and push to `main`. GitHub Pages deploys updates automatically within minutes.

## 2. Site Structure

The site consists of 13 static HTML files across 6 languages (the same languages supported by the Salaty mobile app):

| Language | Code | Direction | Landing Page | Privacy Policy |
| :--- | :--- | :--- | :--- | :--- |
| **English** (Default) | `en` | LTR | `/` (`index.html`) | `/privacy/` (`privacy/index.html`) |
| **Arabic** (العربية) | `ar` | RTL | `/ar/` (`ar/index.html`) | `/ar/privacy/` (`ar/privacy/index.html`) |
| **Indonesian** (Bahasa Indonesia) | `id` | LTR | `/id/` (`id/index.html`) | `/id/privacy/` (`id/privacy/index.html`) |
| **Urdu** (اردو) | `ur` | RTL | `/ur/` (`ur/index.html`) | `/ur/privacy/` (`ur/privacy/index.html`) |
| **Turkish** (Türkçe) | `tr` | LTR | `/tr/` (`tr/index.html`) | `/tr/privacy/` (`tr/privacy/index.html`) |
| **French** (Français) | `fr` | LTR | `/fr/` (`fr/index.html`) | `/fr/privacy/` (`fr/privacy/index.html`) |
| **Not Found** | — | — | `404.html` | — |

## 3. Privacy & Offline Design Principles

Strictly mirrors the 100% offline, privacy-first architecture of the Salaty application:
- **Zero Telemetry & Tracking**: No Google Analytics, no Meta Pixel, no trackers, and no third-party scripts.
- **Zero Cookies**: No session or tracking cookies; no cookie banners required.
- **Zero External CDNs or Fonts**: All typography uses local system font stacks. Zero external network requests to third parties.
- **No Automatic Redirects**: Language selection is explicit via the top navigation switcher, preserving user autonomy and preventing unexpected redirect hops.
- **Canonical & Hreflang**: Complete bidirectional alternate links declared across all 12 content pages.

## 4. Styling & RTL Support

- **Single Shared Stylesheet**: `style.css` provides responsive, accessible styling across all pages.
- **CSS Logical Properties**: Layout padding, margins, borders, and text alignments use logical properties (`margin-inline-start`, `text-align: start`, etc.) to automatically mirror for RTL.
- **Bi-Directional Typography**: Pages in Arabic (`ar`) and Urdu (`ur`) set `dir="rtl"` with customized line-height multipliers for Nastaliq and Arabic script clearance.
- **Accessibility & Mobile-First**: Responsive down to 360 px width without horizontal scroll (wide data tables scroll internally within containers). Skip-to-content links and high-contrast color palettes (WCAG AA).

## 5. Source of Truth

The English privacy policy file in the primary application repository is the **absolute source of truth**:
- **Location**: `docs/site/privacy.md` in `InnovAxons/Salaty`
- Any change to permissions, SDK usage, or policy disclosures must be authored and approved in `docs/site/privacy.md` first.
- The 5 translated privacy pages (`ar`, `id`, `ur`, `tr`, `fr`) and the English static page (`privacy/index.html`) in this repository strictly mirror that document.
- Contact for support and policy inquiries: `innovaxons.apps@gmail.com`.
