---
name: live-report
description: "Make a report whose tables recalculate and whose repeated figures stay linked, so each new period is just new numbers: totals, percentages and the sentences quoting them follow. Use when a sales, operations, budget or KPI report is shared with others and revised every week or month, and the user wants the figures to stay right without a separate spreadsheet."
---

# Report that recalculates

1. **Collect the numbers** the person has (pasted, attached, or listed). Ask only for what is missing to make the tables add up.
2. **Build it.** Call `pageduo_create_doc` with `request` describing the sections, the tables and how the numbers combine (totals, change from last period, percentages), and the figures in `source_material`. Say which figures the text repeats, so they are linked.
3. **Share.** The document is private until the person shares it from PageDuo; offer **Open in PageDuo**.
4. **Next period.** Call `pageduo_update` with the document's `itemId` and the new numbers in plain words ("North 141k, South 96k for September"). Totals, charts and every repeated figure follow; report what moved.

Never invent a figure. If a number is missing, leave it out and say so.
