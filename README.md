# PageDuo for Claude

PageDuo lets Claude make things other people complete outside the chat, and report back: a graded training check from a policy, a sign-off form, a Dynamic Doc whose tables calculate, and documents sent to named people to sign.

## What it adds

- **Connector:** PageDuo's MCP server at `https://pageduo.ai/mcp`. You sign in to PageDuo (or sign up) the first time Claude uses it, and pick a workspace.
- **Skills:**
  - **policy-training**: a policy or handbook becomes a graded training. You see who passed, who failed and who is missing.
  - **live-report**: a weekly brief becomes a Dynamic Doc that updates when the numbers change.
  - **proposal-signoff**: a quote that calculates, adjusted with the client, then sent for signature.
  - **bilingual-contract**: an agreement in two languages, kept in step.

## Data

Requests and attached files go to PageDuo to build the item. Quiz, form and game links can be opened by anyone with the link. Signing documents are visible only to the sender and the signers named. Other documents stay private until shared. Answers people give come back to Claude only when you ask for results. - [Privacy policy](https://pageduo.ai/privacy)
- [How to use it](https://pageduo.ai/tutorials/overview/claude-and-chatgpt)
- [Support](https://pageduo.ai/support)
