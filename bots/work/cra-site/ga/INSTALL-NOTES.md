# GA4 install notes — citizensratification.com

**Status (2026-09-12):** Jeff exact yes to find Measurement ID + install. Waiting on Work for real `G-…` ID and upload path. **Do not edit live HTML until ID + path + Governor named slice.**

## Snippet

Source: `/workspace/cra-site/ga/gtag-snippet.html`

Replace every `G-XXXXXXXXXX` with the Measurement ID Work sends.

## Where to insert

Inside `<head>`, after charset + viewport meta, before large HTML comment blocks / `<style>`.

## Apex root pages to tag (site document root)

| Live name | Local draft if any |
|---|---|
| `index.html` | `/workspace/homepage.html` (or live fetch) |
| `01-support.html` | `/workspace/01-support.html` |
| `02-cra.html` | (live only unless local copy) |
| `03-crb.html` | (live only unless local copy) |
| `04-cri.html` | `/workspace/04-cri.html` |
| `05-how.html` | (live only unless local copy) |
| `06-rebuttals.html` | (live only unless local copy) |
| `07-documents.html` | `/workspace/07-documents.html` |
| `08-about.html` | `/workspace/08-about.html` |
| `privacy-policy.html` | `/workspace/cra-site/privacy-policy.html` |
| `terms-and-conditions.html` | `/workspace/cra-site/terms-and-conditions.html` |

Skip reserved/empty pages with no real HTML. Prefer tagging every public HTML page in site root that visitors hit.

## Gates before live change

1. Work sends Measurement ID
2. Work confirms upload path (Jeff self-upload vs CRA Web / iCloud folder)
3. Governor named slice grant (BM coordinates; Governor grants)
4. Then fill ID → patch pages → upload only those files

## After live

Verify homepage HTML contains `G-…` and `googletagmanager.com/gtag/js`. Tell Work. Social keeps UTM template on apex links.
