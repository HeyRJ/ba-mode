# 4 · Excel handoff

Send this once v1 is baselined. Claude builds one Excel file for the developer and the tester.

```text
Put everything in one Excel file for the developer and the tester:
- Sheet "Stories": one row per acceptance criterion, with Story ID, Epic, Story, AC ID, Given, When, Then, Priority, Rule IDs, Status
- Sheet "Field spec": the field spec as agreed
- Sheet "Business rules": ID, Rule, Example
Set every Status to Draft and freeze the header rows.
```

One row per acceptance criterion means the tester can turn each row into a test case, and the developer can trace every check back to a rule. Claude creates the file itself.

The file from the episode: [`example-kavya/outputs/Reach report card v1 requirements.xlsx`](../example-kavya/outputs)
