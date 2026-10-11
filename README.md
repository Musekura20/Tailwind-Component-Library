# Tailwind Component Library

A small UI library with **buttons, cards and alerts**, made with Tailwind CSS utilities only.
Repeated class lists are extracted into reusable classes with `@apply` in `src/input.css`.

## Group members
- Ineza (individual submission)

## Components
| Type | Classes |
|------|---------|
| Buttons | `.btn-primary`, `.btn-secondary`, `.btn-outline` (hover, focus, disabled) |
| Cards | `.card`, `.card-body`, `.card-title`, `.card-text`, `.card-image` (profile card + product card) |
| Alerts | `.alert-success`, `.alert-warning`, `.alert-error`, `.alert-info` |

## Run it
```bash
npm install
npm run build     # creates dist/output.css
# then open index.html in the browser
npm run dev       # rebuilds CSS when you change files
```

## Trade-off note
Utility classes in HTML are fast to write and need no naming, but the same long class list gets repeated
on every button. Using `@apply` makes the HTML shorter and easier to change in one place, but we lose
some of Tailwind's main benefit (seeing all styles right in the markup) and we must invent and
maintain class names again. Our choice: use `@apply` only for things that repeat a lot (buttons,
cards, alerts) and keep one-off layout in plain utilities.
