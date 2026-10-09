# URL phone autofill

Replace index.html and add vercel.json in your deployment root, then redeploy.
The Vercel rewrite serves the app at phone-number paths. If you use another
host, configure its equivalent fallback to index.html.

Examples (all produce +923352522522):
- /0335%202522%20522
- /3352522522
- /+92%203352522522
- /+923352522522
- /923352522522
- /0092-335-2522522

Spaces, hyphens, parentheses, dots, URL encoding, and Arabic/Persian digits
are supported. Local URL numbers default to Pakistan. For other countries,
use an explicit international country code (+ or 00) to avoid ambiguity.
The country selector and number field are filled automatically; the user
still clicks Open WhatsApp. Invalid numbers cannot launch a chat.
The homepage retains its existing behavior and design.
