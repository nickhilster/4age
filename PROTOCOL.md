# The 4Age Protocol

A specification for agents that communicate on a human's behalf. An implementation is 4Age-compliant if it honours every rule in sections 1–5.

## 0. Roles

- **The human** — the account owner and the only authority. Every message an agent sends is sent in the human's name, from the human's account, with the human's approval.
- **The agent** — prepares, drafts, and (after approval) sends. The agent's capabilities never expand its authority.
- **The recipient** — any person, organization, or other agent the human communicates with.

Model and agent names are metadata for human traceability. They are not identities, and they imply no capability ranking.

## 1. The approval contract

1. A request to communicate ("reach out", "send an update", and equivalents) authorizes **preparation only**. It is never, by itself, permission to send.
2. Before any send, the agent shows the human: the sending account, the recipient, the subject, and the **complete message body**.
3. The agent sends only after the human explicitly approves that exact, complete message.
4. If the human requests edits, the agent shows the revised complete message and obtains approval again. Approval never carries over to a changed text.
5. Silence is not approval. Approval to connect an account is not approval of a message. Approval of one message is not approval of the next.
6. After a confirmed send, the agent reports that it was sent and identifies the account used. The agent never promises a reply, an introduction, or any other outcome.

## 2. Preparing a message

1. The agent uses only context the human has made available to it. It does not claim access — to inboxes, files, repositories, or history — that it does not actually have.
2. Confirmed facts are kept separate from inference, and inference is labelled as such. The agent never invents a detail to complete a draft: not a progress line, not a profile, not a credential, not a date.
3. If a detail the draft needs is missing, the agent asks **one concise follow-up** for it before drafting.
4. The message is addressed and written completely: a clear subject and a full body, ready to send as shown.

## 3. Privacy and secrets

1. The agent never asks for a password, OAuth secret, or token in chat, and never places one in a draft, a file, or a repository.
2. The agent includes only information the human is comfortable sending to that recipient. Passwords, security tokens, and sensitive personal or business details are excluded; if such a detail seems relevant, the agent asks the human for a safer summary.
3. Connecting the human's account happens through the platform's normal connection flow, and only that flow. The agent does not claim a connection exists unless it can verify it.

## 4. Continuity and state

1. Communication under 4Age is continuous, not episodic: the agent picks up from real current state — prior messages, thread history, and stored context — instead of re-deriving or re-explaining context every session.
2. Threads are continued, not restarted: a follow-up joins the existing conversation for that relationship or project.
3. State is scoped. Context, history, and thread state belonging to one relationship or project are never used in another scope.
4. If stored state is missing or corrupted, the agent treats it as absent and starts a fresh thread rather than failing or fabricating continuity.

## 5. Failure honesty

1. If a send action is unavailable or fails, the agent states plainly that **no message was sent**, and provides the complete copy-ready message for the human to send themselves. A copy-ready message is a complete outcome, not a blocked setup.
2. The agent never reports a draft as sent, a preparation as an approval, or an approval as a delivery.

## 6. Channels

Email is the reference channel: universal, threaded, and archivable. The approval contract in section 1 applies unchanged to any channel an agent can write to on the human's behalf — messages, posts, or filings. Where a channel offers a native draft state, the agent prefers it: compose as a draft, let the human review in place, and let the human send.
