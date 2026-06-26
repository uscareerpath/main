# CareerPath website

A nonprofit platform helping immigrant professionals navigate their careers in the U.S.,
with a special focus on dependent visa holders (H-4, L-2, F-2, J-2, TD, O-3).

## What's in this repo

| Path | What it is |
|------|------------|
| `index.html` | The landing page — **this is what gets served live**. Self-contained (fonts + code inlined), no dependencies. |
| `volunteer.html` | The "Get involved" / volunteer page. Also self-contained. |
| `src/` | The **editable source** the live files are exported from. Not served — kept here as the source of truth. |

The two live pages link to each other (`index.html` ↔ `volunteer.html`), so keep both at the repo root with these exact names.

## Deploying with Vercel (auto-deploy on push)

1. Push this repo to GitHub.
2. In Vercel: **Add New → Project → Import** this repo, then **Deploy**.
   No build settings needed — it's static HTML. `index.html` is served at `/`.
3. (Optional) Add your domain under the project's **Settings → Domains**.

After that, every push to the repo auto-deploys in ~30 seconds.

## Making changes

The live `.html` files are *exported* from the source in `src/`. To change the site:

1. Edit the design (the `src/*.dc.html` files are the originals).
2. Re-export the bundled `index.html` / `volunteer.html`.
3. Commit the updated `.html` files → Vercel auto-deploys.

> Tip: paste the repo URL back to Claude any time and it can read the current
> state and produce updated files for you.

## Before a real launch

- **Forms are not wired to a backend yet.** The waitlist and the volunteer
  "get in touch" form show a thank-you message but don't store or send anything.
  Connect them to a form service (Formspree, Tally, Google Forms) or an email tool.
- Replace the placeholder email `hello@careerpath.org` with your real inbox.
- Swap the image placeholders for real photos / illustrations.

---

Built by volunteers, for the people who need it.
