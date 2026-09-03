# DNCE Lab website update (v5)

This is an overlay package for the existing `dongilchung/dncelab` repository. Extract/copy these files into the existing cloned repository; do not delete unrelated existing files such as publications assets, contact/join/links content, or other repository files unless you intend to replace them.

## Images

Place images at:

- `assets/images/lab-logo.png`
- `assets/images/research.avif`
- `assets/images/representation-news.jpg`
- `assets/images/people/dongil-chung.jpg`
- `assets/images/people/minho-hwang.png`
- `assets/images/people/jiwon-park.png`
- `assets/images/people/sunmin-kim.jpg`
- `assets/images/people/minjae-kim.jpg`

## Content data

- `_data/news.yml` = news database
- `_data/people.yml` = people database, including category and optional Google Scholar/Twitter fields
- `_data/publications.yml` = publications database

Publication images are optional. Set the `image` field for any publication to a repository path such as `/assets/images/publications/my-paper.jpg`. The Publications page automatically shows a thumbnail when `image` is present and the normal text-only layout otherwise.

## Website behavior

- `/` shows the representation image and the 3 newest news items.
- `/news/` shows all news from `_data/news.yml`.
- `/people/` shows Principal Investigator, Lab Members, and Alumni as separate sections.
- Email addresses are clickable `mailto:` links.
- Google Scholar/Twitter appear only when the corresponding field in `_data/people.yml` is populated.
- `/publications/` reads `_data/publications.yml` and groups items by year.

## Upload with GitHub Desktop

1. Open GitHub Desktop and choose **Repository → Show in Finder**.
2. Extract this ZIP and copy its contents into that existing `dncelab` repository folder.
3. Add the image files to `assets/images/` and `assets/images/people/` as listed above.
4. Return to GitHub Desktop.
5. Review **Changes**.
6. Enter a commit message such as `Update website content structure`.
7. Click **Commit to main**.
8. Click **Push origin**.
9. After GitHub Pages rebuilds, check `https://dongilchung.github.io/dncelab/`.

For work on another computer, first use **Fetch origin / Pull origin**, make changes, then commit and push.
