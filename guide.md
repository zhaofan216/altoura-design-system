# Altoura Compact Design System

Use Inter typography, layered neutral surfaces, softer body text, blue primary actions, and restrained borders to give Altoura designs the same overall look.

## Use the foundations

Copy `foundations.css`, `fonts.css`, and the `files/` directory into your project. Preserve their relative paths, then load both stylesheets:

```html
<link rel="stylesheet" href="fonts.css">
<link rel="stylesheet" href="foundations.css">
```

```css
body {
  font-family: var(--font-sans);
  background: var(--surface-0);
  color: var(--text-default);
}
.panel {
  padding: 16px;
  border: 1px solid var(--border-default);
  border-radius: var(--radius-lg);
  background: var(--surface-1);
}
```

Add `.dark` to the document root to switch themes. These files supply CSS variables and self-hosted fonts; apply the variables in your own component styles.

## Color roles

| Purpose | CSS variables |
| --- | --- |
| Canvas, raised, nested, recessed surfaces | `--surface-0` through `--surface-3` |
| Headlines and section titles | `--foreground`, `--text-strong` |
| Body and supporting copy | `--text-default`, `--text-secondary` |
| Metadata, placeholders, disabled text | `--muted-foreground`, `--text-placeholder`, `--text-disabled` |
| Borders | `--border-subtle`, `--border-default`, `--border-strong` |
| Primary action and label | `--primary`, `--primary-foreground` |
| Selection background and text | `--primary-subtle`, `--primary-text` |
| Focus and logo blue | `--ring`, `--brand` |

Primary UI blue is #2D76D7. Logo blue is #3169B3. Use semantic variables in screens. The token JSON includes 82 shared variables for both themes plus the font and derived radii. It is a CSS-variable snapshot for handoff and scripts; create corresponding light/dark Figma variables when needed.

For success, warning, info, and destructive feedback, pair `--<status>-subtle` backgrounds with `--<status>-text` labels. Solid backgrounds use matching `--<status>-foreground` labels. Include a label or icon so meaning does not depend on color alone. Category accents identify content types; chart colors identify data series.

## Typography

Use Inter Variable with a sans-serif fallback. Regular copy uses weight 400, labels and card titles 500, section headings 600, and page headings 700.

| Existing context | Size and weight |
| --- | --- |
| Page / section heading in the token reference | 20px / 700; 18px / 600 |
| Dashboard card title | 14px / 500 |
| Supporting copy | 14px / 400 |
| Metadata | 12px / 400 |
| Default button label | 12px / 500 |
| Input | 14px; 12px at the desktop md breakpoint |

Preserve each component’s typography rather than imposing a global body-size rule on controls. Inter includes weights 100–900 and the same normal-style language subsets as the original system.

## Spacing and shape

Use the existing 4px rhythm: 4, 8, 12, 16, 24, and 32px. Typical cards use 16px padding, internal gaps 12px, and dashboard grid gaps 24px. These are layout conventions, not additional CSS tokens.

The base radius is 10px. Derived radii are 6px (sm), 8px (md), 10px (lg), and 14px (xl). Use full rounding for pills and subtle 1px borders for separation.

## Controls and states

Desktop buttons use a default 28px height, 12px medium text, and 8px radius; xs, sm, and lg heights are 20, 24, and 32px. Inputs use 34px height and 8px radius. Base cards use 10px radius with 16px padding and gaps. Dashboard cards use 368 × 168px desktop dimensions and 368 × 188px iPad dimensions.

Provide hover, focus, selected, disabled, loading, and invalid states. Keep focus visible, label icon-only controls accessibly, and use touch-appropriate variants on tablets. Lucide is the system’s icon family, usually 14–16px in desktop controls. The public foundations do not include a JavaScript component library.

## Updates and font license

This public repository is a snapshot exported from the maintained Altoura design system. Update the foundations, token JSON, fonts, and guide together. Every push to the main branch republishes the guide through GitHub Pages.

Inter is licensed under the SIL Open Font License in [INTER-LICENSE.txt](INTER-LICENSE.txt). That license applies to the font files; it does not grant rights to Altoura trademarks or other design assets.
