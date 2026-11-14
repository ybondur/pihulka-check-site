# Pihulka Check — public pages

The Pihulka Check privacy policy, in Ukrainian and English. GitHub Pages builds it
straight from `main` with Jekyll; there is no build step of our own.

| Page | Source |
| --- | --- |
| `/uk/privacy/` | `uk/privacy.md` |
| `/en/privacy/` | `en/privacy.md` |

Links between pages are relative, so the site works on `<owner>.github.io/<repo>/`
now and on our own domain later without changes.

## Changing the policy

- Both languages change together, section for section.
- The version is the date under the heading. The app sends it as
  `user_consent.version` when someone registers, so a new version means a new date
  here and the same date in the app.
- Before changing a published version, copy it to `uk/privacy/<old version>.md`
  (and `en/…`) with `permalink: /uk/privacy/<old version>/`. A consent recorded
  against that version has to stay provable.
- Section 5 lists every service that receives data. When the backend's services
  change, section 5 changes with them.
- A change that touches health data needs consent again in the app.

## Preview locally

```bash
gem install jekyll kramdown-parser-gfm webrick
jekyll serve   # http://localhost:4000
```
