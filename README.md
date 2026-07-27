# legal-porygon

Static legal pages for privately operated applications.

Third-party providers generally require a registered application to expose its terms of service
and privacy policy at publicly reachable addresses. This repository publishes them.

## Layout

One directory per application, so further applications can be added without touching existing
ones:

```
index.html              directory of all applications
style.css               shared stylesheet
actual/                 Enable Banking application (bank sync into Actual Budget)
  index.html
  privacy.html
  terms.html
```

## Adding an application

Create a directory named after the application, copy the three files from `actual/`,
adapt the wording, and add an entry to the root `index.html`. Pages inside an application
directory reference the stylesheet as `../style.css`.

## Notes

No build step, no dependencies. Internal links are relative, so the site works both when served
from a sub-path (GitHub Pages) and from the root of a domain (Cloudflare Pages).
