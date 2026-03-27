# ✦ My Finance Dashboard

Personal finance app I built (with ChatGPT/Claude) to actually manage my money day-to-day — not just track it.

This version is **stable + polished (Pass 3 + Mobile Safe)** and is safe to use with real data.

---

## 🧠 What this app does (for me)

- Track all accounts, cards, loans, BNPL
- Log transactions (pending, cleared, scheduled)
- Plan bills + subscriptions
- See what’s coming up (forecast)
- Know what I can safely spend
- Stay aware without feeling restricted

---

## 📦 Key Systems

### Transactions
- Can log:
  - cleared
  - pending
  - scheduled
- IMPORTANT:
  - transaction date = **when it hits statement**
  - due date (bills/subs) = **separate**
  - I can edit transaction dates without affecting due dates

---

### 💳 BNPL (Klarna, Afterpay, etc.)
Each plan includes:
- total amount
- payment amount
- **first payment date**
- cadence:
  - monthly
  - biweekly
  - weekly
- number of payments

Used to understand:
- future obligations
- real monthly impact

---

### 📅 Bills & Subscriptions
- tracked separately from transactions
- can be logged into transactions when paid
- show up in forecast + upcoming

---

### 📊 Dashboard
- account balances
- spending trends
- “safe to spend”
- reassurance messaging (not scarcity-based)

Quotes rotate automatically (daily-based logic).

---

## 🔄 Data Storage (IMPORTANT)

### Local (default)
- stored in browser (localStorage)

### Google Sheets (MY SETUP)
I sync this app to Google Sheets so I don’t lose data.

Purpose:
- backup
- portability
- visibility outside app

⚠️ Reminder to self:
- if something breaks, my data is still in Sheets
- don’t rely ONLY on browser storage

---

## 📱 Usage

I use this:
- mostly on mobile
- also on desktop

Mobile is optimized (Polish + Mobile Safe pass), but still evolving.

---

## 🎨 Current Version

Includes:
- Polish Pass 1 → visual cleanup
- Polish Pass 2 → UX + feedback
- Polish Pass 3 → interaction fixes
- Mobile Safe Pass → better phone usability

---

## ⚠️ Things to remember

- This is a **live working file**, not version-controlled per change
- Before major edits:
  👉 duplicate file as backup (index-stable.html)

- Don’t change:
  - core logic
  - data structure
unless necessary

---

## 💡 Future Improvements (when I feel like it)

- deeper forecast logic
- smarter insights
- better mobile interactions
- shared usage (Edwin)

---

## 🫶 Why I built this

I don’t respond well to:
- restriction
- scarcity

So this app is designed to:
- give visibility
- keep flexibility
- reduce impulsive spending without pressure

---

## ✅ Status

✔ Stable  
✔ Looks good  
✔ Mobile usable  
✔ Safe to start using with real data  

---

## 📝 Note to future me

If something feels off:
- don’t panic
- check logic vs UI issue
- refer back here before changing things

You built something really good — don’t break it rushing updates 😌




## 🔄 Google Sheets Sync Setup

This app is connected to Google Sheets for backup + persistence.

If something breaks in the app, my data still lives in Sheets.

---

## 📁 Step 1: My Google Sheet

I have a Google Sheet that stores:
- accounts
- transactions
- bills
- subscriptions
- BNPL

⚠️ IMPORTANT:
- Each tab = one data type
- Do not rename tabs unless I update the script

---

## ⚙️ Step 2: Apps Script (the connector)

Inside Google Sheets:
1. Extensions → Apps Script
2. There is a script that:
   - receives data from the app
   - writes to the correct tab
   - returns data when loading

---

## 🌐 Step 3: Web App URL

I deployed the script as a **Web App**

Steps (if I ever need to redo it):
1. Click “Deploy”
2. Select “New deployment”
3. Type: **Web App**
4. Access:
   - Execute as: Me
   - Who has access: Anyone

Copy the URL → THIS is what the app uses

---

## 🔗 Step 4: Connect to App

In my app:
- there is a sync URL field (or config)
- paste the Web App URL

This enables:
- saving data → Sheets
- loading data ← Sheets

---

## 💾 How Sync Works (mental model)

- App = interface
- Sheets = database

When I:
- add/edit something → it saves to Sheets
- reload app → it pulls from Sheets

---

## 🧪 If Sync Stops Working

Check in this order:

### 1. Is the Web App URL still valid?
- Sometimes redeploying changes it

### 2. Did I rename any tabs?
- Script depends on exact names

### 3. Check Apps Script logs
- Extensions → Apps Script → Executions

### 4. Try re-deploying
- New deployment → copy new URL → update app

---

## ⚠️ Safety Rules

- Always keep Google Sheets as source of truth
- If app acts weird → DO NOT panic
- Data is still in Sheets

---

## 💡 Notes to self

- Don’t overcomplicate the script
- Keep structure consistent
- Backup Sheet occasionally (File → Make a copy)

---

## 🫶 Why I did this

Local storage alone is risky.

Sheets gives me:
- backup
- visibility
- flexibility
- peace of mind
