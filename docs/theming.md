# How the plugin looks, and project templates

The Oakfall plugin sits inside Obsidian and uses Obsidian's theme. It does not ship a look, a theme picker, or a theme format for others to build and sell. Looks (Moss, Autumn Harvest, Cupid's Roses, and the rest), Desk and Classic, Focus, and Gall's outfits live in the [Oakfall app](https://oakfall.app/). The plugin's job is the functions: the binder first, then the other modules, in the host's own chrome.

`--oak-` tokens still exist in `styles.css` so a panel can follow Obsidian's variables (`--background-primary`, `--text-normal`, and so on). They are an implementation detail of this repo, not a public theme API. Do not publish a "Oakfall theme" folder against them; it will not be loaded.

## A project template is a folder

A template is a starting project: the folders, the `_Project.md` with labels and statuses filled in, a few starter notes, and a compile preset if one belongs with it. Oakfall ships with novel, short fiction, poetry, essay, screenplay, and recipe collection, which are the shapes that came across from Scrivener. Anyone can add another by making a folder that follows the spec and adding `template.json`:

```json
{
  "name": "Sermon series",
  "author": "someone",
  "version": "1.0.0",
  "oakfall": 1,
  "description": "One project per series, one scene per sermon, scripture references as footnotes."
}
```

Templates install to `.oakfall/templates/`. Creating a project from one copies the folder, assigns fresh `id` values, and stamps the date. Nothing in a template is special after that; it is an ordinary project.

Templates are yours. Publish them on GitHub, sell them on your own site, or list them in a community gallery when it exists. They change starting content, never how Obsidian looks, and never what the spec stores after the copy.

## What this page used to be

Until 2026-10-17 this page specified a folder format (`theme.json`, `theme.css`) for restyling Oakfall's panels on top of Obsidian. That format is withdrawn. The desk is the app.
