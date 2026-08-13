# obsidian vault: doto zettelkasten

A Zettelkasten vault built around Bob Doto's *A System for Writing* (2024), using Kepano's base and categories pattern for the dashboards.

```
00 inbox      fleeting captures, processed weekly
05 sleeping   ideas that resist processing, checked every few months
07 journal    the daily journal: interstitial logging + end-of-day check-in
10 reference  reference notes, one long note per source
20 slip-box   main notes (the ideas) + hub notes, structure notes, keyword index
30 projects   writing projects, one subfolder per piece
40 archive    finished projects
50 templates  note formats
categories    category pages that back the Bases views
```

## Requirements

- Obsidian 1.9+ (Bases is a core plugin)
- Core plugins enabled: **Bases**, **Templates**, **Categories**

## Setup

1. Enable Templates (Settings → Core plugins) and set its template folder to `50 templates`.
2. Bases is on by default in 1.9+. No configuration needed.
3. Enable Categories (Settings → Core plugins) and point it at the `categories` folder.

## How it works

Each numbered folder starts with `00 guide.md`, its rulebook. Read the `00 guide.md` in a folder before working in it; the rules are specific per stage (e.g. inbox notes get processed weekly, main notes never get archived). The folder's `01 …base` file (and `02 related.base`, `03 views.base` in the slip-box) is its dashboard view.

**Category linking, not folders, is what most Bases filter on.** A note belongs to a stage because its frontmatter `categories` field links to a page in `categories/`, e.g. `categories: ["[[main]]"]`, not because of where the file sits. The exceptions are `01 queue.base` (inbox) and `01 sleep.base` (sleeping), which filter by folder, since captures there are meant to be format-free and often lack frontmatter entirely.

**Templates** (`50 templates/`) set the `categories` link automatically, so creating a note from the right template is what puts it on the right dashboard.

## The five steps (Doto)

1. **Capture** — fleeting notes land in `00 inbox`; reference notes in `10 reference`.
2. **Transform** — captures become main notes in `20 slip-box`.
3. **Connect** — link main notes, with context for each link.
4. **Track** — hub notes, structure notes, and the keyword index keep trains of thought findable.
5. **Write** — pull trains of thought into `30 projects`; finished work goes to `40 archive`.

## Folders

- `00 inbox` / `01 queue.base` — fleeting captures. Process weekly. Three fates: main note, sleeping, delete.
- `05 sleeping` / `01 sleep.base` — ideas passed over during processing. Check every few months.
- `07 journal` — the daily journal. Interstitial logging + end-of-day check-in. One file per year.
- `10 reference` / `01 library.base` — reference notes, one long note per source, brief citations with locators.
- `20 slip-box` / `01 main.base`, `02 related.base`, `03 views.base` — main notes (one idea + link), plus hub notes, structure notes, keyword index. Never archived.
- `30 projects` / `01 tracker.base`, `02 logs.base` — one subfolder per piece: project note, draft, creative log. References the slip-box, doesn't absorb it.
- `40 archive` — finished projects only. Not a home for main notes.

## Credits

Method: Bob Doto, *A System for Writing* (2024). Base and categories pattern: kepano (https://github.com/kepano/kepano-obsidian), adapted from the Ahrens vault (obsidian-vault).
