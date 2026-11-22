# Pihulka Check — public pages

The Pihulka Check privacy policy and support page, in Ukrainian and English. GitHub Pages builds it
straight from `main` with Jekyll; there is no build step of our own.

| Page | Source |
| --- | --- |
| `/uk/privacy/` | `uk/privacy.md` |
| `/en/privacy/` | `en/privacy.md` |
| `/uk/support/` | `uk/support.md` |
| `/en/support/` | `en/support.md` |

Links between pages are relative, so the site works on `<owner>.github.io/<repo>/`
now and on our own domain later without changes.

## Changing the policy

- Both languages change together, section for section.
- The version is the date under the heading. It is written once, in
  `_config.yml` (`privacy_version`, and `privacy_version_date` for the words in
  each language); the pages read it from there. The app sends it as
  `user_consent.version` when someone registers, so a new version means a new
  date in `_config.yml` and the same date in the app.
- Before changing a published version, copy it to `uk/privacy/<old version>.md`
  (and `en/…`) with `permalink: /uk/privacy/<old version>/`. A consent recorded
  against that version has to stay provable.
- Section 5 lists every service that receives data. When the backend's services
  change, section 5 changes with them.
- A change that touches health data needs consent again in the app.

## The support address

`support_email` in `_config.yml`; every page and the footer read it from there.

## Changing the support page

The FAQ describes how the app behaves, so it changes with the app: button and
section names, repeat defaults, the reset-code lifetime. Both languages together.

## Before a release: what the pages promise

The pages describe the app as it is released, and some of it is still being
built. Before each release, check every line below against the app; a promise
the release does not keep is softened here first (and, in the policy, under a
new version).

| The pages say | Where | In the code |
| --- | --- | --- |
| An unanswered reminder repeats once more, an hour later, by default | support, "How to stop the repeats" | `DEFAULT_REMINDER_SETTINGS` in pihulka-check-be `src/types/reminder-settings.ts` and pihulka-check-mobile `src/libs/settings/settings-store.ts` |
| "Account" → "Delete account" removes the data from the server | support; privacy, summary and section 8 | Backend: `DELETE /users/me`. App: not built yet |
| Signing in brings medications, schedules and history back; sync between phones | support; privacy, summary | Backend: `/sync/snapshot`. App: not built yet |
| Signing out erases the data from the phone | privacy, section 4 | App: `signOut` in pihulka-check-mobile `src/libs/authentication/session.ts` clears medications, settings and the dose log |
| After signing out, the data stays on the server and comes back on sign-in | privacy, section 4 | App: not built yet (no sync) |
| History older than 90 days loads from the server | privacy, section 4 | App: not built yet |
| The reset code is valid for 15 minutes; sessions last 30 days | support; privacy, section 6 | pihulka-check-be `src/auth` |

## Preview locally

```bash
gem install jekyll kramdown-parser-gfm webrick
jekyll serve   # http://localhost:4000
```
