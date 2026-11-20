---
name: proposal-signoff
description: Write a proposal or quote as a Dynamic Doc whose pricing table calculates, let the client adjust it, then send it to named people to sign and track who has signed. Use for client proposals, quotes, statements of work and service agreements.
---

# Proposal → proposal with sign-off

1. **Build the proposal.** Call `pageduo_create_doc` with the scope, the line items and how they price (hours × rate, materials, discounts) in `request`, and any brief in `source_material`. State the total in the text too, so it is linked to the table.
2. **Adjust.** When terms change ("make it 65 an hour", "drop the tiling"), call `pageduo_update` with the `itemId`. Report the new total.
3. **Send for signing** once the person confirms the final version: call `pageduo_request_signatures` with `document` set to the `itemId`, each signer's name and email, `signing_mode: sequential` only if they asked for an order, and a `due` date if given. Each signer confirms their email and signs on their own line.
4. **Track.** `pageduo_get_responses` with the `itemId` lists who has signed and when, and whether the document changed after it was sent.

Confirm the signers' emails before sending; a sent request cannot be unsent. Do not give legal advice.
