# Running a scrape

From the **dashboard** (Run Scrape), you start an on-demand run and watch it work in
real time.

## Steps

1. **Choose counties.** Select one or more counties whose calendars you want to pull.
2. **Choose the hearing date.** Pick the day's calendar to retrieve — today or a number
   of days ahead. This is the **court hearing date**, not today's date.
3. **Start the run.** Progress streams live in the output area below.

## What you'll see

The run goes through two stages:

```
Queued. Waiting for the browser to fetch the calendar…
Calendar fetched: 3 eviction case(s) found. Retrieving dockets…
Found 3 eviction case(s). The court's docket server is slow (~30s each),
  so this will take about 2 min. Starting…
[1/3] Douglas 26CI0013728 — requesting docket from the court…
[1/3] Douglas 26CI0013728 — docket received in 28s, reading address…
[1/3] ✓ Antonio K Caraballo — 4512 Bedford Avenue Apt. 11
[2/3] …
Done — extracted 3 of 3 case(s) into the CSV.
```

- **Calendar stage** finds the eviction cases scheduled for that date in your counties.
- **Docket stage** opens each case and reads the defendant's name + address. This is the
  slow part — each docket goes through the courts' E-Services site (~30s each).

When it finishes, a **Download CSV** option appears.

!!! note "Pick a date the court has actually calendared"
    Eviction hearings are scheduled for upcoming weekdays. Choosing today (before
    hearings are posted), a weekend, or a holiday will usually return **0 cases** —
    that's expected, not a failure. See the [FAQ](faq.md#why-did-my-run-return-0-cases).

## Be considerate of the court's servers

It's real court infrastructure. Pull what you need — a few counties, a few times a day
— rather than everything, constantly. The app paces its requests deliberately.

Next: **[Read the CSV](reading-the-csv.md)**.
