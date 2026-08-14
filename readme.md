# Doto Zettelkasten Vault (Kepano layer)

A Zettelkasten vault built around Bob Doto's *A System for Writing* (2024), using Kepano's base and categories pattern for the dashboards. Eight folders, ten templates, eleven category pages.

## How it works

Each numbered folder starts with `00 guide.md`, its rulebook. Read the `00 guide.md` in a folder before working in it; the rules are specific per stage (e.g. inbox notes get processed weekly, main notes never get archived). The folder's `01 …base` file (and `02 related.base`, `03 views.base` in the slip-box) is its dashboard view.

**Category linking, not folders, is what most Bases filter on.** A note belongs to a stage because its frontmatter `categories` field links to a page in `categories/`, e.g. `categories: ["[[main]]"]`, not because of where the file sits. The exceptions are `01 queue.base` (inbox) and `01 sleep.base` (sleeping), which filter by folder, since captures there are meant to be format-free and often lack frontmatter entirely.

**Templates** (`50 templates/`) set the `categories` link automatically, so creating a note from the right template is what puts it on the right dashboard.

## The five steps (Doto)

1. **Capture** - fleeting notes land in `00 inbox`; reference notes in `10 reference`.
2. **Transform** - captures become main notes in `20 slip-box`, each with a folgezettel `id`.
3. **Connect** - link main notes, with context for each link.
4. **Track** - hub notes, structure notes, and the keyword index keep trains of thought findable.
5. **Write** - pull trains of thought into `30 projects`; finished work goes to `40 archive`.

## Folders

- `00 inbox` / `01 queue.base` - fleeting captures. Process weekly. Three fates: main note, sleeping, delete.
- `05 sleeping` / `01 sleep.base` - ideas passed over during processing. Check every few months.
- `07 journal` - the daily journal. Interstitial logging + end-of-day check-in. One file per year.
- `10 reference` / `01 library.base` - reference notes, one long note per source, brief citations with locators.
- `20 slip-box` / `01 main.base`, `02 related.base`, `03 views.base` - main notes (one idea + link), plus hub notes, structure notes, keyword index. Never archived.
- `30 projects` / `01 tracker.base`, `02 logs.base` - one subfolder per piece: project note, draft, creative log. References the slip-box, doesn't absorb it.
- `40 archive` - finished projects only. Not a home for main notes.
- `50 templates` - ten templates matching the note types.

## Requirements and setup

- Obsidian 1.9+ (Bases is a core plugin)
- Core plugins enabled: **Bases**, **Templates**, **Categories**

1. Enable Templates (Settings → Core plugins) and set its template folder to `50 templates`.
2. Bases is on by default in 1.9+. No configuration needed.
3. Enable Categories (Settings → Core plugins) and point it at the `categories` folder.

## The book

**Bob Doto, *A System for Writing: How an Unconventional Approach to Note-Making Can Help You Capture Ideas, Think Wildly, and Write Constantly* (2024).** A writing-first Zettelkasten: fleeting notes capture, reference notes keep one long note per source, main notes carry single ideas under folgezettel alphanumeric IDs, hub notes and the keyword index keep trains of thought findable, and the journal plus per-project creative logs drive actual writing. This vault is that system translated to Obsidian.

- Author's website: https://writing.bobdoto.computer/
- Get the book: [Amazon](https://www.amazon.com/dp/B0D18J83VB)

The book works through the whole method with examples; the vault gives you the structure, the book gives you the practice.

## Resources: Bob Doto in conversation

Podcast episodes featuring the author after the book's publication:

- **Focused** (Relay FM), Episode 209: "A System for Writing, with Bob Doto" (July 2024) - the book's system, creative workflows, and why the zettelkasten matters. https://podcasts.apple.com/us/podcast/a-system-for-writing-with-bob-doto/id1138055739?i=1000663855899
- **Aidan's Infinite Play**, Episode 45: "Bob Doto: A System For Writing: Capture Ideas, Think Wildly, Write Constantly" (September 2024) - capturing ideas, thinking wildly, writing without writer's block. https://www.listennotes.com/podcasts/aidans-infinite-play/e45-bob-doto-a-system-for-NF7kE9CPas-/
- **Exam Study Expert**, Episode 205: "A Hands-On Guide To Zettelkasten Notes: Practical Advice from Expert Bob Doto" (November 2025) - practical, hands-on zettelkasten implementation advice. https://examstudyexpert.com/bob-doto/

## Credits

Method: Bob Doto, *A System for Writing* (2024). Base and categories pattern: kepano (https://github.com/kepano/kepano-obsidian), adapted from the Ahrens vault (obsidian-vault). CC BY 4.0.

Prefer the plain method without dashboards? See the stock Doto version: https://github.com/rgtdnl/obsidian-doto-zettelkasten-stock-vault
