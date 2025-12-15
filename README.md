# mohiuddin-khan-shiam.github.io

This repository hosts my personal website:

https://mohiuddin-khan-shiam.github.io/

## Tech

- **Jekyll** (GitHub Pages compatible)
- **Minimal Mistakes / AcademicPages**-style structure (collections + archive pages)

## Where to update content

- **Home page**: `index.html`
- **Pages**: `_pages/`
- **Navigation**: `_data/navigation.yml`
- **Blog posts**: `_posts/`
- **Projects**: `_portfolio/`
- **Publications**: `_publications/`
- **Certifications**: `_certifications/`
- **Open Source contributions**: `_open_source/`
- **CV PDF**: `files/cv.pdf`
- **Profile photo**: `images/profile.jpg`

## Key pages

- **Open Source**: `_pages/open-source.md` (renders entries from `_open_source/`)
- **Certifications**: `_pages/certifications.html` (renders entries from `_certifications/`)

## Local development

1. Install Ruby + Bundler.
2. Install gems:

   ```bash
   bundle install
   ```

3. Run the site:

   ```bash
   bundle exec jekyll serve
   ```

4. Open:

   http://127.0.0.1:4000/

## Optional: rebuild JS assets

If you edit `assets/js/` and want to regenerate `assets/js/main.min.js`:

```bash
npm install
npm run build:js
```
