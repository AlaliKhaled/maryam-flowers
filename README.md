# A Gift for مريم ❤️

A single-page gift site styled as a **developer terminal**. It boots up, types
shell commands on its own, "compiles" the gift with animated progress bars, then
prints the name **مريم / MARYAM** as ASCII banner art framed with roses — signed
off with love.

Pure HTML/CSS/JS. No build step, no dependencies (JetBrains Mono + Amiri load from Google Fonts).

## Run locally

Just open the file:

```bash
xdg-open index.html
```

Or serve it:

```bash
python3 -m http.server 8080
# then visit http://localhost:8080
```

## Customize

Everything is at the top of the `<script>` block in `index.html`:

```js
const NAME_EN = "MARYAM";        // ASCII / latin name
const NAME_AR = "مريم";          // big Arabic hero name
const USER    = "khaled";        // sender (shown in prompt + signature)
const MSG     = "You are the best thing that ever compiled into my life.";
const MSG_AR  = "كلّ يومٍ معكِ هو أجمل من سابقه. أحبّكِ يا مريم.";
```

Terminal colors live in the `:root { ... }` CSS variables (rose/gold love theme).
To change the big ASCII name, replace the `BANNER` string (generate one at
https://patorjk.com/software/taag with the "Standard" font).

## Deploy

It's a static site, so any static host works.

### Vercel
```bash
npm i -g vercel      # if you don't have it
vercel                # preview
vercel --prod         # production
```
Or connect the GitHub repo in the Vercel dashboard → it just works (no framework needed).

### GitHub Pages
Push this folder to a repo, then Settings → Pages → deploy from the `main` branch,
root folder. Done.
