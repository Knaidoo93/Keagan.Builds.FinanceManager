# 🪙 keagan.builds — Finance Manager

**A free, open-source Claude Project file that turns Claude into your personal finance co-pilot.**

Track expenses. Set goals. Stay on budget. Get smart suggestions — all inside Claude, with optional Notion sync.

---

## What Is This?

`keagan.builds/FinanceManager` is a `CLAUDE.md` file — a system prompt you drop into a **Claude Project** to give Claude persistent financial context and a consistent role across all your conversations.

Once set up, Claude becomes a dedicated finance assistant that:

- 📊 Tracks your expenses against a **60/20/20 budget** (or any split you prefer)
- 🎯 Monitors your **financial goals** and calculates progress
- ✅ Manages your **financial todos** so nothing falls through the cracks
- 🧠 Offers **proactive suggestions** based on your patterns
- 📅 Generates **monthly reviews** with honest, data-driven feedback
- 📓 (Optional) Syncs with **Notion** via the Notion MCP integration

No app. No subscription. No data leaving your conversations. Just Claude, your numbers, and a clear framework.

---

## Quick Start

### 1. Create a Claude Project

1. Go to [claude.ai](https://claude.ai) and open **Projects**
2. Create a new project — name it something like *"Finance Manager"*

### 2. Add the CLAUDE.md

1. In your project, go to **Project Instructions**
2. Copy the contents of [`CLAUDE.md`](./CLAUDE.md) and paste it in
3. Fill in the **"What You Know About This User"** section:
   - Your monthly take-home income
   - Your pay frequency
   - Your primary financial goals
   - Your known recurring expenses

### 3. (Optional) Connect Notion

1. In Claude's settings, connect the **Notion integration**
2. Duplicate the [Notion Template](#notion-template) into your workspace
3. Claude will be able to log expenses and update goals directly in Notion

### 4. Start Your First Session

```
budget status
```
```
log $12.50 coffee and croissant
```
```
goal add: Emergency fund — target $6,000 — by December
```
```
monthly review
```

---

## The 60/20/20 Framework

| Bucket | % | Purpose |
|---|---|---|
| 🏠 Needs | 60% | Rent, groceries, utilities, transport, insurance |
| 🌱 Savings & Debt | 20% | Emergency fund, retirement, debt payoff, investing |
| 🎉 Wants | 20% | Dining, travel, entertainment, hobbies |

Claude auto-calculates your dollar targets based on your income and tracks each bucket throughout the month. Prefer a different split? Edit the percentages in `CLAUDE.md`.

---

## Quick Command Reference

| Command | What it does |
|---|---|
| `log [amount] [description]` | Log an expense |
| `budget status` | See current month vs. targets |
| `goal update [name] [amount]` | Update progress on a goal |
| `goal add [name — target — date]` | Add a new goal |
| `todo add [task]` | Add a financial task |
| `todo done [task]` | Mark a task complete |
| `monthly review` | Full monthly summary |
| `suggest` | Ask for a proactive tip |
| `net worth` | Calculate net worth |

---

## Notion Template

The companion Notion template includes:

- **📊 Dashboard** — Monthly snapshot with budget gauges and goal progress
- **💸 Expense Log** — Full database with category, bucket, date, and amount
- **🎯 Goals Tracker** — Board view with progress bars and target dates
- **✅ Financial Todos** — Task list with due dates and priority flags
- **📆 Monthly Reviews** — Archive of past monthly summaries
- **⚙️ Settings** — Income, budget percentages, accounts list

[Duplicate the Notion template →](#) *(link coming soon)*

---

## Customization

The `CLAUDE.md` is designed to be forked and modified:

- **Change the budget split** — Edit the 60/20/20 table to your preferred percentages
- **Add accounts** — Include a section listing your checking, savings, and credit accounts
- **Change the tone** — Want Claude to be more coach-like? More analytical? Edit the interaction style section
- **Add rules** — e.g. "Always flag any single expense over $100 for review"

---

## Contributing

Contributions welcome! Some ideas for PRs:

- [ ] Improved Notion template with better formulas
- [ ] Alternative budget frameworks (50/30/20, zero-based, envelope method)
- [ ] Multi-language versions
- [ ] Sample prompts and conversation starters
- [ ] Investment tracking extension

Please open an issue before starting major work so we can coordinate.

---

## License

MIT — free to use, fork, and modify. Attribution appreciated but not required.

---

*Built by [keagan.builds](https://github.com/Keagan)*
