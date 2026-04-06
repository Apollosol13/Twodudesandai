# Two Dudes and AI — website

Static site for [twodudesandai.com](https://twodudesandai.com).

## Hero image

Add your movie-poster image as:

`images/hero.png`

(Replace the file; keep the same name so `index.html` does not need edits.)

## Local preview

Open `index.html` in a browser, or run a quick server:

```bash
cd /path/to/this/repo
python3 -m http.server 8080
```

Then visit `http://localhost:8080`.

## GitHub repository

1. Create a new repository on GitHub (e.g. `twodudesandai-website`).
2. In this folder:

```bash
git init
git add .
git commit -m "Initial site: mission, projects, about, hero"
git branch -M main
git remote add origin git@github.com:YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

## Hosting (GitHub Pages)

The repo includes a `CNAME` file with `twodudesandai.com` so GitHub Pages can serve your custom domain after you connect it.

1. Repo **Settings → Pages**.
2. Source: **Deploy from a branch**, branch `main`, folder `/ (root)`.
3. Under **Custom domain**, enter **twodudesandai.com** (the `CNAME` file should match). Configure DNS at your registrar (see [GitHub Pages custom domains](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)).

Alternatives: [Netlify](https://www.netlify.com/) or [Vercel](https://vercel.com/) by connecting the same repo.

## Edit copy

- **Mission / projects / bios:** edit the text in `index.html`.
- **Styles:** `styles.css` (colors are in `:root`).
