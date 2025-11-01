# In Sync — Digital Art Exhibit

Digital Art Exhibit is a small static website showcasing collaborative multimedia work from a group of students (photography, cinematography, and graphic design). This repository contains the site HTML, CSS, images, and a small carousel script for the gallery.

## Project Summary

- Project: In Sync — Digital Art Exhibit
- Type: Static website (HTML, CSS, minimal JavaScript)
- Purpose: Display a curated set of multimedia works with a simple, responsive layout

## Live Preview / How to open

You can preview the site locally in several ways.

Option A — Open directly in your browser
- Double-click `index.html` (or open it from your editor). This works for basic viewing but some features (CORS, fetch requests) can behave differently compared to a server.

Option B — Quick local server (recommended)
- If you have Python installed, run this in PowerShell from the project folder:

```powershell
# serve at [http://localhost:8000](https://jugitabada20.github.io/digital-art-exhibit)
python -m http.server 8000
```

- Or use npx http-server (Node.js required):

```powershell
npx http-server . -p 8080
```

Then open http://localhost:8000 (or :8080) in your browser.

## What’s included

```
/ (project root)
  ├─ index.html           # Home page (has the hero section)
  ├─ exhibit.html         # Gallery / exhibit page
  ├─ artist.html          # Artist statement page
  ├─ styles.css           # Central stylesheet
  └─ images/              # All image assets used by the site
```

## How to change the hero or header images

The site uses CSS background images for the hero sections.

- Home hero: Edit `.hero` in `styles.css`. Example:

```css
.hero {
  background-image: linear-gradient(rgba(0,0,0,0.35), rgba(0,0,0,0.35)), url('images/6.jpg');
}
```

- Gallery hero: Edit `.gallery-hero` in `styles.css`:

```css
.gallery-hero {
  background-image: linear-gradient(rgba(0,0,0,0.35), rgba(0,0,0,0.35)), url('images/1.jpg');
}
```

Replace the path with any file inside the `images/` folder.

## Carousel (Gallery) notes

The "Light & Memory" gallery uses a small, dependency-free carousel. Images are stored inline in `exhibit.html` inside the `.carousel-track` element. To add/remove images, edit the `<img>` tags in that container.

The carousel JS is a minimal script at the bottom of `exhibit.html`. If you want features like autoplay, indicators, or touch swipe support, consider using a small library such as Swiper or Siema.

## Styling and layout

- All visual styles are in `styles.css`. The file contains sections for header, hero, carousel, cards, and responsive rules.
- For quick adjustments (overlay darkness, spacing, radius), edit the relevant selectors and refresh the page.

## Accessibility

- Buttons include `aria-label` attributes for screen readers.
- Images should have meaningful `alt` text—replace the empty `alt` attributes in `exhibit.html` with descriptive text for better accessibility.

## Contributing

If you'd like to contribute:
1. Fork the repository
2. Create a branch (`feature/my-change`)
3. Make changes, run a local preview
4. Open a pull request with a clear description of your changes

Small improvements I recommend:
- Add alt text for all gallery images
- Add a keyboard-accessible carousel variant (left/right arrow navigation)
- Add unit or visual tests if you integrate a build system

## License

This repository does not include a license by default. If you want it to be open-source, consider adding an `LICENSE` file. A common choice is the MIT license.

## Contact

If you want changes or help customizing the site (different layout, overlay, autoplay carousel, or deployment), open an issue or reach out to the repository owner.

---

