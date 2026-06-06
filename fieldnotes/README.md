# fieldnotes

A self-contained personal CRM and career workspace for students and early-career engineers doing job searches, networking, and internship tracking. No setup, no account, no server. Download one HTML file, open it in your browser, and you're done.

![fieldnotes screenshot](screenshot.png)

## what it does

- **Contact CRM** — track everyone you're networking with, what stage you're at, what you owe them, heat score, preferred contact method, notes
- **Interaction log** — log every call, email, text, or meeting with a contact; timestamped feed sorted by recency
- **Job pipeline** — track roles from wishlist through offer, linked to contacts at those companies
- **Aspirations** — target companies and role types, auto-linked to contacts and jobs
- **Scratchpad** — rich text notes with `@contact` and `#company` mentions that link back to your CRM cards; headings, bold, bullets, strikethrough
- **Smart filters** — overdue (14d+ no contact), i owe them, high heat, HMC alumni, stags network
- **Daily digest** — copy a plain-text summary of overdue contacts and pending actions into a calendar event for a daily reminder
- **Full export** — JSON (complete backup, importable) and CSV (for spreadsheets)

## why a single HTML file

No framework, no build step, no dependencies. Data lives in your browser's `localStorage`. The whole thing is one file you can download, open, and use immediately — or inspect, fork, and modify without setting up a dev environment.

Tradeoffs: data is tied to one browser on one device. Use the JSON export to back up regularly and move between machines.

## how to use

1. Download `fieldnotes.html`
2. Open it in any modern browser (Chrome, Safari, Firefox, Edge)
3. Add contacts, track jobs, take notes
4. Export your data regularly to avoid losing anything

## keyboard shortcuts (scratchpad)

| Action | How |
|--------|-----|
| Mention a contact | Type `@` + name |
| Mention a company | Type `#` + company name |
| Navigate dropdown | Arrow keys, Enter to confirm |

## data model

All data stored in `localStorage` under these keys:

| Key | Contents |
|-----|----------|
| `crm_v4` | contacts array |
| `crm_jobs` | job pipeline array |
| `crm_aspirations` | target companies and roles |
| `crm_interactions` | interaction log |
| `crm_companies` | custom company list |
| `crm_scratchpad_html` | scratchpad HTML content |

## built with

Designed and iterated with AI. Single-file architecture, vanilla JS, no external dependencies except Google Fonts.

## part of

[`personal-tooling`](https://github.com/trusten5/personal-tooling) — a growing collection of self-contained browser tools built with AI assistance.

---

MIT License
