# Changelog

All notable changes to the **WE HELP** website are documented in this file.

Entries are listed most recent first. Each entry describes *what*
changed and *why*, in enough detail that a reviewer can understand the edit
without opening a diff.

Format for each entry:

```
**YYYY-MM-DD**
- Description of the change and the reasoning behind it.
- Another change made on the same date, as its own bullet.
```

---

**2026-11-02 — Part 3**

*Corrections to earlier work (no written Part 2 feedback was received, so these come from my own review)*
- Fixed the broken gallery image path on `gallery.html` (`assets/images/gallery-04.jpg` did not exist; now `wehelp-pictures/gallery-1.jpg`)
- Removed the deleted `home.html` from the menus and pointed "Home" to `index.html`
- Turned `index.html` into the Home page only, so its About, Services, Gallery, Books and Contacts sections no longer duplicate the separate pages
- Gave every page a single `<h1>` and updated `style.css` selectors to match
- Replaced the identical meta description on every page with a unique one

*Forms*
- Added `enquiry.html` with a validated enquiry form and a response shown for the enquiry type
- Added `js/enquiry.js` (validation, date limits, character counter, response)
- Rebuilt the contact form in `contacts.html` with phone and subject fields, error messages and a character counter
- Added `js/contact.js` (validation and email compiling with `mailto:`)

*Interactive features*
- Added `js/main.js`: mobile menu, back-to-top button, header search, FAQ accordion, gallery lightbox and scroll animations
- Added an FAQ accordion to `services.html`
- Added the lightbox to `gallery.html`
- Added `js/books.js` and rebuilt `books.html` so the cards come from data, with a filter box and a `<noscript>` fallback
- Added the Leaflet map (`js/map.js`) with more than one location to `contacts.html`

*Styling*
- Added Part 3 styles to `style.css`: in-text links, current-page menu highlight, search results, form errors, select/radio/checkbox, enquiry page, FAQ accordion, map, book filter, lightbox and animations, with mobile adjustments

*SEO and deployment*
- Rewrote the `<head>` of all pages: unique title, description, keywords, canonical URL, Open Graph tags and theme colour
- Added NGO structured data (JSON-LD) to `index.html`
- Added internal links between pages and `defer` on scripts
- Added integrity (SRI) attributes to the Leaflet files
- Created `robots.txt` and `sitemap.xml`
- Added the Enquiry link to the menu on every page
- Updated `README.md` with Part 3 details, changelog and references
