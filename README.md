# recruiter-intelligence-suite-os


Live product site + interactive diagnostics. Static HTML only — no build step, no dependencies.

## Structure

```
/                  → overview / landing page (index.html)
/audit/            → Pipeline Trust Decay Audit (interactive, 13-question diagnostic)
/comp-curve/       → Comp Curve Diagnostic (interactive comp calculator)
```

Each folder has its own `index.html`, so GitHub Pages serves clean URLs automatically:
- `https://<username>.github.io/<repo>/`
- `https://<username>.github.io/<repo>/audit/`
- `https://<username>.github.io/<repo>/comp-curve/`

## Deploy (GitHub Pages, no Actions, mobile-safe)

Folder upload from a mobile browser is unreliable — file pickers usually flatten nested paths. Skip it entirely and use GitHub's **Create new file** box instead, which lets you type a path with slashes and it builds the folders for you:

1. On github.com (mobile browser, not the app), create a new repo — e.g. `recruiter-intelligence-suite`.
2. Tap **Add file → Create new file**.
3. In the filename field, type `index.html` (root file). Paste the contents of this repo's `index.html`. Commit.
4. Repeat: filename `audit/index.html` → paste `audit/index.html` contents → commit. GitHub auto-creates the `audit` folder.
5. Repeat: filename `comp-curve/index.html` → paste `comp-curve/index.html` contents → commit.
6. Optionally repeat once more for `README.md`.
7. Go to **Settings → Pages**. Under "Build and deployment": **Source: Deploy from a branch**, **Branch: main**, folder **/ (root)**. Save.
8. Live in 1–2 minutes at the URL pattern above.

No zip, no drag-and-drop, no Actions — just four copy/paste commits.

## Status

- [ ] Case study metrics in `index.html` need review — currently illustrative, not verified client data. Label clearly or remove before public promotion.
- [ ] Custom domain (optional, later)
- [ ] Open Graph / social preview tags (needed before LinkedIn link-sharing looks right)
