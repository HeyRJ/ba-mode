# Field spec template

A field spec has one row per field in the client's file. Each row says what's allowed, gives an example, and gives the exact message shown when the value is wrong. The developer builds the upload checks from it, and the tester tests against it.

| Field | Required | Format and allowed values | Example | Error message |
|---|---|---|---|---|
| `<column name, as the client's team writes it>` | Yes / No | `<type, range, formats accepted, how blanks count>` | `<a real value>` | `<the exact message, with the row number>` |

## Filling in each column

- **Field:** keep the column names the client's team already uses.
- **Required:** say whether the column must be there and whether each cell must have a value. They're not the same thing.
- **Format and allowed values:** be exact. Give the ranges, the formats you accept and the ones you refuse, and say how blanks, "NA" and "-" count. Refer to business rules by ID, for example (BR-12).
- **Example:** a real value from the client's file.
- **Error message:** the exact words, with the row number, like `Row {n}: …`. Give one message per problem, and keep one style across the whole spec.

## Two examples

The first row is the simple one from the episode's kitchen slip. The second is the real Views row that Claude wrote for Kavya's sheet.

| Field | Required | Format and allowed values | Example | Error message |
|---|---|---|---|---|
| Spice | Yes | A whole number from 1 to 5 | 3 | Spice: write a number from 1 to 5. |
| Views | Yes | Whole number, 0 or more. Commas allowed in Indian or western grouping. Spaces at either end ignored. Short forms such as 12.4K or 1.2L are not accepted (BR-11, BR-12). 0 means the post is too new to grade (BR-06). | 1,25,000 | Blank: Row {n}: Views is empty. Enter 0 if there were none.<br>Invalid: Row {n}: Views must be a full number, like 12400 or 12,400. "{value}" is not accepted. |

The full spec for Kavya's sheet has 16 rows, including the file rules. It's the "Field spec" sheet in [`example-kavya/outputs/Reach report card v1 requirements.xlsx`](example-kavya/outputs).

## File rules

Spec the file as well as its columns: file type, size limit, row limit, where the header is, how blank rows count, and the encoding.

## If an answer has no field spec

```text
Now make this buildable. A developer will write the upload checks from this, so turn <client>'s file into:
1. A field spec: one row per column in their file (<the columns>), with Required, Format and allowed values, Example, and the exact error message
2. File rules: file type, size limit, row limit, where the header is, blank rows, encoding
3. Business rules numbered BR-01 onwards: <the rules that matter, e.g. formulas, rounding, bands, duplicates, ties, and what shows when nothing can be processed>

Keep the column names their team already uses. Mark anything <client> didn't decide as "Proposed: confirm with <client>".
```
