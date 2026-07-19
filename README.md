# DROFFENSE — Site Export

Static, self-contained landing page. No build step required.

## Contents

```
export/
├── index.html          # the whole site (HTML + CSS + JS inline)
├── assets/
│   ├── drone.jpg        # DJI FlyCart hero image
│   ├── dropper-nobg.png # Dropper Gen. 4
│   ├── harpoon-nobg.png # Harpoon gripper
│   └── stabilizer-nobg.png
└── README.md
```

The only external dependency is the YouTube background video (loaded via
`<iframe>`), which requires an internet connection at view time.

## Preview locally

```bash
cd export
python3 -m http.server 8080
# open http://localhost:8080
```

(Open via a server, not `file://`, so the YouTube embed and relative asset
paths behave correctly.)

## Deploy

Drop the contents of this folder onto any static host:

- **Netlify** — drag the `export/` folder into the dashboard, or `netlify deploy --dir=export --prod`
- **Vercel** — `vercel deploy export --prod`
- **GitHub Pages** — commit the files to a `gh-pages` branch or `/docs`
- **S3 / Cloudflare Pages / any CDN** — upload as-is

No environment variables, no server runtime.

## Editing

Everything lives in `index.html`. Contact email: `info@droffense.com`.
