# Example: Kavya's report card

Kavya runs a small social media agency. She wants Reach, a small web app, to turn her monthly sheet into a report card for her clients. Kavya, her agency, the bakery and every number here are fictional.

These are the files from the episode, in the order they were used. The Project was set up with `project-instructions.txt` and `reach-context.md`. Everything else went into one chat.

| Step | File | What it is |
|---|---|---|
| Setup | [`project-instructions.txt`](project-instructions.txt) | The Project's instructions, exactly as pasted |
| Setup | [`reach-context.md`](reach-context.md) | The Project's file about Reach: what exists today and its constraints |
| 1 | [`1-brief-and-sheet.md`](1-brief-and-sheet.md) and [`bakery sept FINAL (2).csv`](bakery%20sept%20FINAL%20%282%29.csv) | Kavya's WhatsApp message and her sheet, with the ask-first request |
| 2 | [`2-kavya-reply.md`](2-kavya-reply.md) | Her answers, and the request to write the requirements |
| 3 | [`3-questions-csv.md`](3-questions-csv.md) | The open questions into a CSV |
| 4 | [`4-answers-round-1.md`](4-answers-round-1.md) | Answers to the first 14 questions, after talking to Kavya |
| 5 | [`5-answers-round-2.md`](5-answers-round-2.md) | Answers to 5 more, and v1 baselined |
| 6 | [`6-excel.md`](6-excel.md) | The Excel handoff |
| Output | [`outputs/Report card - questions for Kavya.csv`](outputs) | Every question, Claude's proposed answer and the final answer |
| Output | [`outputs/Reach report card v1 requirements.xlsx`](outputs) | Stories (one row per acceptance criterion), field spec and business rules |

## What happened

- Before writing anything, Claude asked 47 questions and named all 12 traps in the sheet by row. It also caught that Reach's dashboard divides by reach, while Kavya's sheet has no reach column.
- One answer then gave 5 epics and 26 stories with Given/When/Then criteria, plus a field spec, business rules and 14 open questions.
- After two rounds of answers (the lead changed 9 of Claude's 17 proposed answers), v1 was baselined and anything further went to a parking lot for v2.
- The final handoff has 27 stories, 87 acceptance criteria, a 16-row field spec and 20 business rules.

## The 12 traps in the sheet

Row numbers are the spreadsheet's: the header is row 1 and blank rows count.

| Row | Trap |
|---|---|
| 1 | The Views header has a space in front: `" Views"` |
| 2 and 6 | 12,400 and 1,25,000: western and Indian number grouping |
| 4, 7 and 20 | Three more date styles: 03/09/2026, 2026-09-06 and 21/9/26 |
| 5, 26 and 27 | Blank rows |
| 8 | 12.4K, a short form |
| 9 | A Facebook row, though only Instagram and YouTube are supported |
| 12 and 13 | The same post twice |
| 15 | 14-09-2062, a date decades in the future |
| 18 | A giveaway with 1,840 comments that tops the list |
| 22 | 1.2L, a short form |
| 24 | 31-09-2026, a date that doesn't exist |
| 25 | All zeros, with the note "Posted today" |

Try the same brief and sheet with your own setup and see how many your Claude finds.
