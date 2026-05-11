# Notion Template Spec — keagan.builds Finance Manager

This document describes the structure of the companion Notion workspace. Use this as a guide to build or duplicate the template.

---

## Workspace Structure

```
📓 keagan.builds — Finance Manager
├── 🏠 Dashboard
├── 💸 Expense Log  [Database]
├── 🎯 Goals Tracker  [Database]
├── ✅ Financial Todos  [Database]
├── 📆 Monthly Reviews  [Database]
└── ⚙️ Settings
```

---

## Page 1: 🏠 Dashboard

A linked, visual overview page. Not a database — just a Notion page with embedded views.

**Sections:**

### Monthly Snapshot (top of page)
- Callout block: "Month: [Month Year]"
- Three columns, one per bucket:
  - 🏠 Needs: `$X spent of $Y target (Z%)`
  - 🌱 Savings: `$X saved of $Y target (Z%)`
  - 🎉 Wants: `$X spent of $Y target (Z%)`

### Linked Views (embedded databases)
- **This Month's Expenses** — filtered view of Expense Log (current month)
- **Active Goals** — filtered view of Goals Tracker (status = Active)
- **Open Todos** — filtered view of Financial Todos (not checked)

---

## Page 2: 💸 Expense Log

**Database type:** Table

**Properties:**

| Property | Type | Notes |
|---|---|---|
| Name | Title | Short description of expense |
| Amount | Number | Currency format |
| Date | Date | Date of expense |
| Bucket | Select | Needs / Savings & Debt / Wants |
| Category | Select | See category list below |
| Payment Method | Select | Cash / Debit / Credit / Transfer |
| Recurring | Checkbox | Is this a recurring expense? |
| Notes | Text | Optional context |
| Month | Formula | `formatDate(prop("Date"), "MMMM YYYY")` |

**Category options by bucket:**

🏠 Needs: Rent/Mortgage, Groceries, Utilities, Transport, Insurance, Healthcare, Phone/Internet, Subscriptions (essential), Childcare/Education, Other

🌱 Savings & Debt: Emergency Fund, Retirement, Investments, Debt Payment, Sinking Fund, Other

🎉 Wants: Dining Out, Entertainment, Travel, Shopping, Hobbies, Personal Care, Gifts, Subscriptions (optional), Other

**Views:**
1. All Expenses — sorted by date descending
2. This Month — filtered by current month
3. By Bucket — grouped by Bucket
4. By Category — grouped by Category
5. Recurring — filtered: Recurring = true

---

## Page 3: 🎯 Goals Tracker

**Database type:** Table (or Board grouped by Status)

**Properties:**

| Property | Type | Notes |
|---|---|---|
| Goal Name | Title | e.g. "Emergency Fund" |
| Target Amount | Number | Currency format |
| Current Amount | Number | Currency format |
| Progress % | Formula | `round(prop("Current Amount") / prop("Target Amount") * 100)` |
| Target Date | Date | Optional deadline |
| Monthly Contribution | Number | How much to set aside monthly |
| Status | Select | Active / Paused / Completed |
| Bucket | Select | Which 60/20/20 bucket funds this |
| Notes | Text | Strategy, context, motivation |
| Started | Date | When goal was created |

**Views:** All Goals (table), Active (filtered), Board by Status (kanban)

---

## Page 4: ✅ Financial Todos

**Database type:** Table

**Properties:**

| Property | Type | Notes |
|---|---|---|
| Task | Title | What needs to be done |
| Done | Checkbox | Completed? |
| Due Date | Date | Optional deadline |
| Priority | Select | High / Medium / Low |
| Category | Select | Budget / Savings / Debt / Admin / Review |
| Notes | Text | Context or next steps |
| Created | Created time | Auto |

**Views:** Open Tasks (filtered + sorted), All Tasks, Completed

---

## Page 5: 📆 Monthly Reviews

**Database type:** Table

**Properties:**

| Property | Type | Notes |
|---|---|---|
| Month | Title | e.g. "May 2026" |
| Income | Number | Total income this month |
| Needs Spent | Number | Total Needs bucket |
| Savings Contributed | Number | Total Savings & Debt bucket |
| Wants Spent | Number | Total Wants bucket |
| Needs % | Formula | `round(prop("Needs Spent") / prop("Income") * 100)` |
| Savings % | Formula | `round(prop("Savings Contributed") / prop("Income") * 100)` |
| Wants % | Formula | `round(prop("Wants Spent") / prop("Income") * 100)` |
| Rating | Select | On Track / Minor Adjustments / Off Course |
| Notes | Text | Key insights, what to do next month |
| Review Date | Date | When the review was done |

---

## Page 6: ⚙️ Settings

A simple Notion page (not a database).

### Income
```
Monthly take-home income: $[amount]
Pay frequency: [weekly / bi-weekly / monthly]
Last updated: [date]
```

### Budget Targets (60/20/20)
```
🏠 Needs (60%):     $[amount]
🌱 Savings (20%):   $[amount]
🎉 Wants (20%):     $[amount]
```

### Accounts

| Account | Type | Institution | Notes |
|---|---|---|---|
| Main Checking | Checking | [Bank] | Primary spending |
| High-Yield Savings | Savings | [Bank] | Emergency fund |
| Credit Card | Credit | [Issuer] | Pay in full monthly |

### Recurring Expenses

| Expense | Amount | Bucket | Category | Renews |
|---|---|---|---|---|
| Rent | $1,200 | Needs | Rent/Mortgage | 1st of month |
| Phone | $45 | Needs | Phone/Internet | 15th of month |
| Spotify | $11 | Wants | Subscriptions | 22nd of month |

---

## Claude + Notion MCP Integration

Once Notion is connected to your Claude Project, you can say:

- `"Log $47 groceries from today to Notion"` → Creates a row in Expense Log
- `"Update my emergency fund goal to $3,200"` → Updates Goals Tracker
- `"Add a todo: call insurance to renegotiate"` → Creates a task in Financial Todos
- `"Paste my monthly review into Notion"` → Creates a new row in Monthly Reviews

To enable this, share your Notion database IDs with Claude (found in each database URL).

---

*Part of the [keagan.builds Finance Manager](../README.md) open source project · MIT License*
