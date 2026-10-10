# UI Context

## Theme

Use the official shadcn Radix Nova preset with neutral CSS variable tokens. The default is light; a `.dark` ancestor activates the generated dark tokens. This feature adds no theme switcher or theme persistence.

`app/globals.css` is the source of truth for the generated token values and radius scale. It imports Tailwind CSS, `tw-animate-css`, and `shadcn/tailwind.css`.

## Colors

| Role | CSS variables | Tailwind examples |
| --- | --- | --- |
| Page | `--background`, `--foreground` | `bg-background`, `text-foreground` |
| Cards | `--card`, `--card-foreground` | `bg-card`, `text-card-foreground` |
| Popovers and dialogs | `--popover`, `--popover-foreground` | `bg-popover`, `text-popover-foreground` |
| Primary actions | `--primary`, `--primary-foreground` | `bg-primary`, `text-primary-foreground` |
| Secondary actions | `--secondary`, `--secondary-foreground` | `bg-secondary`, `text-secondary-foreground` |
| Muted content | `--muted`, `--muted-foreground` | `bg-muted`, `text-muted-foreground` |
| Accent | `--accent`, `--accent-foreground` | `bg-accent`, `text-accent-foreground` |
| Destructive state | `--destructive` | `text-destructive` |
| Borders, inputs, focus | `--border`, `--input`, `--ring` | `border-border`, `border-input`, `ring-ring` |

Use semantic tokens for new application styling. Preserve the additional chart and sidebar tokens supplied by the official preset.

## Typography

| Role | Font | Tailwind token |
| --- | --- | --- |
| UI and headings | Existing Geist Sans from the root layout | `--font-sans` references `--font-geist-sans`; `--font-heading` references `--font-sans` |
| Code | Existing Geist Mono from the root layout | `--font-mono` references `--font-geist-mono` |

## Border Radius

The preset defines `--radius: 0.625rem` and derived `--radius-sm` through `--radius-4xl` tokens. Use the generated component defaults and Tailwind radius utilities.

## Component Library

- Installed components: Button, Card, Dialog, Input, Tabs, Textarea, and ScrollArea.
- Import from `@/components/ui/<component>`; ScrollArea uses `scroll-area`.
- Use the official shadcn CLI to add components.
- Do not manually modify installed `components/ui/` source. Compose components in application code and customize through supported props and `className`.
- Application code can import `cn()` from `@/lib/utils`; it re-exports the official shadcn class-merging helper used by the generated components.

## Layout Patterns

The home page remains a centered Ghost AI div. Further product layouts are not specified in this feature.

## Icons

Use `lucide-react`. The generated Dialog uses its `XIcon`; component defaults provide icon sizing.
