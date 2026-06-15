# Scheduling automatic runs

Instead of starting runs by hand, you can have the app run on a schedule and **email
you the CSV**. Each user sets their own schedule.

## Set it up

On the **Schedule** page, choose:

- **Enabled** — turn your schedule on or off.
- **Weekdays** — which days of the week to run (e.g. Mon–Fri).
- **Time** — the hour to run, in your timezone.
- **Counties** — which counties to include.
- **Which day's calendar** — today, or N days ahead (e.g. "3 days ahead" to pull the
  calendar for hearings three days out).

Save, and you're done. The app checks schedules every hour and runs yours when it's due.

## Getting the results

When a scheduled run finishes, the CSV is **emailed to you** as an attachment. If a run
hits an error, you'll get an email about that instead, so you're never left guessing.

!!! note "Email must be configured"
    Scheduled-run delivery and password-reset emails require your deployment's
    administrator to have set up email. If you're not receiving scheduled results, check
    with your admin. (On-demand runs don't need email — you download those directly.)

## Tips

- Schedule a few days ahead so the court has posted the hearing calendar by the time the
  run fires.
- Keep the county list focused — large counties have many cases, and each docket is slow
  to fetch (see [Running a scrape](running-a-scrape.md)).
