# Quick chat — original design with automatic URL opening

Deploy index.html and vercel.json at your Vercel project root.
Other hosts need an equivalent fallback rewrite to index.html.

Valid phone-number paths fill the country/number and immediately attempt
whatsapp://send?phone=NUMBER. If the page stays visible, after 2.5 seconds
it navigates to https://web.whatsapp.com/send?phone=NUMBER.
If the page becomes hidden or unloads, the fallback is cancelled.
The Open WhatsApp button retries the same flow after a user gesture.
Editing the number or opening the country picker cancels a pending redirect.

Browsers cannot reliably detect installation. They may block automatic app
launches, show a confirmation, or show an unsupported-protocol warning.
Visibility is a heuristic: switching tabs can also cancel the fallback.
The visible WhatsApp Web link is always available after an opening attempt.
WhatsApp Web availability on mobile is controlled by WhatsApp.

URL numbers without a country code default to Pakistan. Explicit + or 00
country prefixes are supported. Spaces, dots, hyphens, parentheses and
Arabic/Persian digits are supported. Invalid paths stay in the input with
an error and never redirect. Validation uses phone-number rules, not just
digit count, and cannot determine whether a number has a WhatsApp account.
The root homepage does not auto-open anything.

Examples: /0335%202522%20522, /3352522522, /+92%203352522522,
/+923352522522, /00923352522522, /923352522522.


## Valid URL opening screen

The original white/green design is restored. A valid URL phone number replaces
the input form with a centered opening screen: existing WhatsApp logo, animated
ellipsis, normalized international number, WhatsApp Web link, and original
branding. Reduced-motion preferences disable the dots' animation. Invalid URL
numbers retain the original editable form and inline error. The homepage also
retains the original form. App launch and 2.5-second Web fallback are unchanged.
