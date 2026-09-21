# Fingaz

A hand-to-hand duel for two thumbs — chopsticks, with knockouts.
One self-contained HTML file: no build step, no dependencies, works offline.

## Play

Open `index.html`, or visit the hosted version.

- Tap one of your hands, then a rival hand. Your fingers are added to theirs.
- **5 or more** knocks that hand out for good.
- **Shift** slides fingers between your own hands. **Half** revives a dead hand.
- **Minus** and **Team** are one-shot specials.
- A dice roll decides who goes first.

Play the CPU — Momo, Kurogane or Yurei — or hand the phone back and forth
in 2-player mode, where the second deck is rotated for the player opposite.

## Put it on the web with GitHub Pages

1. Create a new **public** repository on GitHub.
2. Upload everything in this folder to the root of the repo
   (`index.html`, `manifest.webmanifest`, `sw.js`, and the icons).
3. **Settings → Pages → Source: Deploy from a branch → `main` / `/ (root)` → Save.**
4. After a minute or two it's live at
   `https://<your-username>.github.io/<repo-name>/`

Free GitHub Pages requires the repo to be public. If you want it private,
Cloudflare Pages and Netlify both host private repos free and work the same way.

### Once it's hosted

- **Add to home screen** on a phone and it opens fullscreen with its own icon.
- It keeps working with no signal, thanks to `sw.js`.
- Sharing the link shows the `og-image.png` preview card.

If you change the game, bump `CACHE = 'fingaz-v1'` in `sw.js` (to `v2`, etc.)
so returning players get the new version instead of the cached one.

## Files

| file | what it is |
| --- | --- |
| `index.html` | the whole game — art, sound, music and logic |
| `manifest.webmanifest` | makes it installable to a home screen |
| `sw.js` | offline cache |
| `icon-*.png` | app icons |
| `og-image.png` | link preview card |
