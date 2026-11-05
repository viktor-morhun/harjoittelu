# Harjoittelu Pipeline

An outreach tracker for finding a work-practice placement (työharjoittelu) during integration training in the Helsinki region. It lists 195 IT companies ranked by fit and keeps track of every contact from first message to reply.

**Live:** https://viktor-morhun.github.io/harjoittelu/

## Features

- 195 Helsinki, Espoo and Vantaa companies ranked by a fit score (0–100). The score is based on priority, open junior/full-stack roles, AI-tooling stack, team size and verified contacts.
- Stages: Not contacted → Sent → Replied → Interview → Accepted / Declined. Stages change inline or from the detail panel, and every change is written to an activity log.
- List and Board views. The Kanban board supports drag and drop with mouse and touch (long-press on phones and tablets), with auto-scroll while dragging.
- Follow-up reminders: marking a company as Sent schedules a follow-up 7 days later, and overdue ones are highlighted.
- Message templates in English and Finnish with `{company}`, `{name}`, `{email}`, `{phone}` and `{link}` variables. Copy the subject and body, then mark the company as sent.
- Stats for contacted companies, response rate, interviews and follow-ups due.
- Search, filters (priority, city, hiring now) and sorting (fit, last updated, follow-up date, name).
- Add your own companies, and export to CSV.
- Backup and restore as JSON. All data stays in your browser (`localStorage`).
- Light and dark theme, and works on phones.
- Keyboard shortcuts: `/` search · `j`/`k` move · `Enter` open (list rows and board cards) · `1`–`6` set stage · `Esc` close.

## Stack

A single static `index.html` with vanilla JavaScript and CSS. It has no build step and no dependencies apart from the Geist font from Google Fonts.

## Run locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Data

The company data was collected in November 2026 from company websites, Duunitori, itduunit.fi, Jobly, HN "Who is hiring", VCBacked and Seedtable. Contacts marked as verified were taken from the company's own website. Everything else should be checked before you reach out.
