# GRC Portfolio Starter Kit

Stop describing your work in a resume bullet. Start showing it. This kit turns your GRC projects into a real, live website — deployed automatically, every time you push a change.

## What you're getting

- A working portfolio site (MkDocs + Material theme) with pages already scaffolded for governance, risk, and compliance
- A GitHub Action that deploys your site automatically — no manual build step, ever
- A recruiter-ready project template for writing up your automation work the way hiring managers actually read it — plus a filled-out real example (an Okta access review automation) so you can see what "done" looks like before you write your own
- A `.gitignore` pre-configured to stop you from accidentally leaking AWS keys, `.env` files, or Terraform state to a public repo

## Setup (10 minutes, no prior Git experience required)

### 1. Get the repo onto GitHub
- Create a new repository on GitHub (public, so GitHub Pages can serve it for free)
- Push this starter kit into it (see the Git cheat sheet below if you've never done this)

### 2. Turn on GitHub Pages
- In your repo, go to **Settings → Pages**
- Under **Source**, select the `gh-pages` branch (this gets created automatically the first time the Action runs)
- Your site will be live at `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`

### 3. Update `mkdocs.yml`
- Set `site_url` to your actual GitHub Pages URL
- Change `site_name` to your name

### 4. Edit `docs/index.md`
- Replace the placeholder with your real bio, current focus, and contact info

### 5. Push a change and watch it deploy
- Any push to `main` triggers the GitHub Action in `.github/workflows/deploy.yml`
- Check the **Actions** tab in your repo to watch it build
- Give it 1-2 minutes, then refresh your live site

## The GRC Analyst → GRC Engineer Git Cheat Sheet

If spreadsheets and SharePoint are your normal, here's everything you need. No prior experience assumed.

### Getting the repo onto your machine
```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
cd YOUR-REPO-NAME
```

### Saving your changes
```bash
git add .
git commit -m "Add first automation project"
```
`git add .` stages everything you changed. `git commit` saves it locally with a message describing what you did — write these like you're leaving a note for future-you.

### Sending changes live
```bash
git push
```
This is the step that actually triggers the deploy. The moment you push, the GitHub Action picks it up and rebuilds your site.

### Checking what's changed before you commit
```bash
git status
```
Shows you what's staged, what's modified, and what Git doesn't know about yet. Run this before every `git add .` until it becomes muscle memory.

### If you're not sure what you broke
```bash
git log --oneline
```
Shows your commit history. Every commit is a checkpoint you can get back to.

## Filling your first portfolio slot

Your `/automation/` folder has two files: a real, filled-out example (an Okta access review automation) so you can see what a complete write-up looks like, and a blank template for your own project. Study the example, then replace the placeholder with your own work — don't ship the example as your own project.

## The reference templates page

`docs/templates.md` has three optional fill-in-the-blank templates (policy, risk assessment, control mapping), all on one page with a table of contents. Don't need them? Delete `docs/templates.md`, then remove the `Templates: templates.md` line from the `nav:` section in `mkdocs.yml`.

## Adding to the .gitignore

Already blocked by default: `.aws/credentials`, `.env` files, Terraform state, `venv/`, `__pycache__/`, and common build junk. If you add a new tool that generates local secrets or cache files, add its pattern to `.gitignore` before your first commit involving it — not after.

## Local preview (optional)

Want to see the site before pushing?
```bash
pip install -r requirements.txt
mkdocs serve
```
Then open `http://127.0.0.1:8000` in your browser.
