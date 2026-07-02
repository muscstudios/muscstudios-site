# Musc Studios Site

Static public connect page for Musc Studios.

The main page is:

```text
/connect/
```

This repo has no framework, no build step, and no dependencies. It is ready for Cloudflare Pages as a static site.

## Files

```text
index.html
connect/index.html
assets/style.css
assets/logo.png
assets/background.png
README.md
```

## Logo

Place the official Musc Studios logo at:

```text
assets/logo.png
```

The connect page uses that file at the top of the page. If the image is missing or cannot load, the page shows a clean text fallback: `Musc Studios`.

## Background

Place the Musc Studios background image at:

```text
assets/background.png
```

If you export the background as a JPG instead, update the CSS `background` image path in `assets/style.css` from `./background.png` to `./background.jpg`.

## Test locally

You can open either file directly in a browser:

```text
index.html
connect/index.html
```

For a closer production-style test, run a local static server from the repo root:

```sh
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000/connect/
```

## Deploy to Cloudflare Pages

1. Push this repo to GitHub.
2. In Cloudflare, go to Workers & Pages.
3. Create a Pages project and connect the GitHub repo.
4. Use these build settings:
   - Framework preset: None
   - Build command: leave blank
   - Build output directory: `/`
5. Deploy.
6. Add the custom domain `muscstudios.com`.
7. The connect page will be available at:

```text
https://muscstudios.com/connect/
```
