# DNCE Lab GitHub Pages update

This ZIP is an **overlay package** for the existing `dongilchung/dncelab` repository. Copy/extract these files into the repository root; do not delete the existing publications, links, join, contact, or other files.

## What changed

- `/` is now the **News** page and shows the same complete news list as `/news/`.
- News content is managed in `_data/news.yml`.
- People content is managed in `_data/people.yml`.
- `/research/` keeps the current Research text and adds a `research.avif` image area.
- The lab logo is configured as `lab-logo.png`.
- People photos use fixed display dimensions with `object-fit: cover`, so different source image sizes/crops display uniformly.
- Existing navigation remains: NEWS, RESEARCH, PEOPLE, PUBLICATIONS, LINKS, JOIN, CONTACT.

## Image files to add

The ZIP does not contain the actual photographs/logo because only their filenames were provided. Add these real files to the repository root with exactly these names:

- `lab-logo.png`
- `research.avif`
- `dongil-chung.jpg`
- `minjae-kim.jpg`
- `sunmin-kim.jpg`
- `minho-hwang.png`
- `jiwon-park.png`

## Recommended Mac setup

### 1. Git
Install Git. macOS may offer Command Line Tools automatically when you first run `git` in Terminal.

### 2. GitHub Desktop (easiest synchronization)
Install GitHub Desktop, sign in to GitHub, and clone `dongilchung/dncelab`. You can then edit files locally and use **Commit to main → Push origin**.

### 3. Jekyll local preview (recommended if you want to check the site before publishing)
Ruby and Bundler are needed. This repository includes a `Gemfile` using the `github-pages` gem. From the repository folder:

```bash
bundle install
bundle exec jekyll serve
```

Then open the local URL shown by Jekyll (normally `http://localhost:4000/dncelab/`).

## First installation using Terminal

```bash
git clone https://github.com/dongilchung/dncelab.git
cd dncelab
```

Extract this ZIP and copy its contents into the `dncelab` folder. Add the real image files listed above. Then:

```bash
bundle install
bundle exec jekyll serve
```

After checking the site:

```bash
git status
git add .
git commit -m "Redesign lab website and organize news and people data"
git push origin main
```

## Future content updates

### Add/edit News
Edit only `_data/news.yml`. Add a new item at the top:

```yaml
- date: 2026-09-02
  title: "News title"
  content: |
    News text goes here.

    A second paragraph can go here.
```

Both `/` and `/news/` automatically update from this file.

### Add/edit People
Edit `_data/people.yml`. Change name, role, affiliation, email, order, or image filename there.

### Git synchronization

On any computer that has the repository:

```bash
git pull origin main
```

After local changes:

```bash
git add .
git commit -m "Update lab website"
git push origin main
```

Git therefore serves as the version-controlled synchronization layer for the News and People data. The YAML files are the simple content database; no separate database server is required.


## Recommended workflow with GitHub Desktop

1. Clone `https://github.com/dongilchung/dncelab.git` with GitHub Desktop.
2. Extract this ZIP into the cloned `dncelab` folder and allow files to be merged/replaced. Do **not** delete the existing repository files.
3. Put the six image files into `assets/images/`:
   - `lab-logo.png`
   - `research.avif`
   - `dongil-chung.jpg`
   - `minho-hwang.png`
   - `jiwon-park.png`
   - `sunmin-kim.jpg`
   - `minjae-kim.jpg`
4. Open the repository in GitHub Desktop. Review the changed files.
5. Commit with a message such as `Update DNCE Lab website structure and assets`.
6. Click **Push origin**. GitHub Pages will rebuild the site from the configured publishing source.
7. For work on another computer, first use **Fetch origin / Pull origin**, make changes, commit, and then **Push origin**.

GitHub Pages publishes changes pushed to the configured branch/source automatically.
