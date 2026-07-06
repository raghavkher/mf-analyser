# Mutual Fund Analyser

Static single-file mutual fund analytics app.

## Local editing

Edit the app here:

```bash
outputs/coin-mf-analyser.html
```

Open locally:

```bash
open outputs/coin-mf-analyser.html
```

After JS/HTML edits, run:

```bash
node -e "const fs=require('fs'); const html=fs.readFileSync('outputs/coin-mf-analyser.html','utf8'); new Function(html.match(/<script>([\s\S]*)<\/script>/)[1]); console.log('embedded script parses');"
```

## GitHub Pages deployment

1. Create a new GitHub repository.
2. Push this folder to that repository.
3. In GitHub, go to `Settings → Pages`.
4. Set source to `Deploy from a branch`.
5. Select branch `main` and folder `/root`.
6. Save.

The public URL will open `index.html`, which redirects to:

```bash
outputs/coin-mf-analyser.html
```

## Updating the live site

After editing locally:

```bash
git add outputs/coin-mf-analyser.html index.html README.md
git commit -m "Update analyser"
git push
```

GitHub Pages will update the live site shortly after the push.

## Privacy note

Uploaded tradebooks are processed in the browser. They are stored in browser `localStorage` on that user’s device unless overwritten or cleared.
