# Invoice Operations Portfolio (Excel)

A fictional consultancy's invoice admin, built in Excel.

I made this to practise the weekly work of a business support administrator: tracking invoices, chasing aged debts, logging new projects and reporting clearly to a team.

**All data is made up.** No real client, employer or workplace data is in this file.

![Dashboard](screenshots/dashboard.png)

## The problem

A consultancy raises lots of invoices. Some get paid late, some partly paid, some not at all. Someone has to know what is overdue, who owes the most, and who to chase first.

## What's in the workbook

| Tab | What it does |
|---|---|
| **Start Here** | Short guide to the workbook, assumptions and limits |
| **Dashboard** | Total invoiced, payments, outstanding balance, overdue count, ageing buckets, monthly invoiced vs collected |
| **Client Ageing** | Ranks 15 clients by overdue balance, with each client's oldest debt |
| **Payment Tracker** | Daily worklist. Dropdown action, next follow-up date and notes for every invoice |
| **Invoice Data** | 150 invoices. Balance, status, days overdue, ageing band and priority are all formulas |
| **Project Setup Log** | Proposal codes, conflict checks and project set-up, with flagged conflicts and set-up times |
| **Reminder Emails** | Three templates: friendly nudge, follow-up, final notice |
| **Monthly Report** | Plain-English findings that update when the data changes |

![Client ageing](screenshots/client-ageing.png)

## What I found

At the reporting date (13 Nov 2026):

- Invoiced **$606,850**, received **$342,857**. Collection rate **56.5%**.
- **59 of 79** open invoices are overdue, worth **$207,581**.
- **18 invoices** are 61+ days overdue ($52,417). I would phone these clients, not just email.
- Three clients (Mosaic Engineering, Northstar Legal, Cobalt Partners) owe **39%** of the overdue balance.
- 30 invoices are High priority (more than 30 days overdue).

## How it works

- **Reporting date input** on Dashboard B5. Change it and every status, ageing band and priority recalculates.
- **Ageing bands:** Current, 1-30, 31-60, 61+ days.
- **Priority rules:** High is more than 30 days overdue. Medium is 1-30 days. Low is not yet due. Paid is Closed.
- **Formulas used:** SUMIFS, SUMIF, COUNTIF, IF, IFERROR, INDEX/MATCH, LARGE, MAXIFS, EDATE, TEXT.
- **Other Excel features:** tables, dropdown lists, conditional formatting, charts, frozen headers.

![Project set-up log](screenshots/project-setup-log.png)

## Assumptions and limits

- Paid amounts are totals as at the snapshot. The monthly view groups them by invoice month, not by the month the cash arrived.
- Changing the reporting date recalculates ageing, but it can't rebuild past payment history.
- Payments should be checked against accounting records before anyone makes decisions from this.

## What I would add next

- Timesheet and expense claim trackers
- A shared inbox log with response times
- Power Query to load invoice exports automatically

## Contact

Katie Nguyen | Sydney | katie.mnguyenx@gmail.com
