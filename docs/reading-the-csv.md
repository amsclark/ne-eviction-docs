# Reading the CSV

Each run produces a CSV with one row per eviction case. The columns are:

| Column | What it is |
|---|---|
| **name** | The defendant (tenant) named on the case |
| **address** | Street address from the docket |
| **city state zip** | City, state, and ZIP |
| **case number** | The court case number (e.g. `26CI9999999`) |
| **county** | The county the case is in |

## Example

```csv
name,address,city state zip,case number,county
Jordan Rivera,123 Example Street Apt. 4,Omaha NE 68100,26CI9999999,Douglas
```

## Notes on the data

- **Multiple defendants:** when a case lists more than one named defendant, additional
  names are combined into the address/name fields as the court records them.
- **Placeholder parties** like "All other occupants", "John Doe", or "Real Name Unknown"
  are skipped — only real named parties are kept.
- **Odd spacing or a stray typo** (e.g. a doubled letter in a city name) generally comes
  straight from the court's docket page. The app cleans up column placement where it can,
  but it doesn't invent or correct the source text.
- **Blank address fields** mean the docket didn't list a parseable address for that party.

## Using it

The CSV opens directly in Excel, Google Sheets, or any mail-merge / outreach tool — it's
plain comma-separated values with a header row.
