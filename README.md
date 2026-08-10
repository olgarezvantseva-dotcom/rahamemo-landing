# RahaMemo

A ledger that reads your bank statement so you don't have to.

RahaMemo turns a raw bank statement export into a categorized, browsable record of where money actually goes — parsed automatically, kept entirely on your own device.

**Status:** in active development — not yet public.

## What it does

- **Statement parsing (core)** — upload a bank statement export and each line is read and structured: merchant, amount, and date pulled out of whatever format the bank exports.
- **Automatic categorization (core)** — transactions are sorted into categories (groceries, transport, subscriptions, etc.) without manual tagging, using the Anthropic API to interpret merchant names and context.
- **Local-first storage (design choice)** — parsed data is kept in the browser via `localStorage` rather than sent to a backend database. The statement stays on your device.

## Built with

| Layer | Tech |
|---|---|
| Parsing | Anthropic API |
| Frontend | Web app |
| Storage | localStorage |

## Where it stands

Statement parsing and categorization work end-to-end. Onboarding, editing categories, and multi-account support are still being built out.

---

Built by [Olga Bestšastnaja](https://www.linkedin.com/in/olgabest%C5%A1astnaja)
