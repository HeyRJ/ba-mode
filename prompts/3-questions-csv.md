# 3 · Open questions into a CSV

Claude ends every requirements answer with open questions. Send this to get them as a file you can share with the client.

```text
Keep the open questions separately, in a Questions CSV file I can share with <client>. One row per question, with a proposed answer wherever you'd suggest one, so they can just say yes or no. I'll get answers after discussing with them, and I'll answer what I can myself.
```

When the answers come back, paste them in by question number and ask Claude to update everything to match, showing only what changed. [`example-kavya/4-answers-round-1.md`](../example-kavya/4-answers-round-1.md) shows how.

Each round of answers brings new questions. When the new ones stop blocking the build, baseline v1 (see "Stop the loop" in [`lead-review-checklist.md`](../lead-review-checklist.md)).

As typed in the episode: [`example-kavya/3-questions-csv.md`](../example-kavya/3-questions-csv.md)
