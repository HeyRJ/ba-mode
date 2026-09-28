# BA mode

A Claude setup for business analysts. It takes a messy client brief to requirements a developer can build and a tester can test. Claude drafts, and you make the calls.

It comes from **Claude for BAs · 01** on the [Rohan J](https://www.youtube.com/@rohanbuilds-ai) YouTube channel (in Hindi). In the episode, a client's WhatsApp message and a sheet with 12 hidden traps turn into 47 clarifying questions. They then become 27 user stories with 87 Given/When/Then acceptance criteria, a field spec and 20 business rules, handed over as one Excel file.

## What's inside

| File | What it's for |
|---|---|
| [`project-instructions.md`](project-instructions.md) | WHO, WHAT and HOW for your Claude Project: the rules every answer follows |
| [`prompts/`](prompts) | The four messages you send, in order: ask first, write, questions CSV, Excel |
| [`lead-review-checklist.md`](lead-review-checklist.md) | What to catch before anything goes to the client or the developer |
| [`field-spec-template.md`](field-spec-template.md) | One row per field: format, allowed values and the exact error message |
| [`example-kavya/`](example-kavya) | The episode's example: Kavya's brief, her sheet, every message sent and the outputs |

## How to use it

1. **Set up a Claude Project** for the product. Paste [`project-instructions.md`](project-instructions.md) into its instructions, with your product in WHO.
2. **Add a short context file** to the Project: what the product does today and its constraints. [`example-kavya/reach-context.md`](example-kavya/reach-context.md) shows the idea.
3. **Ask first.** Start a chat in the Project, attach the client's file and send [`prompts/1-ask-first.md`](prompts/1-ask-first.md). Claude asks its questions before writing anything, and names the rows it's asking about.
4. **Write.** Take the questions to the client. Then send their answers with [`prompts/2-write.md`](prompts/2-write.md). You get epics, user stories, Given/When/Then criteria, priorities, a field spec, business rules and non-functional requirements.
5. **Put the open questions in a CSV.** Send [`prompts/3-questions-csv.md`](prompts/3-questions-csv.md). Each question comes with a proposed answer, so the client can just say yes or no. Paste their answers back.
6. **Review as the lead** with [`lead-review-checklist.md`](lead-review-checklist.md). When new answers stop changing anything the build needs, baseline v1 and park the rest.
7. **Hand over.** Send [`prompts/4-excel.md`](prompts/4-excel.md) to get one Excel file with the stories, field spec and business rules for the developer and the tester.

## Before you start

- Put work data only into AI tools your company allows.
- Kavya, her agency, the bakery and every number in the example are fictional.
- The episode was recorded on Claude Pro with Opus 5.5. Projects, file uploads and creating files are on the Free plan too, which uses Sonnet and Haiku (checked on claude.com/pricing on 28 Sep 2026).

## Next

Claude for QAs · 01 turns this Excel file into test cases. A QA mode repo will follow in the same way.
