# DNCE Lab GitHub Pages update package

This is an overlay package for the existing `dongilchung/dncelab` repository. Do not delete the existing repository; extract these files into the existing cloned repository and overwrite matching files.

## Image locations

Add the real image files yourself:

- `assets/images/lab-logo.png`
- `assets/images/research.avif`
- `assets/images/representation-news.jpg`
- `assets/images/people/dongil-chung.jpg`
- `assets/images/people/minho-hwang.png`
- `assets/images/people/jiwon-park.png`
- `assets/images/people/sunmin-kim.jpg`
- `assets/images/people/minjae-kim.jpg`

## Pages

- `/` is the home/news page and shows the large representation image plus the three newest news items.
- `/news/` shows all news items.
- `/research/` uses the Research text from the current Wix site and `research.avif` below it.
- `/join/` contains the current Wix Join content, internal anchors, email links, and the linked position PDF.
- `/contact/` contains the current Wix contact information, a Research Participation section, and a Google Maps embed below it.
- `/people/` is driven by `_data/people.yml`.
- News is driven by `_data/news.yml`.

## GitHub Desktop workflow

1. Clone `https://github.com/dongilchung/dncelab.git`.
2. Extract this package into that existing repository folder and overwrite matching files.
3. Add the real images at the paths above.
4. Open GitHub Desktop and review Changes.
5. Commit to `main`.
6. Click `Push origin`.
7. Check `https://dongilchung.github.io/dncelab/` after GitHub Pages finishes building.

For future updates, edit `_data/news.yml` for News and `_data/people.yml` for People, then commit and push.
