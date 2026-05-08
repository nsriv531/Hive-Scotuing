# Form the Hive

This version has **zero npm dependencies**.

## To Run locally

```bash
npm i
npm run dev
```

Then open:

```text
http://localhost:3000
```

You can also open `index.html` directly in a browser, but using `npm run dev` is closer to how it behaves when hosted.

Recommended settings for Vercel:

- Framework Preset: Other
- Build Command: `npm run build` or leave blank
- Output Directory: leave blank / root

The `vercel.json` file rewrites routes back to `index.html`, so the app loads from the root URL.

## Main files

```text
index.html      # The scouting app
server.js       # Tiny local static server, no dependencies
package.json    # Scripts only, no dependencies
vercel.json     # Static Vercel routing
```
