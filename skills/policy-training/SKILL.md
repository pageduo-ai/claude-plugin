---
name: policy-training
description: "Turn a policy, handbook, SOP or slide deck into a graded training check that staff take at a link, then report who passed, who failed and who has not done it. Use when someone wants employees, new hires or contractors to show they understood a document."
---

# Policy → graded training

1. **Get the material.** If no policy is attached or pasted, ask for it. Never write questions from memory.
2. **Get the settings the person has, and ask for none they did not mention.** Audience; how many questions; a pass mark only if they gave a number (PageDuo uses 80% and says so); a deadline only if they gave one; `identify_by: name_and_email` when they will check against a staff list.
3. **Build it.** Call `pageduo_create_quiz` with the person's own words in `request` and the complete text in `source_material`. Mix multiple choice with one written question when understanding matters; written answers are graded against a rubric.
4. **Hand over the link** from the card. Staff need no account and see only their own result.
5. **Report.** When asked, call `pageduo_get_responses` with the quiz's `itemId` and, if they give the team list, `expected_people`. Lead with the answer: how many passed of how many, then who is missing, who was late, and the hardest question.
6. **Fix and re-run.** For a change, call `pageduo_update` with the `itemId`; the link stays the same.

Say "knowledge-check completion" for what the results show. A quiz is not certification or practical sign-off (for example, operating equipment).
