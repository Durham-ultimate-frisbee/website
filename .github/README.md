# Durham University Ultimate Frisbee Club — website

**English** | [中文](README.zh-CN.md)

Live site: **https://durham-ultimate-frisbee.github.io/website/**

The official website of Durham University Ultimate Frisbee Club (DUF), looked after by club members.

## What this is

- **Pages:** home (with training times), about, people, honours, news and contact.
- **Everything you see on the site lives in [`content/`](../content/)** as simple text files — you never need to touch the code.
- **Safe to edit:** if something is filled in wrongly, the site isn't updated and you get a plain-English message saying exactly what to fix. The live site always stays on the last working version.
- **Free and private:** plain web pages on GitHub Pages — no server, logins, tracking or cookies. Hidden location data in photos is removed automatically.

## Who looks after it

| Role | Who | Looks after |
|---|---|---|
| **Website maintainers** | Club members with access to this repository | The content: people, honours, news, training times, photos |
| **Technical owner** | Tao ([@alvinz26](https://github.com/alvinz26)), who built the site | The code and design. Any change outside `content/` needs his approval |

**New maintainer?** Ask a club admin to add you to this repository with the **Write** role.
When you hand over at the end of your time in the club, add your successor the same way.

## Editing the content

| File | What it controls |
|---|---|
| [`content/site.yaml`](../content/site.yaml) | Club name, colours, logo, social links, the banner at the top, honours filters |
| [`content/people.yaml`](../content/people.yaml) | Exec, captains and coaches — one block per person per season |
| [`content/honours.yaml`](../content/honours.yaml) | Results: season, competition, team, medal, and squad list if you have it |
| [`content/news/`](../content/news/) | News — one file per post |
| [`content/pages/join.md`](../content/pages/join.md) | The home-page "New to ultimate?" section, including the training timetable |
| [`content/pages/about.md`](../content/pages/about.md) | The About page |
| [`content/images/`](../content/images/) | Logo, photos and news covers |

**How to make a change** (on the GitHub website, nothing to install):

1. Open the file and click ✏️ **Edit**.
2. Make your change, then **Commit changes…** → keep **Create a new branch and start a pull request** → **Propose changes** → **Create pull request**.
3. Wait for the automatic check to show a **green ✓** (a few minutes), then click **Squash and merge**.

Changes inside `content/` don't need anyone's approval. Every field is explained in
[docs/data-model.md](../docs/data-model.md), and there is a step-by-step guide in Chinese in
[docs/content-guide.md](../docs/content-guide.md).

## Every new season

- [ ] **Exec:** add the new exec to `content/people.yaml` with the new season (e.g. `2027/28`). Keep last year's entries — the People page shows only the newest season.
- [ ] **Training:** update the timetable in `content/pages/join.md`.
- [ ] **Honours:** add results after each tournament to `content/honours.yaml` (squad lists make the player leaderboard work).
- [ ] **News:** post trials, taster sessions, results and socials in `content/news/`.
- [ ] **Banner:** update or remove `notice:` in `content/site.yaml`.

## Photos

- Only use photos that **everyone pictured is happy to have online**, and that the **photographer has agreed** to.
- Upload them to the right folder in `content/images/` (e.g. `content/images/people/`) and write the path in the file, e.g. `photo: images/people/alex-smith.jpg`.
- JPG, up to about 2000 px wide. Location and camera details are removed automatically when the site is published.

## How long until changes appear

Usually **a few minutes** after a change is merged. The **Actions** tab shows progress: yellow = publishing,
green ✓ = live (refresh the page), red ✗ = something needs fixing.

## When something goes wrong

- A red ✗ means the content check found a problem — **the live site is unaffected**.
- Click the red ✗ → **Details**, and find the block starting with `Content check failed`. It names the file, the entry, the field and what to change:

  ```
  content/people.yaml → 2027/28 · Alex Smith (line 12)
    • role — is required but missing.
  ```

- Fix it and save again. Every past version is kept, so nothing can be lost.
- Stuck, or need a new feature? Open an issue in this repository and mention **@alvinz26**.

## Credits

Website designed and built by **Tao** ([@alvinz26](https://github.com/alvinz26)), based on his open-source
[team-site-template](https://github.com/alvinz26/team-site-template) ([MIT licence](../LICENSE)).
Please keep the "Website by Tao" credit in the footer.
