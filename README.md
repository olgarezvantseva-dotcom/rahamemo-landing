# RahaMemo

A ledger that reads your bank statement so you don't have to.

RahaMemo turns a raw bank statement export into a categorized, browsable record of where money actually goes, parsed automatically, kept entirely on your own device.

**Status:** live at [rahamemo.com](https://rahamemo.com), in active development.

## What it does

- **Statement parsing (core)** — paste a bank statement export, upload a `.txt`/`.csv`, or upload a screenshot or photo of your transaction list. Each line (or image) is read and structured: merchant, amount, and date pulled out of whatever format the bank exports.
- **Automatic categorization (core)** — transactions are sorted into categories without manual tagging, using the Anthropic API to interpret merchant names and context. Rows the model wasn't confident about are flagged for review before anything is added.
- **Review before it's added (core)** — parsed rows land in a review queue, not straight in the ledger. Nothing is saved until you confirm it.
- **Budgets & category limits** — set an overall monthly budget and per-category spending limits, with pace tracking against the day of the month.
- **Custom categories** — add, rename, or delete spending categories to match how you actually think about your money.
- **Local-first storage (design choice)** — parsed data is kept in the browser via `localStorage` rather than sent to a backend database. Statement images are held in memory only while being read, then discarded — never written to disk or sent anywhere except directly to Anthropic's API.

## Built with

| Layer | Tech |
|---|---|
| Parsing | Anthropic API |
| Frontend | Web app |
| Storage | localStorage |

## Where it stands

Statement parsing (text and screenshots), categorization, review-before-confirm, budgets/limits, onboarding, and editing categories all work end-to-end. Multi-account support is still being built out.

---

Built by [Olga Bestšastnaja](https://www.linkedin.com/in/olga-best%C5%A1astnaja/)
