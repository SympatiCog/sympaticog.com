# SympatiCog.com

Static marketing site for SympatiCog, built in the **Light Signal** design system.
No build step — plain HTML + one stylesheet.

## Files
```
index.html                      Landing page (hero, services, approach, about, contact)
warp-ema-signup.html            Warp EMA SMS signup (with opt-in consent checkbox)
warp-privacy-policy.html        Warp SMS Privacy Policy
warp-terms-and-conditions.html  Warp EMA Terms of Service
styles.css                      Shared Light Signal styles
favicon.svg                     Signal-mark favicon
```

## Deploy to Netlify
1. Push the **contents of this folder** to the repo root (so `index.html` sits at the top level).
2. In Netlify: **Add new site → Import from Git →** pick `SympatiCog/sympaticog.com`.
3. Build command: *(none)* · Publish directory: `/` (repo root).
4. Deploy. Netlify serves clean URLs automatically (`/warp-ema-signup`, etc.).
5. Point the `sympaticog.com` domain at Netlify (Netlify DNS or an ALIAS/A record) and remove it from GoDaddy hosting.

## Forms (Netlify Forms)
Both forms are wired for Netlify Forms — no backend needed:
- `contact` — landing-page contact form
- `warp-ema-signup` — SMS signup, incl. the `sms-consent` checkbox

Netlify auto-detects them on first deploy. Submissions appear under **Site → Forms**.
Set up notification emails there (Netlify → Forms → Settings & notifications).
A honeypot field (`bot-field`) is included for spam; add reCAPTCHA in Netlify if you want more.

## Notes
- The opt-in SMS checkbox is **unchecked by default** and **required** to submit the signup
  (affirmative express consent, TCPA-friendly). Consent is not required to participate in the
  study — that's stated on the page, in the Terms, and in the Privacy Policy.
- Fonts load from Google Fonts (Archivo, JetBrains Mono, Montserrat).
