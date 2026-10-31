# AI Lead Capture Chatbot Demo

A 24/7 chatbot demo for real estate and clinic websites. It answers common questions and collects leads (name and phone) automatically.

Built by [Laiba Aftab](about.html), Next.js Developer & AI Automation Specialist.

## Features

- **Two demo modes:** switch between Real estate and Clinic with one click.
- **Lead capture flow:** booking, pricing, doctor and "talk to a human" questions start a short flow that asks for the visitor's name and phone number.
- **Phone validation:** the bot asks again if the number looks invalid.
- **Lead counter:** the header shows how many leads were captured in the session; click it to see the latest one.
- **Quick-reply buttons** for the most common questions.
- **Whole-word keyword matching**, so "hi" does not trigger on words like "this" or "which".
- **Accessible:** keyboard focus styles, ARIA labels, and reduced-motion support.
- **Responsive:** works on mobile and desktop.

## Getting started

No build step or dependencies are needed.

1. Download `chatbot-demo.html`.
2. Open it in any modern browser.

To host it, upload the file to any static host (GitHub Pages, Netlify, Vercel) or embed it on your site.

## Project structure

```
chatbot-demo.html   # HTML, CSS and JavaScript in a single file
README.md
about.html          # optional: linked from the footer
```

If you don't have an `about.html`, remove or change the footer link.

## Customizing

All content lives in the `BOTS` object in the script section of `chatbot-demo.html`.

| What to change | Where |
| --- | --- |
| Bot name, icon, greeting | `BOTS.re` / `BOTS.cl` → `name`, `icon`, `greeting` |
| Quick-reply buttons | `quick` array (`[label, message]` pairs) |
| Keywords and answers | `rules` array (`keys`, `reply`, `lead`) |
| Small talk and fallback | `SMALLTALK` and `FALLBACK` |
| Colors | CSS variables in `:root` |

Set `lead: true` on a rule to start the name and phone capture flow after that answer.

## Limitations

- Replies are keyword-based, not AI-generated.
- Leads are kept in memory only and are lost on page refresh.

## Ideas for next steps

- Send captured leads to WhatsApp, email, Google Sheets or a CRM through a webhook.
- Replace keyword matching with the Claude API for natural conversations.
- Add a Urdu / Roman Urdu language option.
- Save leads to a database and build a simple admin view.

## Contact

For a custom chatbot for your business, get in touch with Laiba Aftab.
