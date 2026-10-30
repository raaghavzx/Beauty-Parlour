# Honey Beauty Parlour & Makeup Studio — Website

Multi-page, fully animated, responsive website. Pure HTML, CSS and JavaScript:
no frameworks, no build step, no server needed.

## Folder structure

```
honey-beauty-parlour/
├── index.html        Home (hero, about, stats, services, portfolio, reviews, process, CTA)
├── about.html        Story, team, why choose us
├── services.html     Services, bridal packages, service details, FAQ
├── gallery.html      Filterable portfolio with full-screen lightbox
├── reviews.html      Google rating breakdown + client quotes
├── contact.html      Slot booking (WhatsApp), contact info, Google Map, live open/closed status
├── 404.html          Not-found page
├── css/
│   ├── base.css         colours, fonts, buttons, grid
│   ├── layout.css       preloader, header, mobile menu, footer, floating buttons
│   ├── components.css   every section/component
│   └── animations.css   keyframes + scroll-reveal classes
├── js/
│   ├── config.js        ★ business details (phone, WhatsApp, timings, services)
│   ├── components.js    header, footer, floating buttons shared by all pages
│   ├── main.js          menu, sticky header, FAQ, back-to-top
│   ├── animations.js    scroll reveal, counters, parallax, cursor, tilt
│   ├── gallery.js       filters + lightbox
│   ├── slider.js        testimonial slider
│   ├── booking.js       slot booking → WhatsApp
│   └── contact.js       open-now badge, hours, Google Map embed
└── img/
    ├── hero-bride.jpg
    ├── gallery/        portfolio photos
    └── brand/          logo + favicon
```

## Editing content

- **Phone, WhatsApp, address, timings, services list:** edit `js/config.js` only. All pages update automatically.
- **Photos:** replace files in `img/gallery/` keeping the same names, or add new `<figure class="gallery__item">` blocks in `gallery.html` (use `data-cat="bridal"` or `data-cat="studio"`).
- **Colours / fonts:** change the variables at the top of `css/base.css`.

## How slot booking works

1. Customer picks service, date (today up to 180 days ahead) and a 1-hour slot between 10 AM and 7 PM.
   Past times for today are disabled automatically.
2. On submit, WhatsApp opens with a ready booking message addressed to the studio number in `config.js`.
3. The studio confirms by replying on WhatsApp.

## Going live (free options)

- **Netlify:** app.netlify.com → *Add new site → Deploy manually* → drag this whole folder. Live in seconds.
- **GitHub Pages:** push the folder to a repository → *Settings → Pages → Deploy from branch*.
- **Any cPanel hosting:** upload the folder contents into `public_html`.

Connect a custom domain (for example `honeybeautykota.in`) from the hosting dashboard.

## Browser support
Latest Chrome, Edge, Firefox, Safari, Samsung Internet; Android and iPhone.
Animations automatically calm down for visitors who enable "Reduce motion".
