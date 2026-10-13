# Publishing the GitHub profile README

## 1. Create the special profile repo
1. Go to https://github.com/new
2. Owner: **alexnieves-cs**. Repository name: **alexnieves-cs** (must match your username exactly).
3. Make it **Public**. Leave out the README, .gitignore, and license (this folder already has the files).
4. Click **Create repository**.

## 2. Push
From this folder (`/workspace/gh-profile` on Grok Bot's computer, or a copy on yours):

```bash
git remote add origin https://github.com/alexnieves-cs/alexnieves-cs.git
git push -u origin main
```

(If `origin` already exists, use `git remote set-url origin https://github.com/alexnieves-cs/alexnieves-cs.git` instead of `add`.)

The `preview_*.png` / `preview.html` files are local only (listed in `.gitignore`).

## 3. Turn on the snake animation
1. In the repo, go to **Settings → Actions → General → Workflow permissions** and choose **Read and write permissions**. Save.
2. Open the **Actions** tab. Enable workflows if asked.
3. Run **Generate snake animation** with **Run workflow**. It creates the `output` branch with `github-snake.svg` and `github-snake-dark.svg`.
4. After that, it runs every 12 hours and on every push to `main`.

## 4. Stats cards
github-readme-stats and streak-stats need no setup. Private repo names never appear. `count_private=true` only adds private commit counts on self-hosted instances. To count private contributions on the graph and snake, turn on **Private contributions** under Profile → Contribution settings.

## 5. Profile settings (github.com/settings/profile)
- **Name:** Alex Nieves
- **Bio** (147 chars):
  > CS + Finance @ Wake Forest · SWE @ Steward Technologies · GPS-denied drone nav, fintech & AI agent tooling · Seeking Summer 2027 SWE/AI internships
- **Company:** Steward Technologies · **Location:** your choice · **Social accounts:** LinkedIn
- Check **Available for hire** if you want recruiters to see it.

## 6. Pin repos
On your profile, **Customize your pins** and pin:
1. `terminal-canvas` (public)
2. Any other public repos. Private repos (denied-signal-stack) can't be pinned for visitors; the README covers them as "demo on request."
