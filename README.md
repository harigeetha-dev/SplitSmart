# SplitSmart

Split a restaurant bill fairly and collect payments with PayPal.

Upload a photo of the bill and AI reads the items. Type plain-language rules
like "Priya is vegetarian, Ravi did not drink water" and AI decides who shares
which item. Then create a PayPal payment link for each person.

## How it uses PayPal
PayPal Orders API (sandbox): one checkout link per person for their share,
and payment capture after approval.

## How it uses AI
Gemini reads the bill photo into items and prices, and applies the group's
rules to decide who shares each item. A person always reviews the ticked
boxes before any payment link is created.

## Run it yourself
1. Install Node.js 20 or newer.
2. Copy `.env.example` to `.env` and fill in your own PayPal sandbox keys
   (developer.paypal.com) and a Gemini API key (aistudio.google.com).
3. Run `npm install`, then `node server.js`.
4. Open http://localhost:3000

Use a PayPal sandbox Personal account to pay. Never use real money.

## License
MIT