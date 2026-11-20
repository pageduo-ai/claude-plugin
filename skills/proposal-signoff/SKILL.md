---
name: proposal-signoff
description: Get a quote, proposal or statement of work signed: a document whose pricing table recalculates when the client changes a quantity, sent to named people who each sign on their own line by link, with who has signed tracked. Use when the user wants a client or partner to sign off on terms, not only a draft to read.
---

# Quote or proposal, signed

1. **Build the proposal.** Call `pageduo_create_doc` with the scope, the line items and how they price (hours × rate, materials, discounts) in `request`, and any brief in `source_material`. State the total in the text too, so it is linked to the table.
2. **Adjust.** When terms change ("make it 65 an hour", "drop the tiling"), call `pageduo_update` with the `itemId`. Report the new total.
3. **Send for signing** once the person confirms the final version: call `pageduo_request_signatures` with `document` set to the `itemId`, each signer's name and email, `signing_mode: sequential` only if they asked for an order, and a `due` date if given. Each signer confirms their email and signs on their own line.
4. **Track.** `pageduo_get_responses` with the `itemId` lists who has signed and when, and whether the document changed after it was sent.

Confirm the signers' emails before sending; a sent request cannot be unsent. Do not give legal advice.
