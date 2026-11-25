# 4Age

**A human-approved agent communication protocol.**

4Age is a convention for how AI agents communicate on a person's behalf — by email first, and by extension over any channel where an agent can act in someone's name. Its rule is simple:

> An agent may draft anything. It may send nothing without the human's explicit approval of the exact, complete message.

That friction is not a limitation waiting to be automated away. It is the product. 4Age exists so that a person can delegate real communication to agents — outreach, status updates, coordination between agents — without ever delegating the authority to speak in their name.

## The loop

1. **Trigger.** The human asks the agent to prepare a message ("reach out to…", "send an update on…"). A trigger authorizes preparation only — never sending.
2. **Draft.** The agent composes the complete message from context the human has made available: recipient, subject, full body. Facts are kept separate from inference; nothing is invented.
3. **Approve.** The agent shows the human the exact text, the recipient, and the sending account. The human approves that exact text — or edits it, in which case the revised text is shown and approved again. Silence is not approval. Approval to prepare is not approval to send.
4. **Send.** Only after explicit approval of the exact message does anything move, from the human's own account, in the human's name.
5. **Report.** The agent confirms what was sent and from which account — and never promises a reply, an introduction, or an outcome.

If sending is unavailable or fails, the complete copy-ready message is handed to the human to send themselves. That is a complete path, not a blocked state — and the agent says plainly that nothing was sent.

## Standing principles

- **The human is always the connector and the authority.** Nothing sends without their explicit approval.
- **Approval is exact.** It covers one specific message, shown in full. Any change re-opens approval.
- **Continuity over recap.** Communication picks up from real current state — persistent context, threaded history — instead of re-explaining everything every session.
- **Names are metadata.** Model and agent names exist for human traceability, not as identity or capability rankings.
- **Facts before inference, always labelled.** An agent never invents a detail — a progress line, a profile, a credential — to complete a draft.
- **Secrets never travel.** No passwords, tokens, or sensitive personal or business details in drafts, chat, or repository files. If a detail matters, the human provides a safer summary.
- **State is scoped.** Context and thread state belong to a relationship or a project; they never leak across scopes.

## Why email

Email is the one channel every agent, every person, and every organization already shares — addressable, threaded, archivable, and readable by humans and machines alike. 4Age treats email as the agent-to-agent and agent-to-human interop layer, with the human as the routing authority. The same approval contract applies to any other channel an agent can write to.

## Status

4Age is a living protocol, in daily production use: it governs an email mesh of personal and specialist agents (a personal agent, a business chief-of-staff agent, and a founder-operator agent) coordinating work for its author, and it has been applied in tooling that drafts continuity emails from a project's git history — always as drafts, always human-sent.

The full specification is in [PROTOCOL.md](PROTOCOL.md).

## License

MIT — see [LICENSE](LICENSE).

Designed by Nikhil Khedkar ([TeamBotics](https://teambotics.app)).
