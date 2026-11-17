# bazinger — mobile app landing page

A responsive one-page landing for a made-up mobile app, built as practice for an HTML5 & CSS3 course
(2018). HTML and CSS with a small jQuery image slider and a click-to-play YouTube video.

## What's on the page

- Transparent header over a full-width hero slider (jQuery + [Unslider](https://github.com/idiot/unslider) 2.0.3)
- Features: three icon cards
- Gallery: four photos with captions
- Video section: the play button loads the YouTube player only when clicked
- "Download now" call to action
- Contact form over an embedded Google Map

The menu links scroll to these sections.

## Run it

Open `index.html` in a browser, or serve the folder locally:

```bash
python3 -m http.server 8000
# → http://localhost:8000
```

## Structure

```
.
├── index.html
├── style.css              # Page styles
├── css/
│   ├── unslider.css       # Slider base styles
│   └── unslider-dots.css  # Slider dots in the page's colours
├── js/
│   └── unslider-min.js    # Unslider 2.0.3
└── images/
```

jQuery 3.7.1 is loaded from the official CDN with a Subresource Integrity hash.
To change the video, set `YOUTUBE_VIDEO_ID` in the script at the bottom of `index.html`.

## What it practices

- Semantic HTML5 with in-page navigation (`#features`, `#gallery`, `#video`, `#download`, `#contact`)
- CSS Grid for the cards and gallery, flexbox for the header and form
- Responsive breakpoints at 1133 px, 900 px, 660 px and 525 px: on phones the slide text moves
  under the image and the contact form under the map
- Accessible forms and buttons, visible keyboard focus
- Lazy video embed via `youtube-nocookie.com`

## Notes

- "bazinger" is a made-up brand; "Download" links and the form are placeholders, not wired to anything.
- Gallery captions are Nike product descriptions and the photos are third-party; this is a
  non-commercial learning project, not affiliated with any brand.

Made by [Ilya Bielov](https://www.facebook.com/MrBiela).
