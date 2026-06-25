# St. Josephine Bakhita – OBs & OGs Leadership Election Portal

A single-page, static HTML app for collecting voter details and embedding a Google Form to cast votes for the **Chairperson** role.

## Features

- Voter registration screen (name, graduation year, email)
- Inline validation for required fields + email format
- Embedded Google Form (iframe)
- Confirmation overlay with Cancel / OK actions
- “Thank you” celebration overlay (confetti)
- Success screen showing voter details and submission timestamp

## Live page

- `index.html` (open directly in a browser)

## How it works (high level)

1. User enters voter details on the **Voter Registration** screen.
2. Clicks **Continue to Vote** → details are displayed on the vote screen.
3. The Google Form is shown inside the page.
4. User submits the form on Google.
5. User clicks **I’ve submitted my vote** → the thank-you overlay appears, then the success screen.

> Note: Due to browser **cross-origin restrictions**, the page cannot reliably detect Google Form submission automatically from inside the iframe. The UI therefore relies on the **"I've submitted my vote"** button.

## Setup / Running

No build step required.

### Option A: Open locally

- Double-click `index.html` or open it in your browser.

### Option B: Use a local web server (recommended)

Some browsers behave better when served over HTTP.

Example (if you have Python installed):

```bash
python -m http.server 5500
```

Then open:

- http://localhost:5500/

## Configuration

### Embedded Google Form

Edit the iframe `src` in `index.html`:

```html
<iframe
  src="https://docs.google.com/forms/d/e/.../viewform?embedded=true"
  ...
></iframe>
```

### Graduation Year Range

In `index.html`, the year dropdown is generated from the current year down to **1990**.

## File structure

- `index.html` — all markup, styling (CSS), and logic (JavaScript) are contained here.
- `TODO.md` — project notes.

## Technologies used

- Bootstrap 5 (CDN)
- Bootstrap Icons (CDN)
- Google Fonts (CDN)
- Vanilla JavaScript

## Contact

- United OBs & OGs of St. Josephine Bakhita
- Email: ssemwogerere.ashiraf@stud.umu.ac.ug
- WhatsApp: https://wa.me/256701422100

