# Ian Crosby Portfolio

Single-page portfolio website for Ian Crosby.

## Files

- `index.html` — main site
- `preview.html` — optional preview/scratch file
- `assets/` — images and media

## Local Preview

Open `index.html` in your browser.

## Structure

- Hero, About, Projects carousel, Operating System section, Contact (LinkedIn button)
- Project cards and carousels are data-driven in `index.html`

## Notes

- Images are stored under `assets/` and pre-treated for consistent tone/contrast.
- Carousel images are grouped per project in `hubCarouselItemsByProject`.

## Recovery / Rebuild

If anything breaks or you need to rebuild from scratch:

1. Restore base files
- `index.html`
- `assets/`

2. Verify key sections exist
- Hero, About, Projects, Operating System, Contact

3. Check data blocks in `index.html`
- `projectCardData` (titles + blurbs)
- `projectHeroMap` (card background images)
- `hubCarouselItemsByProject` (per-project carousel images)
- `projectCarouselBlurbMap` (carousel footer blurbs)

4. Re-apply image treatment (optional)
If raw images were re-added, apply the baseline image treatment:
`/opt/homebrew/bin/magick <input> -strip -colorspace sRGB -modulate 102,92,100 -contrast-stretch 1%x1% -unsharp 0x0.8+0.5+0.02 <output>`

5. Quick smoke check
- Open `index.html` and confirm:
  - Carousel loads
  - Clicking cards opens correct carousels
  - Images render
  - LinkedIn button works
