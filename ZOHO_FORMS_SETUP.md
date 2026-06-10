# Zoho Forms setup for DecideWise AI

The DecideWise AI website is now connected to Zoho Forms for lead capture.

## Connected forms

The following Zoho Form public/permalink URLs are configured inside `index.html`:

```js
const ZOHO_FORMS = {
  'early-access': 'https://forms.zohopublic.com/rkohbk619rkgm1/form/DecideWiseAIEarlyAccessRequest/formperma/LBDgBfaEB6Qtia0kJGZxP0Ll16FMryO1j1rw79ZtpPI',
  demo: 'https://forms.zohopublic.com/rkohbk619rkgm1/form/DecideWiseAIDemoRequest/formperma/43gMk-cqFwWcTrkUR3WGXJMKMsvK4mg6TqLFGS96zl4',
  contact: 'https://forms.zohopublic.com/rkohbk619rkgm1/form/DecideWiseAIContactFounder/formperma/gkuhRPozVbz0Qp0gdrFaE7VMTE-H8X7cTl9pZfg14_Q'
};
```

## Button behavior

- **Request Early Access** opens the early-access Zoho Form inside the website modal.
- **Book an Early Demo** opens the demo-request Zoho Form inside the website modal.
- **Contact Founder** opens the founder-contact Zoho Form inside the website modal.
- Each modal also includes a direct link to open the secure Zoho Form in a new tab if iframe embedding is blocked by the browser.
- The mobile number action copies the number instead of auto-opening the phone dialer, preventing blocked-content browser errors.

## Notifications

In Zoho Forms, keep email notifications enabled for:

```text
founder@decidewiseai.me
```

## GitHub Pages note

GitHub Pages is static hosting. Zoho Forms handles the actual form submissions externally, so no backend server is required for the current landing page.
