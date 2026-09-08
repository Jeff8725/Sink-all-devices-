# Upload notes — citizensratification.com SMS compliance pages

**Do not publish from this workspace.** These files are upload-ready drafts only. HTTPS must be fixed on GoDaddy (AutoSSL) before Telnyx will treat the URLs as live compliant pages. Jeff enables SSL / completes portal steps when ready. Do not contact Jeff from the bot for this upload.

## Files to upload (site root)

| Local path | Destination on GoDaddy (public_html / site root) |
|---|---|
| `/workspace/cra-site/privacy-policy.html` | `privacy-policy.html` |
| `/workspace/cra-site/terms-and-conditions.html` | `terms-and-conditions.html` |

Final public URLs (after SSL works):

- `https://citizensratification.com/privacy-policy.html`
- `https://citizensratification.com/terms-and-conditions.html`

(Also acceptable if the live site uses `www.`; prefer one canonical host and redirect the other.)

## GoDaddy steps (exact)

### A. Enable HTTPS (AutoSSL) — required before Telnyx verification

1. Sign in to GoDaddy → **My Products**.
2. Find **Web Hosting** for citizensratification.com → **Manage**.
3. Open **cPanel** (or the hosting control panel used for this site).
4. Under **Security**, open **SSL/TLS Status** (or **Manage SSL sites** / AutoSSL).
5. Select the domain `citizensratification.com` (and `www` if listed).
6. Run **Run AutoSSL** / **Install Certificate**. Wait until status shows Active / Valid (not Expired or None).
7. If AutoSSL fails: confirm the domain’s A/CNAME records point at this hosting account, then retry. Do not leave the site on HTTP-only for Telnyx campaign links.

### B. Upload the two HTML files to site root

1. In cPanel, open **File Manager**.
2. Go to the site document root (usually `public_html` for the primary domain, or the folder mapped to citizensratification.com).
3. Confirm existing pages such as `index.html` and `08-about.html` are in this same folder (same pattern as current hand-coded static site).
4. **Upload** (or drag-and-drop):
   - `privacy-policy.html`
   - `terms-and-conditions.html`
5. Overwrite only if older stubs with those exact names already exist. Do not rename to `sms-privacy.html` — Telnyx and public links should use the names above.
6. Set permissions readable by the web server (typical: files `644`).

### C. Verify in a browser (HTTPS)

1. Open a private/incognito window.
2. Visit:
   - `https://citizensratification.com/privacy-policy.html`
   - `https://citizensratification.com/terms-and-conditions.html`
3. Confirm:
   - Padlock / HTTPS with no certificate warning
   - Page title and body load (navy header, Citizens Ratification branding)
   - Carrier language visible: program name **Citizens Ratification Inc.**; **STOP** / **HELP**; **message frequency may vary**; **message and data rates may apply**; **no mobile information shared with third parties for marketing**
   - Corporate contact shows **CEO Jeff Gunson**, phone (903) 646-1735, JeffGunson@hotmail.com
   - Cross-links between Privacy and Terms work
4. If HTTP redirects to HTTPS, good. If HTTPS fails, finish AutoSSL before submitting URLs to Telnyx.

Optional: from the About page or footer, add links to these two files later (not required for this upload package).

### D. Telnyx 10DLC / campaign fields (after HTTPS verified)

In Telnyx (Messaging → 10DLC / campaign for the CRI brand), paste:

| Field | Value |
|---|---|
| Privacy Policy URL | `https://citizensratification.com/privacy-policy.html` |
| Terms and Conditions URL | `https://citizensratification.com/terms-and-conditions.html` |
| Program / brand name | Citizens Ratification Inc. |
| Website | `https://citizensratification.com` |
| Support / contact | CEO Jeff Gunson · (903) 646-1735 · JeffGunson@hotmail.com |

Also ensure campaign description, sample messages, and opt-in flow match these pages (include brand name, STOP, HELP, and msg & data rates language in samples as Telnyx/TCR require).

Do **not** cancel Twilio or send a Telnyx test until Jeff explicitly says yes to that exact send (existing Work bot rule).

## Content checklist (already in these HTML files)

- [x] Program name: Citizens Ratification Inc.
- [x] CEO Jeff Gunson as corporate contact (locked CEO title)
- [x] STOP to opt out; HELP for help
- [x] Message frequency may vary
- [x] Message and data rates may apply
- [x] No sharing of mobile opt-in / mobile information with third parties for marketing or promotional purposes
- [x] Self-contained static HTML (inline CSS; matches CRA navy/gold header/nav/footer pattern from `08-about.html`)
- [x] No publish / no GoDaddy login / no Jeff contact from this prep task

## Source notes

- Short prior drafts at `/workspace/hub-clone/docs/sms-privacy.html` and `sms-terms.html` were **Jeff household** stubs — **not** used as CRA copy.
- Layout matched from local `/workspace/08-about.html` and live fetch of `http://citizensratification.com/08-about.html`.
