# danbrickey.dev

Dan Brickey's personal portfolio landing page — the front door to the projects,
served at **https://danbrickey.dev**.

A single, self-contained static page: an editorial "engineer's lab-notebook /
drafting-sheet" design (grid paper, ruled sections, a connector spine down the
project log), with light and dark modes. No framework, no build step, no
dependencies — just `index.html`.

## Structure

| File | What it is |
|------|------------|
| `index.html` | The whole site — HTML + inlined CSS + ~30 lines of vanilla JS (the light/dark theme toggle). |

## Local preview

Open `index.html` directly in a browser, or serve it:

```bash
python -m http.server 8000
# → http://localhost:8000
```

The theme toggle (top-right) flips light/dark; it defaults to your OS
`prefers-color-scheme` and remembers your choice in `localStorage`.

## Deploy

Deployed on **Vercel**, connected to this repo:

- **Framework preset:** Other · **Build command:** none · **Output/root:** repo root
  (`index.html` is at the top level — no build, no output subfolder).
- **Production domain:** `danbrickey.dev` (apex).
- **Redirects (301/308 → apex):** `brickey.dev`, `www.brickey.dev`,
  `danbrickey.com`, `www.danbrickey.com`, and `www.danbrickey.dev`. DNS +
  redirect rules live in Cloudflare; email routing on `brickey.dev`
  (`dan@brickey.dev`) is independent of the web redirect and unaffected.

Every push to `main` triggers a Vercel production deploy.

## Placeholders to fill

- **Headshot** — the hero frame currently holds a neutral SVG placeholder;
  replace the `.headshot__placeholder` block with a real `<img>` (a marked
  comment shows the spot).
- **GitHub contact chip** — intentionally omitted until there's a public repo or
  a profile README to link to (see the comment in the contact section).

## Provenance

The design originated as a Claude Design handoff and was first built as feature
0.13.2 of the `healthcare-data-platform` project; it graduated here to its own
repo as the standalone portfolio front door. The original design package + build
record live in that project's history.
