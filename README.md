# freelance-profit-tracker

A React Native app for freelancers to log work by client/project, track expenses, and view monthly profitability + efficiency analytics.

## Why this exists
Freelancers often track time and expenses in separate places (or not at all), making it hard to know:
- Which clients/projects are truly profitable
- Where non-billable “time leakage” happens (admin, travel, rework)
- Your effective hourly rate after expenses

This app is designed to make daily logging fast (<10 seconds) and turn it into useful monthly insights.

## Key features (MVP)
- ✅ Log work entries by **Client → Project**
- ✅ Categorize time: **Billable / Non-billable / Leakage**
- ✅ Record **duration + date** (timer can come later)
- ✅ Add **expenses linked to a work entry** (toll, parking, etc.)
- ✅ Monthly dashboard:
  - Total hours (billable vs non-billable vs leakage)
  - Revenue estimate
  - Expenses total
  - Net estimate
  - Effective hourly rate
- ✅ Drill down by **client / project / category**

## Screens (wireframe)
> Add screenshots here later:
- Today / Home
- Add Entry
- Monthly Summary
- Clients

## Tech stack
- React Native (Expo)
- Local-first storage: SQLite
- Charts: TBD

## Project structure (suggested)
```
/src
  /components
  /screens
  /navigation
  /db
  /services
  /utils
  /types
```

## Data model (high level)
- Clients
- Projects
- Work Entries
- Entry Expenses
- Monthly Overheads (optional)

## Analytics (core formulas)
- **Revenue**:
  - hourly: `hours * hourly_rate`
  - fixed: `fixed_amount`
- **Net**: `total_revenue - total_expenses`
- **Billable ratio**: `billable_hours / total_hours`
- **Effective hourly rate**: `(total_revenue - total_expenses) / total_hours`

## Getting started
> Placeholder (update once bootstrapped)

```bash
# install deps
npm install

# start
npx expo start
```

## Roadmap
### v1 (MVP)
- [ ] CRUD: clients, projects, entries, expenses
- [ ] Monthly dashboard + breakdown
- [ ] UX speed features (recent clients, presets, duplicate entry)

### v1.5
- [ ] Timer mode
- [ ] Export CSV
- [ ] Basic PDF summary

### v2
- [ ] Cloud sync + multi-device
- [ ] Invoicing export
- [ ] Tax categories / tags

## Contributing
PRs welcome! If you want to help:
1. Pick an issue from the backlog (or propose one)
2. Create a feature branch
3. Open a PR with screenshots or screen recording if UI-related

## License
MIT
