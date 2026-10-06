# Altoura Design System

Compact design foundations for a consistent Altoura look: 82 shared tokens in light and dark themes, self-hosted Inter fonts, typography, spacing, radii, and core control guidelines.

**[Open the visual guide](https://zhaofan216.github.io/altoura-design-system/)** · **[Read the team guide](guide.md)**

## Use in your project

Download this repository and copy `foundations.css`, `fonts.css`, and `files/` into your app or prototype. Load the two CSS files, then use variables such as `var(--surface-0)`, `var(--text-default)`, and `var(--font-sans)`. Add `.dark` to the document root for dark mode.

For a local preview, open `index.html` in a browser. The guide includes CSS and JSON downloads and click-to-copy swatches. Clipboard support may vary for local file URLs; the swatch displays the token if copying is unavailable.

## Contents

- `index.html` — visual reference with a theme toggle.
- `guide.md` — compact styling and usage rules.
- `foundations.css` — plain CSS custom properties for both themes.
- `tokens.json` — CSS-variable snapshot for handoff and scripts.
- `fonts.css` and `files/` — self-hosted Inter Variable with language subsets.
- `INTER-LICENSE.txt` — font license.

The public repository contains shared foundations and visual guidance. Interactive component behavior belongs in the consuming app. Updates are exported from the maintained Altoura system; update these files together to keep the public snapshot consistent.

## Publish the guide

The GitHub Actions workflow deploys these static files to GitHub Pages on pushes to `main`. Repository Settings → Pages should use **GitHub Actions** as the build source. No package installation, build step, or private registry is required.

Inter’s SIL Open Font License applies to the fonts. Altoura trademarks and other design assets are not covered by that font license.
