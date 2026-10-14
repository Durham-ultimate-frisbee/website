# Durham University Ultimate Frisbee Club — website

**English** | [中文](README.zh-CN.md)

Live site: **https://durham-ultimate-frisbee.github.io/website/**

## What this is

The website of Durham University Ultimate Frisbee Club (DUF): home page with training times, about,
people, honours, news and contact.

It is a static website built with [Astro](https://astro.build) and published free on GitHub Pages — no server,
logins, tracking or cookies. Everything you see on the site lives in the [`content/`](../content/) folder as
simple text files, so updating it never means touching the code. If something is filled in wrongly, the site
isn't updated and you get a plain-English message saying what to fix; the live site always stays on the last
working version.

Designed and developed by **Tao** ([@alvinz26](https://github.com/alvinz26)).

## What to update

| File | What it controls |
|---|---|
| [`content/people.yaml`](../content/people.yaml) | Exec, captains and coaches — one block per person per season (the site shows the newest season) |
| [`content/pages/join.md`](../content/pages/join.md) | The "New to ultimate?" section on the home page, including the training timetable |
| [`content/honours.yaml`](../content/honours.yaml) | Results: season, competition, team, medal, and the squad list if you have it |
| [`content/news/`](../content/news/) | News — one file per post |
| [`content/pages/about.md`](../content/pages/about.md) | The About page |
| [`content/site.yaml`](../content/site.yaml) | Club name, colours, logo, social links, the banner at the top |
| [`content/images/`](../content/images/) | Logo, photos and news covers |

**How to make a change** on the GitHub website:

1. Open the file and click ✏️ **Edit**.
2. **Commit changes…** → keep **Create a new branch and start a pull request** → **Propose changes** → **Create pull request**.
3. When the automatic check shows a **green ✓** (a few minutes), click **Squash and merge**. The site updates a few minutes later.

Every field is explained in [docs/data-model.md](../docs/data-model.md); there is a step-by-step guide in Chinese in
[docs/content-guide.md](../docs/content-guide.md).

## Photos

- Only use photos that **everyone pictured is happy to have online**, and that the **photographer has agreed** to.
- Upload them to the matching folder in `content/images/` and write the path in the file, e.g. `photo: images/people/alex-smith.jpg`.
- JPG, up to about 2000 px wide. Location and camera details are removed automatically when the site is published.

## When something goes wrong

- A red ✗ means the content check found a problem — the live site is unaffected.
- Click the red ✗ → **Details**, and find the block starting with `Content check failed`. It names the file, the entry, the field and what to change:

  ```
  content/people.yaml → 2027/28 · Alex Smith (line 12)
    • role — is required but missing.
  ```

- Fix it and save again. Every past version is kept, so nothing can be lost.
- Still stuck? Open an issue in this repository.

---

Built on [team-site-template](https://github.com/alvinz26/team-site-template) · [MIT licence](../LICENSE)
