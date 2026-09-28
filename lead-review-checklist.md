# Lead review checklist

Claude drafts the requirements. These are the calls it can't make for you. Go through them before anything goes to the client or the developer.

## 1. Before anything goes to the client

- [ ] Everything marked "Proposed: confirm with client" is either confirmed or in the questions file.
- [ ] Each proposed answer is something the client would actually want. In the episode, Claude proposed a PDF the client never asked for, so it was dropped.
- [ ] Placeholders mean what the client means by them. In the client's sheet, "-" in Shares meant zero, not an error to fix.
- [ ] Limits come from the client's real files and machines. In the episode, 1,000 rows, 1 MB and 2 seconds became 10,000 rows, 5 MB and 3 seconds.

In the episode, the lead changed 9 of Claude's 17 proposed answers after talking to the client.

## 2. Numbers

- [ ] **Band edges.** When ranges touch (A is 6–10, B is 3–6), say which band the edge belongs to. In the episode, each band includes its lower edge, so 6.0% is an A.
- [ ] **Rounding.** Say whether the grade uses the exact number or the one shown. In the episode it's the one shown: 2.98% shows as 3.0% and gets a B.
- [ ] **Worked examples** use real rows from the client's file, and you check them again after every round of answers. In the episode, YouTube went from 2.8% to 2.6% once the answers changed the rules.
- [ ] **Check the final numbers yourself**, in a spreadsheet or with a short script, before the handoff.

## 3. Stories and acceptance criteria

- [ ] Every rule the client gave made it in.
- [ ] There are no vague words (fast, easy, user-friendly). Every criterion has exact values and could become a test case as written.
- [ ] Big stories are split up, and the priorities make sense. Anything the client said "later" to is Won't (this release).
- [ ] Non-functional requirements have numbers and say how a tester checks them.
- [ ] Where the feature changes something the product already does, the answer says so.

## 4. Field spec and business rules

- [ ] Every column in the client's file is covered, including the optional ones and any column the app ignores.
- [ ] Error messages are exact text a developer can copy, all in one style.
- [ ] Row numbers in messages match the spreadsheet: the header is row 1 and blank rows count.
- [ ] Each business rule is defined once, has an ID, and is referred to by that ID everywhere else.

## 5. Stop the loop

Every round of answers brings new questions. When the new ones stop blocking the build, baseline v1:

```text
That baselines v1. From now on, don't add open questions unless one blocks a Must story. Put anything else under "Parking lot (v2)" instead.
```

## Sending review notes

When you catch a miss, send it as a numbered list with the exact fix, and ask for only what changed:

```text
Review notes from me, the lead:
1. <what's wrong, and the exact fix>
2. <…>

Fix the stories, the field spec and the business rules for these. Show only what changed, and list any new questions for <client>.
```
