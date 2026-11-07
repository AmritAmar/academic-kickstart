# amritamar.com

Personal site built with Hugo 0.55.6 and the Academic theme (git submodule in `themes/academic`).
Hosted on Cloudflare Pages: every push to `master` builds and deploys to https://amritamar.com.

```bash
git submodule update --init   # first time only
hugo server                   # preview at http://localhost:1313
```

Cloudflare Pages build settings: build command `hugo`, output directory `public`,
environment variable `HUGO_VERSION=0.55.6`.

The old `AmritAmar/AmritAmar.github.io` repo only redirects visitors to amritamar.com.
