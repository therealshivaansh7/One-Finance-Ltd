# One Finance Ltd — Arthathon 2026

## Project overview
One Finance Ltd is a browser-based small-business finance dashboard concept. It brings together a finance overview, GST-related tools, loan and cash-flow planning interfaces, an E-Way Bill workflow, market-information displays, and an AI CFO assistant experience.

This repository contains a static HTML frontend. It is a prototype/demo and should not be represented as a production banking, tax-filing, or regulated financial service.


## Problem statement

Small businesses in India manage GST, cash flow, loans and market information across separate tools, which is slow and confusing. One Finance Ltd brings these into one dashboard, with an AI CFO assistant to help owners understand their numbers.

## Features present in the frontend

- Responsive single-page interface with dark/light themes and visual themes.
- Business health-score and finance dashboard displays.
- GST calculator and GST/IRN-related interface elements.
- Loan/EMI and cash-flow planning interface.
- E-Way Bill and foreign-exchange interface.
- Market-intelligence and chart/visualization sections.
- Gemini-powered text assistant, voice assistant, text-to-speech, and image-generation code paths.
- Firebase Authentication code paths (email/password, Google sign-in, phone sign-in, and anonymous sign-in), conditional on Firebase configuration being supplied.

**Integration boundary:** The current HTML includes demo figures and client-side interface logic. It does not contain credentials or a configured backend for live GSTN/NIC e-invoice or E-Way Bill filing, live bank connectivity, real payment processing, or real financial trades. Do not describe those as live integrations unless you separately implement and test them.


## How to run

1. Clone the repo:
## Features present in the frontend
- Responsive single-page interface with dark/light themes and visual themes.
- Business health-score and finance dashboard displays.
- GST calculator and GST/IRN-related interface elements.
- Loan/EMI and cash-flow planning interface.
- E-Way Bill and foreign-exchange interface.
- Market-intelligence and chart/visualization sections.
- Gemini-powered text assistant, voice assistant, text-to-speech, and image-generation code paths.
- Firebase Authentication code paths (email/password, Google sign-in, phone sign-in, and anonymous sign-in), conditional on Firebase configuration being supplied.

**Integration boundary:** The current HTML includes demo figures and client-side interface logic. It does not contain credentials or a configured backend for live GSTN/NIC e-invoice or E-Way Bill filing, live bank connectivity, real payment processing, or real financial trades. Do not describe those as live integrations unless you separately implement and test them.

## Technology and external services
- HTML5, CSS, and JavaScript (single-page frontend).
- Tailwind CSS CDN.
- Google Fonts (Plus Jakarta Sans, Outfit, and Fira Code).
- Google GenAI JavaScript SDK (`@google/genai`) loaded from `esm.sh`.
- Google Gemini API model identifiers referenced in the source:
  - `gemini-3-flash-preview` — text generation / Google Search grounding.
  - `gemini-3.1-flash-live-preview` — live voice assistant.
  - `gemini-2.5-flash-preview-tts` — text-to-speech.
  - `gemini-3.1-flash-image` — image-generation request path.
- Firebase JavaScript SDK v11.6.1 (Firebase Authentication), initialized only when a runtime `__firebase_config` value is available.
- Unsplash and placehold.co image assets/placeholders.

Model availability and API behavior can change. Verify model access in your own Google AI Studio / Google Cloud project before the demo.

## API keys and configuration
### Gemini
The interface accepts a Gemini API key at runtime. No real key is included in this repository. For a public demo, use a restricted key with appropriate API restrictions and quotas. A key entered into browser JavaScript can be inspected by visitors; this is not a secure production architecture. For production, route Gemini requests through a server-side function and keep the key in server-side environment variables.

Do not commit API keys, passwords, bank details, PAN numbers, UPI IDs, or private user data.

### Firebase
The source expects Firebase configuration to be injected at runtime as `__firebase_config`. This repository does not include a Firebase project configuration. To enable authentication, create/configure a Firebase project, enable the required sign-in providers, and provide the configuration through a secure deployment/runtime setup. Also configure authorized domains for your Netlify site. Without this setup, Firebase authentication features may not work; the app may fall back to its demo/session behavior.

## Run locally
1. Download or clone this repository.
2. Open `index.html` in a modern browser.
3. For module imports and browser APIs, it is preferable to serve the folder through a local static server rather than opening the file directly. For example, with Python installed:
   `python -m http.server 8000`
4. Visit `http://localhost:8000`.

## Deploy to Netlify
1. Upload the extracted project folder to Netlify Drop, or connect this GitHub repository to Netlify.
2. Build command: leave blank.
3. Publish directory: `.`

The `netlify.toml` file sets the static publish directory.

## Demo video checklist
- Show the deployed app loading.
- Demonstrate features that actually work in the browser.
- Show the AI assistant only after configuring and testing your own Gemini API key.
- Explain which figures are sample/demo values.
- Do not show real personal, banking, tax, or payment credentials.
- Keep the YouTube video public or unlisted and under five minutes, as required by Arthathon.

## Limitations and responsible-use note
This is a prototype frontend. It does not itself establish a connection to official GSTN/NIC systems, banks, payment rails, or live market-data providers. Financial figures and status indicators shown in the UI may be sample/demo values. Do not use it to file taxes, move money, execute trades, or make lending decisions.

## Arthathon 2026
Prepared as a project submission package. Add your team member details and final deployed URL before submission.

Future Enhancements

- Integration with official GST and banking APIs.
- Real-time financial data synchronization.
- Advanced AI-powered financial insights and recommendations.
- Automated invoice generation and management.
- Enhanced security with encrypted data storage.
- Multi-user support with role-based access control.
- Advanced financial analytics and customizable reports.
- Mobile application support for better accessibility.

- Target Users

One Finance is designed for:

- Small business owners and entrepreneurs.
- Startups and independent business operators.
- Accountants and financial managers.
- Businesses looking to simplify financial management.

- 

