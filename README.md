# PageDuo for Claude

PageDuo lets Claude make things other people complete outside the chat, and report back: a graded training from a policy, a sign-off form, a Dynamic Doc whose tables calculate, and documents sent to named people to sign.

## Install

In Claude Code:

```
/plugin install pageduo --marketplace pageduo-ai/claude-plugin
```

To add only the connector in Claude: **Settings → Connectors → Add custom connector**, with the URL `https://pageduo.ai/mcp`.

## What it adds

- **Connector:** PageDuo's MCP server at `https://pageduo.ai/mcp`. You sign in to PageDuo (or sign up) the first time Claude uses it, and pick a workspace.
- **Skills:**
  - **policy-training**: a policy, handbook or SOP becomes a graded training check. You see who passed, who failed and who is missing.
  - **live-report**: a report whose tables recalculate and whose repeated figures stay linked, so each new period is just new numbers.
  - **proposal-signoff**: a quote or proposal whose pricing recalculates, sent to named people who each sign by link.
  - **bilingual-contract**: an agreement in two languages, kept in step, then sent for signature if you want.

## Data

Requests and attached files go to PageDuo to build the item. Quiz, form and game links can be opened by anyone with the link. Signing documents are visible only to the sender and the signers named. Other documents stay private until shared. Answers people give come back to Claude only when you ask for results.

- [Privacy policy](https://pageduo.ai/privacy)
- [How to use it](https://pageduo.ai/tutorials/overview/claude-and-chatgpt)
- [Support](https://pageduo.ai/support)
