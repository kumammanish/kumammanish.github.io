# How this repo works

`kumam.github.io` is a single-page static portfolio site with no build system, no
package manager, and no test suite. Everything lives in one file, `index.html`, deployed
directly by GitHub Pages.

## Component overview

```mermaid
flowchart TD
    subgraph Repo["kumam.github.io (repo root)"]
        HTML["index.html (~1120 lines)"]
        Assets["assets/images/\n(profile photo)"]
        Ignore[".gitignore"]
    end

    subgraph HTMLFile["index.html — three inline blocks"]
        Style["&lt;style&gt; (~lines 21-711)\nCSS custom properties in :root\n(--bg-dark, --accent, --text-primary, ...)"]
        Body["&lt;body&gt; (~lines 712-1044)\nnav + section elements"]
        Script["&lt;script&gt; (~lines 1045-1121)\nvanilla JS, no dependencies"]
    end

    HTML --> Style
    HTML --> Body
    HTML --> Script
    Body -.references.-> Assets

    Style -->|"themes via CSS vars"| Body
    Script -->|"drives interactivity of"| Body
```

## Page sections (in DOM order)

```mermaid
flowchart LR
    Nav[nav] --> Hero[section#hero]
    Hero --> About[section#about]
    About --> Experience[section#experience]
    Experience --> Projects[section#projects]
    Projects --> Skills[section#skills]
    Skills --> Contact[section#contact]

    subgraph ExperienceDetail["experience section internals"]
        Tabs[".job-tab buttons\n(data-job attribute)"] -->|click switches| Panels[".job-panel divs\n(job1, job2, job3)"]
    end

    Experience -.contains.-> ExperienceDetail
```

## JavaScript behavior (`<script>` block)

No dependencies, four responsibilities:

1. **Mobile nav toggle** — shows/hides the nav on small screens.
2. **Experience tab switching** — clicking a `.job-tab` shows the matching `.job-panel`
   (matched via `data-job`).
3. **Scroll-reveal** — `IntersectionObserver` watches each `.section` element and
   reveals it as it enters the viewport.
4. **Smooth-scroll** — in-page anchor links (`nav` → sections) scroll smoothly instead
   of jumping.

## Styling approach (`<style>` block)

All theming goes through CSS custom properties declared once in `:root`
(`--bg-dark`, `--bg-light`, `--accent`, `--text-primary`, etc.) — change the color
scheme by editing these variables, not individual selectors throughout the file.

## Deployment

```mermaid
flowchart LR
    Dev["Edit index.html locally"] -->|"git push to main"| GH["GitHub"]
    GH -->|"GitHub Pages serves\nbranch root directly"| Live["kumam.github.io\n(live in 1-2 min)"]
```

No CI, no build step — GitHub Pages serves `index.html` directly from the `main` branch
root. Local preview: open `index.html` in a browser, or `python -m http.server 8000`.

## External dependencies

CDN-only, no npm packages: Google Fonts (Inter) and Font Awesome icons, both loaded via
`<link>` tags in `<head>`. The favicon is an inline SVG data URI (`<MK>` text mark), not
a separate file.

## Content editing

Personal details (name, links, job history, projects, skills) are hardcoded inline in
`index.html` — there's no separate data/config file to look for. See `CLAUDE.md` at the
repo root for exact line ranges and editing notes.
