# Two Dudes and AI — website

Static site for [twodudesandai.com](https://twodudesandai.com), deployed with **Netlify** from **GitHub**.

## 1. Push to GitHub (do this first)

1. On GitHub, create a **new repository** (e.g. `twodudesandai-website`). Do **not** add a README, `.gitignore`, or license (this repo already has them).
2. In this folder on your machine:

```bash
cd /Users/brennenstudenc/Desktop/Twodudes
git remote add origin git@github.com:YOUR_USERNAME/YOUR_REPO.git
git push -u origin main
```

Use **HTTPS** instead of SSH if you prefer:

`git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPO.git`

## 2. Connect Netlify

1. Sign in at [Netlify](https://www.netlify.com/) (GitHub login is fine).
2. **Add new site → Import an existing project → GitHub**, authorize Netlify if asked, pick this repository.
3. Leave **build command** empty. Set **publish directory** to **`.`** (a dot = site root). The included `netlify.toml` does this for you.
4. Deploy. Netlify gives you a random `something.netlify.app` URL to verify the site.

## 3. Custom domain (twodudesandai.com)

1. In Netlify: **Site configuration → Domain management → Add a domain** → enter `twodudesandai.com` and `www.twodudesandai.com` if you want both.
2. Follow Netlify’s **DNS** instructions for your registrar:
   - Usually an **apex** record (A or ALIAS) for `twodudesandai.com` and a **CNAME** for `www` pointing at Netlify.
3. Turn on **HTTPS** in Netlify (it provisions a certificate after DNS propagates; can take a few minutes to hours).

Remove or update any old DNS records that pointed the domain elsewhere (e.g. previous GitHub Pages records).

## Local preview

```bash
cd /Users/brennenstudenc/Desktop/Twodudes
python3 -m http.server 8080
```

Open `http://localhost:8080`.

## Hero image

`images/twodudesai.png` — replace the file to change the poster; `index.html` references it.

## Edit copy

- **Content:** `index.html`
- **Styles:** `styles.css` (`:root` for colors)
