# Inkarnation
**Where Lives Are Changed Through Christ**

A free ministry Progressive Web App for incarcerated people, families and volunteers.

## Included
- Home page with featured yoga illustrations
- 365 unique daily devotionals and prayers (12 Scripture themes rotate through the calendar)
- Bible studies, a complete 365-day Genesis-to-Revelation Bible reading plan, Letters of Hope, family support and volunteer resources
- 16 gentle yoga poses with individual matching illustrations
- Box breathing and a five-minute guided Christian meditation
- Prayer request form with an optional name
- Ministry contact: Inkarnationministry@gmail.com

## Prayer email setup (required before submissions work)
The prayer form is designed for **Netlify Functions + Resend**. It does not send requests until the ministry configures the backend.

1. Create a free Netlify account and deploy this folder as a Netlify site (the included `netlify.toml` configures the function folder).
2. Create a Resend account, verify a sending domain, and create an API key.
3. In Netlify: **Site configuration → Environment variables**, add:
   - `RESEND_API_KEY` = your Resend API key
   - `PRAYER_FROM_EMAIL` = a sender address on the domain you verified with Resend
4. Redeploy the site, then submit a test request and confirm it arrives at Inkarnationministry@gmail.com.
5. Do not put the API key in `index.html`, GitHub, or any public file.

The function validates the request, limits message length, includes a honeypot field, and sends email server-side. This starter does **not** include persistent rate limiting, CAPTCHA, or encrypted case-management storage. Email is not a confidential or encrypted care channel. Do not request sensitive personal information; publish a privacy notice and retention policy before public launch. Consider adding CAPTCHA and durable rate limiting before promoting the form widely.

## Publish
### Netlify (recommended for prayer form)
Deploy the project folder to Netlify. The serverless function is required for prayer email.

### GitHub Pages (static app only)
GitHub Pages can host the static app, but it cannot run the included prayer-email function. If hosted only on GitHub Pages, the prayer form will display a service-not-configured error. For working submissions, use Netlify or another host that supports the included serverless endpoint.

## Important limitations
This is a web app/PWA, not a native app-store app. No login, synced admin editor, payment processor, or donation account is connected. Devotionals use 12 Scripture themes that rotate across 365 days, not 365 unique passages. Wellness content is general information, not medical advice. Follow facility rules.


## Prayer requests
The Prayer tab instructs visitors to email Inkarnationministry@gmail.com directly. Visitors can tap the address to open their email app. Do not send emergencies or highly sensitive information.

## Bible reading and devotionals
The Devotionals tab contains 365 distinct day entries, each with a theme, Scripture reference, reflection, practical response and prayer. The Bible Study & Reading Plan tab includes a consecutive chapter schedule through all 1,189 chapters of the 66-book Protestant Bible over 365 days.
