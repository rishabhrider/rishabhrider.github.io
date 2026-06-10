# Zoho Forms setup for DecideWise AI

The website is ready for Zoho Forms, but the real Zoho form URLs must be created inside your Zoho account and pasted into `index.html`.

## Recommended forms to create

Create these three forms in Zoho Forms:

1. **DecideWise AI — Early Access Request**
   - Name
   - Email
   - Organization / Team
   - Primary use case
   - Message / What do you want to test?

2. **DecideWise AI — Demo Request**
   - Name
   - Email
   - Organization / Team
   - Primary use case
   - Preferred demo date/time
   - Message

3. **DecideWise AI — Contact Founder**
   - Name
   - Email
   - Organization / Team
   - Reason for contact
   - Message

Set email notifications to:

```text
founder@decidewiseai.me
```

## Where to paste Zoho form links

Open `index.html` and find this block:

```js
const ZOHO_FORMS = {
  'early-access': '',
  demo: '',
  contact: ''
};
```

Replace it with your Zoho public/permalink URLs:

```js
const ZOHO_FORMS = {
  'early-access': 'https://forms.zohopublic.in/YOUR_ORG/form/EarlyAccess/formperma/YOUR_ID',
  demo: 'https://forms.zohopublic.in/YOUR_ORG/form/DemoRequest/formperma/YOUR_ID',
  contact: 'https://forms.zohopublic.in/YOUR_ORG/form/ContactFounder/formperma/YOUR_ID'
};
```

## Current fallback behavior

Until you paste the Zoho URLs, the website opens a professional modal form and prepares an email request to `founder@decidewiseai.me`. This prevents broken buttons and keeps the site usable.

## Button behavior

- **Request Early Access** opens the early-access form/modal.
- **Book an Early Demo** opens the demo form/modal.
- **Contact Founder** opens the contact form/modal.
- The site no longer auto-opens the phone dialer, so it avoids blocked-content errors.
