# Ziki agents page redesign

Task 1 of the HNG15 individual task: a reworked version of [`ziki.dev/settings/agents`](https://ziki.dev/settings/agents) that improves how humans and agents interact in Ziki.

## What changed

The live Ziki page buries a full paragraph of rules above the list, repeats the role
explanation twice (`My agents` vs `Your agents` vs `LEVELS`), and crams six controls
into every agent card. This rebuild keeps Ziki's design system and reworks the
hierarchy:

- **Clear type hierarchy** — page title (24) → section title (16.5) → card title (14.5),
  with small uppercase eyebrow labels doing the grouping instead of big headings.
- **Shorter copy** — the 80-word wall of text became a one-line subtitle plus a
  "What each role can do" reference section with one line per role.
- **Calmer cards** — key + copy, level select and a `⋯` overflow menu (project,
  regenerate, revoke, delete) instead of six always-visible buttons.
- **Working interactions** — search, role filter tabs, copy-key with feedback,
  confirm dialogs for destructive actions, create-agent flow, toasts.
- **Responsive** — hamburger nav below 960px, single-column cards below 780px,
  no horizontal overflow at 390px.
- **Light and dark** — uses Ziki's own `--zk-*` tokens (`#f5f7fc` / `#070f22`,
  Inter), with a toggle that persists.

## Run it

Open `index.html`, or serve the folder:

```sh
npx serve .
```

## Notes

Static HTML, no build step, no dependencies. Sample data only, no live keys.