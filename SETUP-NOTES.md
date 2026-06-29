# Astrova Systems — rebuild (v3)

This version is a full visual redesign on top of the v2 structure: scroll-triggered
reveals throughout, an animated particle-grid hero, tilt/glow hover cards for
services, an animated connector line for the process steps, a draggable video
testimonial carousel, and a continuously scrolling reviews marquee. All
animations respect `prefers-reduced-motion`.

## 1. Run it
```
npm install
npm run dev
```
Open http://localhost:4321

## 2. Add your real images and videos
The site currently references these paths but the files aren't included
(pull them from your old site's `images/` and `videos/` folders):

Place in `public/images/`:
- astrova-logo.png
- apexlogo.png, apexlogo2.png, wraptors.png, tintworld.jpg, eliteautospa.jpg,
  blackoptix.png, legends.jpg, advanced.jpg, triple.png, iced.png, shade.jpg,
  dream.jpg, elitetint.png, velocity.png
- zeyad1.jpg
- og-default.jpg (a 1200x630 image used when the site is shared on social media)
- poster1.png through poster13.png (thumbnail images shown before each
  testimonial video plays — matched 1-to-1 with testimonial-1.mp4 through
  testimonial-13.mp4)

Place in `public/videos/`:
- testimonial-10.mp4, testimonial-2.mp4, testimonial-11.mp4

Once dropped into those folders, refresh the browser — no code changes needed,
the paths already point there.

## 3. Pages
- `/` — homepage
- `/testimonials` — full testimonials page

## 4. Before going live
- Update `astro.config.mjs` `site:` if the domain ever changes
- Replace the Google review snippets in `GoogleReviews.astro` if you want to
  pull fresh ones
- Add real `og-default.jpg` for social sharing previews
- Run `npm run build` then deploy the `dist/` folder (or connect the repo
  directly) to Vercel or Netlify

## 5. Deploying
**Vercel**: push this folder to a GitHub repo, then "Import Project" on
vercel.com — it auto-detects Astro, no config needed.

**Netlify**: same idea — "Add new site" → connect repo → it auto-detects
Astro and sets build command `npm run build`, publish directory `dist`.
