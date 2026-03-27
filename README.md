# my finance ✦

Personal finance dashboard for Joanne (+ Edwin). Single HTML file, hosted on GitHub Pages, syncs to Google Sheets.

---

## 💡 Features

- **Accounts** — checking, savings, with per-account transaction history and inline reconcile
- **Envelopes** — YNAB-style budget categories, drag to reorder
- **Transactions** — add income/expenses, merchant autocomplete, running balance, bulk actions
- **Bills & Recurring** — mark paid, auto-logs transaction and deducts from account
- **Subscriptions** — membership/subscription tracker with renewal alerts
- **Credit Cards** — 13 cards, utilization tracking, one-tap payment logging
- **Loans** — balance tracking, one-tap payment logging
- **Paycheck Planner** — split paycheck across accounts, assign bills per paycheck
- **Forecast** — 3/6/12 month spending projection
- **Two profiles** — Joanne (PIN protected 🔒) + Edwin, each with separate data
- **Google Sheets sync** — auto-saves in the background
- **PWA** — installable on iPhone/Android like a native app
- **Dark mode** — toggle in the top corner
- **Mobile + iPad responsive**

---

## 🚀 Setup (first time)

1. Open your GitHub Pages URL
2. You'll see a yellow "Setup needed" banner at the top
3. Paste your **Google Apps Script URL** → hit Connect
4. Your data loads automatically from Google Sheets

> Your Apps Script URL never changes — you only need to do this once per browser/device.

---

## 🔄 Updating the app (when you get a new file from Claude)

1. Download the new `index.html`
2. Go to your GitHub repo → click `index.html` → click the pencil ✏️ to edit → or just drag and drop the new file
3. Commit the change
4. Open your GitHub Pages URL — it may take 1–2 minutes to update
5. If it asks for your Apps Script URL again, just paste it in — your data is safe in Google Sheets

> **Your data is never in the HTML file itself.** It lives in Google Sheets and your browser's localStorage. Replacing the file never wipes your data.

---

## 🔒 Profile PIN

Joanne's profile is PIN protected. To set or change the PIN:

1. Make sure you're on Joanne's profile
2. Go to ⚙️ Settings → scroll to the purple **Profile PIN** card
3. Enter a 4-digit PIN twice → Save

Edwin will see a numeric keypad when he tries to switch to your profile.

---

## 💳 Logging a CC or loan payment

1. Go to **Credit Cards** or **Loans**
2. Tap **💳 Make payment** / **💰 Pay** on the card or loan
3. Enter the amount, choose which account to pay from → confirm
4. The transaction is logged, your bank account balance updates, and the card/loan balance goes down automatically

---

## 🔍 Reconciling an account

1. Go to **Accounts** → tap any account card
2. Scroll to the **Reconcile** panel on the right
3. Type your actual bank balance
4. Choose:
   - **Log adjustment & reconcile** — adds a correction transaction automatically
   - **Just update balance** — silently fixes the number (use this if you've already found and fixed the discrepancy in your transactions)

---

## 🏗 Stack

| Thing | What |
|---|---|
| Language | Vanilla HTML + CSS + JavaScript |
| Styling | Tailwind CSS via CDN |
| Cloud sync | Google Apps Script → Google Sheets |
| Hosting | GitHub Pages |
| Framework | None — no build step, no dependencies |

---

## 📁 Files in this repo

| File | What |
|---|---|
| `index.html` | The entire app — one file |
| `apps-script.js` | Paste this into Google Apps Script for Sheets sync |
| `README.md` | This file |

---

## 🆘 If something looks broken

1. Open browser DevTools (F12) → Console tab
2. Screenshot any red errors
3. Send to Claude with the current `index.html` for a fix
4. Your data is safe in Google Sheets — a broken file never touches your data
