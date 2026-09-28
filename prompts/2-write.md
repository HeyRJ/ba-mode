# 2 · Write

Take Claude's questions to the client first. Send this once you have their answers.

```text
<client>'s reply:

---
<paste the client's answers>
---

Now write the requirements for <the feature>:
1. Epics, then user stories (As a… I want… so that…)
2. Acceptance criteria for each story in Given/When/Then
3. A priority for each story: Must, Should, Could or Won't
4. Non-functional requirements as a separate list
5. Assumptions and open questions at the end

Use <client>'s numbers exactly. Anything they didn't decide, mark "Proposed: confirm with <client>".
```

The field spec and the business rules come from the Project instructions, so you don't need to ask for them here. If an answer ever arrives without them, use the prompt at the end of [`field-spec-template.md`](../field-spec-template.md).

As sent in the episode: [`example-kavya/2-kavya-reply.md`](../example-kavya/2-kavya-reply.md)
