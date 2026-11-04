# Maintaining Dong Du's homepage

The public site is https://dongd.info/ (CNAME: `dongd.info`). This is a customized al-folio v1 site; runtime layouts remain owned by the pinned gems. Keep `Gemfile.lock` tracked and review dependency updates separately from content changes.

## Content entry points

- `_pages/about.md`: biography, photo, services, recruiting, eight recent news items, selected papers.
- `_bibliography/papers.bib`: complete publication list. `_pages/publications.md` renders every year automatically, newest first; no annual year-list edit is needed.
- `_news/*.md`: announcements. The home page shows eight; `/news/` keeps the complete history. Use an explicit timezone for new entries. Preserve historical dates unless an authoritative correction is known.
- `_data/socials.yml`: verified contact links. Do not restore template email, Scholar ID, or example CV PDF.
- `_data/cv.yml`: migrated personal CV in the v1 schema. It remains unpublished and needs a content review before release. `_data/cv_legacy.yml` preserves the complete previous CV verbatim, including historical titles and dates; do not infer a promotion date from the current title.
- `assets/img/dongdu-profile.jpg`: optimized 1000-pixel portrait used by the page. The full-resolution `dongdu-2024.jpeg` is retained in source and excluded from the public build. Earlier personal photos `dongd.jpeg` and `dongdu.jpeg` are also preserved.

A bibliography entry should have a unique key and official author order/title/year/venue. Use the publisher's DOI or page URL. Set `bibtex_show={true}`, a venue `abbr`, and `selected={true}` only if it belongs on the homepage. Existing `corresponding` information is retained, displayed via `additional_info`, and excluded from exported BibTeX. The complete sources and unresolved details for this update are in `PUBLICATION-SOURCES.md`.

## Reopen a page when ready

Projects is now enabled and contains DeltaBox Lite. The nine sample project files remain explicitly excluded. CV, blog, repositories, people, teaching, bookshelf, plugin showcase and the example dropdown are disabled. They are retained in source. Hiding uses both `published: false` / `nav: false` in front matter and explicit `_config.yml` exclusions so templates do not enter search or sitemap output.

1. Replace all example material on the chosen page and in its data/assets.
2. Remove that page's `_config.yml` exclusion and change `published` to `true`.
3. Set `nav: true` and a distinct `nav_order` if it needs a navigation entry.
4. For new projects, add a genuine project file under `_projects/`. Keep the nine `*_project.md` sample exclusions until each sample is replaced. For books and teaching, remove their collection exclusion and enable output only after replacing the samples.
5. For CV, enable `al_folio.features.cv.enabled`; review `_data/cv.yml` and add a genuine PDF only if desired. The Einstein JSON/RenderCV examples remain excluded.
6. For blog, enable pagination and add a real post before exposing its entry.
7. Rebuild and check output, search, and sitemap. Do not remove all exclusions wholesale.

## Build and preview

Use Ruby 3.3 or later with Bundler 4.0.6 (the lockfile version), Node.js for Terser, and a UTF-8 locale. The Linux desktop's system Ruby 2.5 and cached old al-folio Docker image cannot satisfy this lockfile. Use a modern runtime; do not downgrade the lockfile to accommodate that environment.

```sh
export LANG=en_US.UTF-8
export LC_ALL=en_US.UTF-8
bundle install
JEKYLL_ENV=production bundle exec jekyll build
bundle exec al-folio upgrade audit --no-fail
bundle exec al-folio upgrade overrides audit
bundle exec jekyll serve --host 127.0.0.1 --port 8765
```

ImageMagick generation is disabled because the current site uses a prepared small portrait. No notebook conversion is required by published pages; the plugin may print an advisory if Jupyter is absent. Plugin/theme components and the GitHub deployment workflow are preserved.

For a remote preview, bind to loopback and forward it from your desktop:

```sh
ssh -N -L 8765:127.0.0.1:8765 dd@dd-PC7
```

Open http://127.0.0.1:8765/. A preview is not a production deployment. The GitHub workflow deploys after pushing to `main`/`master`; this maintenance branch must be reviewed before any commit/push/merge.

## Migration audit (2026-11-04)

The old bibliography has **23** entries (one entry is indented, so a column-zero grep counts only 22); all keys remain, with nine new entries for **32** total. All 24 old news files remain, plus four new items. Both old and new `_posts/` were empty. Biography, services and recruiting content remain, with spelling/name/link corrections. The personal CV and two older portraits were the personal material omitted by the earlier migration and have now been restored.

Old theme JavaScript, SCSS, template screenshots and `papers-template.bib` were intentionally not copied: these are template/runtime assets, not missing personal content. No local template override was introduced. The upgrade audit and override audit both pass.

### Linux desktop convenience commands

An isolated Homebrew portable Ruby 4.0.9 runtime and the locked gems are installed in `~/devlop/blog/.homepage-tools/` on `dd-PC7`. The runtime archive and Linux gem archives were checked against the official SHA256 records. This directory is outside the repository; system Ruby is untouched. `bin/site` discovers this sibling directory, selects a UTF-8 locale, and enforces the tracked lockfile:

```sh
cd ~/devlop/blog/dd-page-new-new
bin/site build
bin/site audit
bin/site serve
```

The desktop also has glibc 2.27, below the locked Nokogiri native gem requirement (2.28). On this host `bin/site` automatically runs in the already available `ubuntu:22.04` container, mounting the isolated runtime and source and using your user ID; no host libraries are upgraded.

`serve` builds the production pages and serves the static output at `127.0.0.1:18765` (the container port is published on host loopback only). Run `bin/site build` after content edits to refresh the preview. Forward that port with `ssh -N -L 18765:127.0.0.1:18765 dd@dd-PC7` when using the Linux server from another machine. If local port 18765 is occupied by another preview, choose a different local port in the SSH forwarding command. On another checkout without this runtime, the script uses the Ruby/Bundler already on PATH. Dependency installation remains an explicit `bundle install`; the script never resets `Gemfile.lock`.
