# WE HELP — You Are Not Alone

A website for **WE HELP**, offering 24/7 text and hotline support, therapy
connections, and a judgment-free space for anyone facing a mental health
struggle.

## Project Links
- **Live website:** (https://kalila-tech.github.io/WEHELP-Website2/)
- **GitHub repository:**  https://github.com/Kalila-Tech/WEHELP-Website2.git

## Project Overview
WE HELP is a mental health support organisation. Its website explains the
support on offer (a 24/7 text line, a 24/7 support hotline, and connections to
professional therapy), shows the community behind it, recommends reading, and
lets visitors get in touch or enquire about volunteering, sponsoring and
partnering.

## Website Goals and Objectives
- Make sure no one has to face a mental health struggle in silence
- Present the text line, hotline and therapy support clearly so people can find help quickly
- Give people a calm, judgment-free first impression of the organisation
- Let visitors volunteer, sponsor, partner or simply get in touch through clear forms

## Key Features and Functionality
- Multi-page website: Home, About, Services, Gallery, Books, Enquiry, Contacts
- Responsive, accessible layout with a skip link, sticky header and a mobile menu
- Header search that finds pages as you type
- FAQ accordion on the Services page
- Gallery with a lightbox (previous, next, close and keyboard support)
- Books page built from data with a live search filter
- Interactive Leaflet map with more than one location on the Contacts page
- Enquiry form with validation and a response based on the enquiry type
- Contact form with validation that compiles the message into an email
- Scroll animations that respect the "reduce motion" setting
- On-page SEO, `robots.txt` and `sitemap.xml`

## Timeline and Milestones
| Milestone                                          | Target               |
|-----------------------------------------------------|----------------------|
| Research, sitemap and folder structure              | Part 1 window        |
| HTML structure for all pages                        | Part 1 window        |
| CSS styling and responsive design                   | Part 2 window        |
| JavaScript functionality, forms and SEO             | Part 3 window        |
| Live deployment and final README                    | End of Part 3 window |

## File Structure

```
├── index.html              # Home
├── about.html              # About
├── services.html           # Services + FAQ accordion
├── gallery.html            # Gallery + lightbox
├── books.html              # Recommended reading (built by js/books.js)
├── enquiry.html            # Enquiry form
├── contacts.html           # Contact details, map and contact form
├── style.css               # External stylesheet, linked from every page
├── robots.txt              # Crawler instructions + sitemap location
├── sitemap.xml             # List of all pages for search engines
├── js/
│   ├── main.js             # Menu, back-to-top, search, accordion, lightbox, animations
│   ├── books.js            # Builds and filters the book cards
│   ├── enquiry.js          # Enquiry form validation and response
│   ├── contact.js          # Contact form validation and email
│   └── map.js              # Leaflet map
├── wehelp-pictures/        # Image assets used in the site icon and gallery
├── README.md               # This file
└── changelog.md            # Detailed change log
```

## How to View

Open `index.html` in a browser, or serve the folder with a local dev server
(e.g. VS Code's Live Server extension) and browse to:

```
http://127.0.0.1:5500/<project-folder>/index.html
```

The pages load Google Fonts (Fraunces + Inter), Font Awesome icons (kit
script), and the Leaflet map library, so an internet connection is needed for
those to load correctly.

## Design System

- **Colour:** soft purple (`#5B3E96` / `#382A5C`) for calm and trust, warm
  coral (`#E8927C` / `#D97B62`) as an accent
- **Type:** Fraunces (serif, headings), Inter (sans-serif, body)
- **Layout:** card-based grids, sticky header and nav, back-to-top button
- **Signature elements:** an animated "breathing" visual on the hero
  section, a swaying hug emoji in the logo, and a skip-link for keyboard
  users

## Sitemap

| Page | File | Purpose |
|---|---|---|
| Home | `index.html` | Hero introduction, mission statement, "What We Provide" list |
| About | `about.html` | Organisation background and mission |
| Services | `services.html` | 24/7 text line, hotline and therapy support cards, plus FAQ |
| Gallery | `gallery.html` | Photos representing the community and support offered |
| Books | `books.html` | Recommended reading on mental health topics |
| Enquiry | `enquiry.html` | Volunteer, sponsor, partner or information enquiries |
| Contacts | `contacts.html` | Hotline/text/email details, emergency note, map and contact form |

## Part 3 Details
Part 3 added JavaScript functionality, search engine optimisation (SEO), and deployment.

### Interactive Elements
- **FAQ accordion (services.html):** four questions that expand and collapse, one open at a time, using `aria-expanded` for screen readers. Code in `js/main.js`.
- **Mobile menu and back-to-top button:** the CSS from Part 2 already styled these; JavaScript now makes them work.
- **Scroll animations:** cards, gallery photos and list items fade in as they scroll into view using the `IntersectionObserver` API. Animations are switched off for visitors who prefer reduced motion.

### Interactive Map (contacts.html)
- Built with the **Leaflet** library and **OpenStreetMap** tiles (`js/map.js`).
- Shows more than one location, each with a popup, and zooms so every marker is visible.

### Gallery with Lightbox (gallery.html)
- Clicking or pressing Enter on a photo opens it larger with its caption.
- Close with the X button, a click on the dark background, or Esc. Previous and next buttons and the arrow keys move between photos.

### Dynamic Content and Search
- **Header search (every page):** typing shows matching pages; Enter opens the first result.
- **Books page (books.html):** the book cards are built by JavaScript from a list of books (`js/books.js`), and a filter box narrows them by title, author or topic. A `<noscript>` copy of the cards is provided if JavaScript is off.

### Enquiry Form (enquiry.html)
- **Controls:** text, email, phone, dropdown (enquiry type), radio buttons (how to contact), date picker, text area with character counter, and a required checkbox.
- **Validation (`js/enquiry.js`):** name at least 2 characters; valid email; South African phone number, required only when a phone call or WhatsApp is chosen; enquiry type chosen; date from today up to 90 days ahead; message 10–500 characters; consent box ticked. Each field shows its own error message.
- **Response:** a valid enquiry shows a response for the chosen type (volunteering, sponsoring, partnership or information) and the chosen contact method and date.
- The form carries a notice that it is not for emergencies and points to the Contacts page.

### Contact Form (contacts.html)
- **Controls:** name, email, optional phone, subject dropdown, and a message box with a live character counter.
- **Validation (`js/contact.js`):** same rules as the enquiry form; message 10–500 characters.
- **Email:** a valid form is compiled into an email (subject and body) with a `mailto:` link, which opens the visitor's email app addressed to the organisation.

### Search Engine Optimisation (SEO)
**On-page**
- Unique `<title>` tags (under 60 characters) and meta descriptions (under 155 characters) on every page.
- Meta keywords per page, with the same terms used in headings and text (for example: mental health support, 24/7 text line, support hotline, therapy support).
- One `<h1>` per page with a logical heading order.
- Descriptive alt text on every gallery image and lazy loading on gallery images.
- Canonical URLs, Open Graph share tags, and a theme colour.
- Internal links between pages with descriptive link text.
- Structured data (JSON-LD, type NGO) on the home page with name, phone, email and area served.
- Mobile-friendly through the viewport tag and the responsive CSS.

**Off-page (planned)**
- Share the site on the organisation's social media pages (Facebook, Instagram, X, LinkedIn).
- Ask mental health directories and partner organisations to link to the site.

**Technical SEO and security**
- `robots.txt` allows crawling and points to the sitemap; `sitemap.xml` lists all seven pages.
- Scripts are loaded with `defer` for faster page loading.
- Integrity (SRI) hashes on the Leaflet files so a tampered file is rejected.
- Form output is written with `textContent` rather than `innerHTML` so typed text is never run as HTML.

### Deployment
- Deployed on **GitHub Pages**: [add your live website link here]

## Changelog

All edits made to the repository are logged below, most recent first.
Each entry describes what changed and why. The same entries are kept in `changelog.md`.

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
- Updated this README with Part 3 details, changelog and references

## AI Usage Declaration
This module's assessment is open book and the use of AI was permitted. I used Claude (an AI assistant) to help me plan and write the Part 3 JavaScript, SEO tags and README text. I tested the code, adjusted it to my project, and deployed the site myself.

## References
- Agafonkin, V. (2026). Leaflet: an open-source JavaScript library for interactive maps. Available at: https://leafletjs.com [Accessed: 2 November 2026].
- OpenStreetMap contributors (2026). OpenStreetMap. Available at: https://www.openstreetmap.org [Accessed: 2 November 2026].
- Font Awesome (2026). Font Awesome icons. Available at: https://fontawesome.com [Accessed: 2 November 2026].
- Google (2026). Google Fonts: Fraunces and Inter. Available at: https://fonts.google.com [Accessed: 2 November 2026].
- MDN Web Docs (2026). Intersection Observer API. Available at: https://developer.mozilla.org/en-US/docs/Web/API/Intersection_Observer_API [Accessed: 2 November 2026].
- MDN Web Docs (2026). Client-side form validation. Available at: https://developer.mozilla.org/en-US/docs/Learn_web_development/Extensions/Forms/Form_validation [Accessed: 2 November 2026].
- MDN Web Docs (2026). ARIA: aria-expanded attribute. Available at: https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Reference/Attributes/aria-expanded [Accessed: 2 November 2026].
- Google (2026). Search Engine Optimization (SEO) Starter Guide. Available at: https://developers.google.com/search/docs/fundamentals/seo-starter-guide [Accessed: 2 November 2026].
- Sitemaps.org (2026). Sitemaps XML format. Available at: https://www.sitemaps.org/protocol.html [Accessed: 2 November 2026].
- Schema.org (2026). NGO. Available at: https://schema.org/NGO [Accessed: 2 November 2026].
- GitHub Pages (2026). Documentation. Available at: https://pages.github.com [Accessed: 2 November 2026].
- Anthropic (2026). Claude [Large language model]. Available at: https://claude.ai [Accessed: 2 November 2026].
- [Add the source of the photos in `wehelp-pictures/`, for example the stock photo site and photographer.]
