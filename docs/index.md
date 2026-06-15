# Nebraska Eviction Scraper

A web app for tenant-advocacy outreach that pulls **eviction-case calendar and
docket data** from Nebraska Courts E-Services and gives you a clean CSV of
defendants and their addresses.

You sign in, pick the counties and the hearing date you care about, and the app
gathers the cases and the address on each docket — work that used to be done by
hand, one case at a time.

## What you can do

- **[Run a scrape](running-a-scrape.md)** on demand and download the results as a CSV.
- **[Schedule](scheduling.md)** it to run automatically on the days/times you choose,
  with the CSV emailed to you.
- Store your **Justice E-Services credentials** once (encrypted) so the app can fetch
  dockets on your behalf.

## Quick start

1. **[Get an account & sign in](getting-started.md)** — accounts are created by an
   administrator; there's no open sign-up.
2. Add your **E-Services credentials** on the Credentials page.
3. **[Run a scrape](running-a-scrape.md)** for a county and an upcoming hearing date.
4. **[Read the CSV](reading-the-csv.md)** — name, address, city/state/zip, case
   number, county.

!!! note "It can be slow — that's the court's server"
    Pulling each docket goes through the courts' E-Services site, which is slow
    (often ~30 seconds per case). The progress log keeps you posted case by case;
    a run with many cases simply takes a while.

Stuck? See the **[FAQ & troubleshooting](faq.md)**.
