# 1 · Ask first

Attach the client's file to the chat and send this with their message. Claude reads both and asks what it needs to know before it writes a single requirement.

```text
New request from a client, <client>. Their message is below and their file is attached.

---
<paste the client's message>
---

Before you write any requirements, read the message and the file, then ask me the questions you need answered. Group them under Scope, Business rules, Data and Non-functional. Where the file raises a question, name the row. Don't answer your own questions.
```

**Why it works:** "Before you write any requirements" stops Claude from drafting on guesses. "Name the row" makes every question checkable against the file. In the episode, this one message got 47 questions, and they named all 12 traps in the sheet by row.

As sent in the episode: [`example-kavya/1-brief-and-sheet.md`](../example-kavya/1-brief-and-sheet.md)
