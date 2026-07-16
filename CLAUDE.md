# EDGE Group site

GitHub Pages site for the EDGE Group @ DET, Politecnico di Torino.
Jekyll, built by GitHub Pages itself on every push to `main` — a push is a deploy.
There is no Action, no `Gemfile`, and no dependency to install for deploying.

## Where things are

```
_config.yml            site title, tagline, nav, and the topic map (see below)
_layouts/default.html  header, nav, footer — every page
_layouts/post.html     article wrapper (title, date, byline)
assets/css/style.css   all styling, no framework
index.html             landing page
projects.html          repo list + the fetch/grouping script
research.md people.md contact.md articles.md gallery.md
_posts/                one Markdown file per article
_data/gallery.yml       photo filename -> event, read by gallery.md
photo/                  the actual gallery photo files, served as static files
photo/people/           headshots referenced directly by path in people.md
```

## Adding things

- **A page** → new `.md` with `layout: default`, `title:`, `permalink:` front matter,
  then add it to `nav:` in `_config.yml`.
- **An article** → copy any existing file in `_posts/` to `_posts/YYYY-MM-DD-slug.md` and
  replace the front matter and body. Filename date must match `date:`; future dates don't
  publish. Front matter fields: `title`, `date`, `authors`, `citation` (venue/year string),
  `paper_url`, `repo_url` (omit entirely when there's no repository) — the post body is the
  abstract. `/articles/` groups posts by year into click-to-expand `<details>` sections
  (newest year open by default), each post rendered as a box: title, `authors`, `citation`,
  then the abstract itself behind a second click-to-expand. `paper_url`/`repo_url` become
  icon links on the right. The search box on that page filters by `title`/`authors` only
  (not the abstract) — see the `data-title`/`data-authors` attributes on `.pub` in
  `articles.md` if that ever needs to change.
- **A repo** → nothing here. Tag it on GitHub. See below.
- **A gallery photo** → drop the image file in `photo/`, then add one entry to
  `_data/gallery.yml` (`file:` the exact filename, `event:` the caption/tag). `gallery.md`
  groups photos by `event` automatically — reuse the same `event` string across photos
  from the same event so they land in one section. This is a Jekyll data file (not a
  page), because GitHub Pages builds with no custom plugins and no Action, so Liquid
  needs YAML it can iterate natively — a free-text manifest can't be parsed without one.
- **A person** → drop a headshot in `photo/people/` and reference it directly by path
  in `people.md` (`<img class="person-photo" src="/photo/people/name.jpg" ...>`). No repo
  photo yet → point at `/photo/people/omino.png`, the placeholder silhouette. `.person-photo`
  CSS crops every photo to the same small circular size regardless of source dimensions,
  so photos don't need to be pre-resized before adding.

## The project list

`projects.html` fetches `api.github.com/orgs/edge-group-polito/repos` client-side on page
load and groups repos by their **GitHub topics**. The topic-to-section mapping lives in
`topics:` in `_config.yml` and is injected into the page with `{{ site.topics | jsonify }}`.

- New research area → one `github-topic: Section Title` line in `_config.yml`.
- New repo → tag it on GitHub (repo page → About → gear → Topics). Nothing to commit here.

Several topics on one repo → it appears in several sections. Untagged repos land in "Other"
so nothing disappears silently.

What is hidden, and why — this is deliberate, don't "simplify" it away:

- **Anything tagged `no-site`** (`hide_topic:` in `_config.yml`): explicit opt-out, checked
  first, beats every other rule. Tag a repo `no-site` on GitHub and it leaves the page.
- `.github` and the site repo itself: infrastructure, never interesting.
- **Untagged forks**: the org carries ~14 upstream mirrors (`llvm-project`, `pulp-runtime`,
  `pulpissimo`, `cv32e40x`, …) that nobody works on. A fork *with* a known topic is shown —
  tagging it is how you say "this fork is ours". That is why `x-heep` and `cva6` are absent:
  they need a topic, not a code change.
- Archived repos **are shown**, with an `archived` badge. `KALIPSO`, `LOKI`, `ATHOS` and
  `CHIMERA` are real group output and were wrongly hidden at first.

A blanket `if (r.fork) continue` was the original bug: it hid `x-heep` (the group's own
platform) and `keccak_or_ascon` even after it was tagged.

Two failure modes worth knowing, both already hit once:

- A topic in `_config.yml` that no repo actually uses does nothing, and a topic on a repo
  that isn't in `_config.yml` silently sends it to "Other". **Check the real topics before
  editing the map**: `curl -s "https://api.github.com/orgs/edge-group-polito/repos?per_page=100" | jq -r '.[] | select(.topics|length>0) | "\(.name) \(.topics)"'`
- Most of the org (23 repos as of July 2026) is untagged and sits in "Other". That shrinks
  as people tag repos; it is not a bug to code around.

Topic keys must be valid GitHub topics: lowercase letters, numbers, hyphens; no slashes, no
spaces, no uppercase. Punctuation belongs in the section title on the right (`ai-ml: AI/ML`).

Never replace this with a hardcoded list of repos — it goes stale the moment someone adds a
repo and forgets the site exists.

## Constraints

- **No JS framework, no CSS framework, no npm.** Vanilla, hand-written, inline where small.
  Jekyll + the browser are the whole toolchain.
- **No GitHub Action.** Pages builds Jekyll natively; adding CI to do it again is noise.
- Keep pages readable as plain Markdown. Liquid only where it removes duplication.

## Previewing

Local preview needs Jekyll, which is **not** installed here and won't install cleanly on the
system Ruby 2.6 (`jekyll not found`, `/usr/bin/ruby` is 2.6.10). Options, in order of laziness:

1. Push to a branch and look at the Pages preview / just push to `main`.
2. `brew install ruby` then `gem install jekyll bundler` if local preview is worth it.

Liquid templating can't be checked with `python3 -m http.server` — it serves the raw
`{{ }}`. Don't trust that as a preview.

## If asked to make the repo list faster / SEO-visible

The known upgrade is a nightly GitHub Action writing `repos.json`, with `projects.html`
fetching that instead of the live API. ~20 lines. Only do it if the client-side fetch causes
a real problem (rate limits, search indexing) — not preemptively.

## Style

Prose is for researchers and prospective students. Plain, concrete, no marketing voice.
`TODO:` markers are real gaps waiting on content from the group — ask before inventing text
for them.
