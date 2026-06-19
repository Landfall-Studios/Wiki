---
title: Contributing
description: How to add to the Landfall SMP Wiki
---

Thanks for helping document the world! The wiki is open to anyone. Adding a missing person, fixing a date, and expanding a location all start the same way: a pull request on the wiki's GitHub repo.

This guide assumes you've never used GitHub before. If you have, skim the [[#TL;DR (for the impatient)|TL;DR]] and skip to the conventions at the bottom.

## TL;DR (for the impatient)

1. Fork the [Wiki repo](https://github.com/Landfall-Studios/Wiki).
2. Edit or add a markdown file under `content/`.
3. Open a pull request against the `v5` branch.
4. Once merged, the site rebuilds and redeploys automatically.

## Where the content lives

Everything you can read here is generated from markdown files in the `content/` folder of the [Wiki repo](https://github.com/Landfall-Studios/Wiki). The folder structure mirrors the site:

```
content/
├── Epochs/        ← timeline arcs
├── Groups/        ← factions, guilds, crews
├── Locations/     ← places, by epoch
├── Major Events/  ← significant happenings
├── People/        ← characters
├── Procedures/    ← rules, mechanics, etc
└── index.md       ← the home page
```

To add to the wiki, you add or edit a `.md` file in the right folder.

## The quick path (GitHub web UI, no command line)

Best for fixing typos, adding a paragraph, or other small edits.

1. Sign in to GitHub and open the file you want to change. For example, `content/People/Some Character.md`.
2. Click the pencil icon (top right of the file view). GitHub will offer to fork the repo for you. Click **Fork this repository**.
3. Make your edits in the in-browser editor.
4. Scroll down to **Commit changes**. Write a short description (`Fix Lilaris dates`, `Add Red Diamond Casino history`). Choose **Create a new branch** and click **Propose changes**.
5. On the next screen, click **Create pull request**. Fill in what you changed and why, then submit.

That's it. A maintainer will review, and once it's merged your edit goes live within a couple of minutes.

## The full path (local clone, for bigger changes)

Best for adding multiple pages, uploading images, or anything you want to preview locally before submitting.

### 1. Fork and clone

1. Click **Fork** at the top right of the [Wiki repo](https://github.com/Landfall-Studios/Wiki).
2. Clone your fork:

   ```bash
   git clone https://github.com/YOUR-USERNAME/Wiki.git
   cd Wiki
   ```

3. Add the upstream repo so you can pull in others' changes later:

   ```bash
   git remote add upstream https://github.com/Landfall-Studios/Wiki.git
   ```

### 2. Make a branch

Keep your work isolated from `v5` so you can have multiple PRs in flight:

```bash
git checkout v5
git pull upstream v5
git checkout -b add-new-faction
```

Branch names are casual. `add-new-faction`, `fix-timeline-dates`, `casino-rework` all work.

### 3. Edit content

Open `content/` in your editor of choice. [Obsidian](https://obsidian.md/) works particularly well since the wiki uses Obsidian-flavored markdown (wikilinks, callouts, embeds, see the conventions section below).

Add new `.md` files where they belong. Put images under `content/Media/Images/` with subfolders mirroring the content structure.

### 4. (Optional) Preview locally

If you want to see your changes before submitting:

```bash
npm install
npx quartz build --serve
```

Then open <http://localhost:8080>. The site rebuilds on file changes.

### 5. Commit and push

```bash
git add content/
git commit -m "Add the Ehrengard Empire"
git push origin add-new-faction
```

### 6. Open the pull request

GitHub will print a URL after the push. Open it, click **Create pull request**, target `v5`, and describe your change. Submit.

## What happens after merge

When a maintainer merges your PR into `v5`:

1. The `Deploy Quartz site to GitHub Pages` workflow fires automatically.
2. It installs dependencies, runs `npx quartz build`, and uploads the resulting `public/` folder to GitHub Pages.
3. A few minutes later, your changes are live on this site.

You don't need to do anything to trigger this, it runs on every push to `v5`.

## Conventions

### Frontmatter

Every page should start with frontmatter (YAML between `---` lines) so the site renders nice titles, descriptions, and link previews:

```markdown
---
title: Red Diamond Casino
description: A neon-soaked gambling hall on the eastern wharf.
tags:
  - location
  - 530
---
```

`title` is what appears in browser tabs and link previews. `description` shows in social previews and search results. `tags` group pages and multiple are fine so long as they follow established convention. Note that old pages do not have the required frontmatter yet.

### Wikilinks

Link between pages with `[[Page Name]]` (matches the filename, ignoring `.md` and folder path). Add a custom display label with `[[Page Name|what readers see]]`:

```markdown
The Casino is run by [[Larrism]], whose origins trace back to [[Landfall-530 - Noble Blood|the Noble Blood epoch]].
```

### Images

Embed with `![[image-name.png]]` (Obsidian style) or `![alt text](path/to/image.png)` (standard markdown). Put images in `content/Media/Images/<category>/`.

### Callouts

Highlight notes, warnings, lore quotes, etc:

```markdown
> [!warning] Sensitive Content
> This page contains sensitive content.
```

Supported types: `note`, `info`, `tip`, `warning`, `danger`, `quote`, `example`, and more.

### Sensitive content

Pages dealing with heavy themes should link to or be linked from [[Themes and Discretion|Themes & Discretion]] so readers can navigate them with context.

## Asking for help

Stuck? Not sure where a page belongs, or whether something fits the canon? Open a draft PR or a GitHub issue and tag a maintainer. It's better to ask than to guess.

Welcome aboard, and thanks for adding to the canon.
