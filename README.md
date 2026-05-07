# Form the Hive — Static Vercel Version

This version keeps the original scouting app as a single `index.html` file and removes the Next.js dependency tree.

## Why this is faster than the Next.js wrapper

The original app is already plain HTML, CSS, and JavaScript. The previous Next.js wrapper installed Next.js, React, React DOM, TypeScript, and platform-specific compiler packages. That makes `npm i` much slower even though the app itself does not need those packages.

This version has **zero npm dependencies**.

## Run locally

```bash
npm i
npm run dev
```

Then open:

```text
http://localhost:3000
```

You can also open `index.html` directly in a browser, but using `npm run dev` is closer to how it behaves when hosted.

## Deploy to Vercel

Push this folder to GitHub and import it into Vercel.

Recommended settings:

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
