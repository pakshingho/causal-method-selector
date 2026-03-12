# Causal Inference Method Selector

Standalone static web app for choosing causal inference methods from study design, identification structure, and business goal. It preserves the current selector logic, references, responsive overview diagrams, switchback support, shareable query-string state, and exportable robustness checklists from the original portfolio-site version.

## Project Structure

- `index.html`: standalone page shell and tool markup
- `style.css`: self-contained styles for the standalone app
- `app.js`: selector logic, references, query-string sync, and checklist export
- `media/`: responsive overview diagrams used by the page

## Local Preview

Serve the repo root with any static file server so the browser can load `app.js` and the export flow cleanly.

```bash
python3 -m http.server 8000
```

Then open [http://localhost:8000](http://localhost:8000).

You can also use any equivalent static server, such as `npx serve .` or your editor's built-in preview tool.

## GitHub Pages Deployment

This repo is already structured for GitHub Pages because all assets are referenced with relative paths from `index.html`.

If this directory is not yet connected to GitHub, initialize or create a repository first, then push the files before enabling Pages.

### Option 1: Deploy from the default branch

1. Push the repository to GitHub.
2. In GitHub, open `Settings` -> `Pages`.
3. Under `Build and deployment`, choose `Deploy from a branch`.
4. Select your branch and choose the `/ (root)` folder.
5. Save the setting and wait for the Pages deployment to finish.

### Option 2: Deploy with GitHub Actions

1. Push the repository to GitHub.
2. In `Settings` -> `Pages`, set `Source` to `GitHub Actions`.
3. Add a workflow that publishes the repo root as a static site.

Because the app is pure HTML, CSS, JS, and static media, no Hugo, Wowchemy, or build step is required.

## Attribution And Disclaimer

This standalone app was extracted from the author's portfolio-site implementation and repackaged as a minimal static web app for GitHub Pages.

Reference links to third-party packages, books, articles, and company engineering posts remain the property of their respective authors and publishers.

This tool is an educational decision aid, not a substitute for design review, domain expertise, causal DAG work, or formal assumption checking. Use it to structure analysis plans and robustness reviews rather than as automatic proof of identification.
