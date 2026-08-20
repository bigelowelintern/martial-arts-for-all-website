# Martial Arts For All Foundation — Website

Static, no-build HTML/CSS/JS site. No backend, no dependencies.

## Structure

```
index.html       Home
about.html        About Us
programs.html      Programs
partners.html      Partners
css/style.css     Shared styles
js/main.js       Mobile nav toggle
Images/          Logo + photos
```

See [CONTENT_TODO.md](CONTENT_TODO.md) for placeholder content that still needs real copy before launch.

## Local preview

No build step required — open `index.html` directly in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Deploying to GitHub Pages

1. Push this folder to a GitHub repository (the `.nojekyll` file is already included so GitHub doesn't run the site through Jekyll).
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`.
4. Save — GitHub will publish the site at `https://<username>.github.io/<repo>/`.

## Pointing your purchased domain

1. In your domain registrar's DNS settings, add:
   - An `A` record for the apex domain (`example.org`) pointing to GitHub Pages' IPs: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`.
   - A `CNAME` record for `www` pointing to `<username>.github.io`.
2. In the repo, add a file named `CNAME` at the root containing just your domain (e.g. `martialartsforall.org`).
3. Back in **Settings → Pages**, enter the custom domain and check **Enforce HTTPS** once the certificate provisions (can take up to 24 hours).
