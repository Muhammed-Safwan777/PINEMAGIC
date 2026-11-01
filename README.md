# PineMagic Bromelain: Usage & Safety Guide

The mobile-first page customers see when they scan the QR code on the PineMagic Bromelain 2400 GDU (15 g) jar. It covers the correct dose, when to take it, benefits, safety warnings and FAQs.

HIZLI ESCALA LLP, Ramanattukara, Kozhikode, Kerala, PIN 673633.

## Files

```
index.html                  The whole page (HTML + Tailwind via CDN + a little vanilla JS)
assets/
  logo.png                  Full PineMagic logo (footer)
  logo-mark.png             Pineapple mark (header)
  logo-wordmark.png         "pinemagic" wordmark (header)
  jar.webp                  Photo of the 15 g jar
  dosage-spoons.webp        Correct vs incorrect spoon image
  favicon.png               Browser tab icon
```

There is no build step. Tailwind CSS and the fonts (Source Serif 4, Atkinson Hyperlegible) load from their CDNs.

## Publish with GitHub Pages

1. Create a new public repository on GitHub, for example `pinemagic-bromelain-guide`.
2. Upload `index.html`, `README.md` and the whole `assets` folder to the root of the repository (**Add file → Upload files**, then drag them in).
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, set **Source** to *Deploy from a branch*, choose the `main` branch and the `/ (root)` folder, then click **Save**.
5. After a minute or two the page is live at `https://<your-username>.github.io/pinemagic-bromelain-guide/`.
6. Generate the QR code from that address (or from your custom domain, see below).

### Custom domain (optional)

In **Settings → Pages → Custom domain**, enter something like `guide.pinemagic.in`. Then add a `CNAME` DNS record at your domain provider pointing that subdomain to `<your-username>.github.io`. Turn on **Enforce HTTPS** once it's available.

## Editing the page

All the text is in `index.html`, one section per block:

| Section | Find this in index.html |
| --- | --- |
| Header and intro | `<header id="top"` and `<section id="intro"` |
| Dosage | `<section id="dosage"` |
| When to take it (switch + timeline) | `<section id="timing"` |
| Benefits | `<section id="benefits"` |
| Safety warnings | `<section id="safety"` |
| FAQ | `<section id="faq"` |
| Disclaimer and company details | `<footer` |

To replace an image, keep the same file name in `assets/`, or update the `src` path in `index.html`.

Colours and fonts are set in the `tailwind.config` block near the top of `index.html`.
