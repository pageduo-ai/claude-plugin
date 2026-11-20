---
name: bilingual-contract
description: Write an agreement, policy or notice in two languages side by side, with each paragraph's translation kept in step and repeated terms (dates, amounts, durations) linked, then optionally send it for signature. Use for bilingual office documents such as supplier agreements, staff policies and notices.
---

# Bilingual contract

1. **Get the languages and the terms**: the two languages (main one first), the parties, and the key terms (amounts, durations, dates).
2. **Build it.** Call `pageduo_create_doc` with `languages` set to both languages, the terms in `request`, and any existing text in `source_material`. Say which terms repeat across clauses so they are linked.
3. **Change a term once.** Call `pageduo_update` with the `itemId` ("make the term 18 months"); every copy changes, in both languages. Report how many places moved.
4. **Sign** if asked: `pageduo_request_signatures` with `document` set to the `itemId` and each signer's name and email.

This is for ordinary office documents. Do not draft deeds, consumer loans or regulated filings, and do not give legal advice; suggest a lawyer review where the stakes call for it.
