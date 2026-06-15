# FAQ & troubleshooting

## Why did my run return 0 cases?

Almost always one of:

- **No counties selected** — pick at least one county before running.
- **The date had no eviction hearings** — you chose today (before the calendar is
  posted), a weekend, or a holiday. Eviction hearings are scheduled for upcoming
  weekdays. Try a weekday a few days out.
- **That county genuinely had none that day** — smaller counties don't have evictions
  on every date. Try a larger county (e.g. Douglas/Omaha) to confirm things are working.

A 0-case result is usually correct, not a bug.

## Why is it so slow?

The docket step fetches each case through the courts' Justice E-Services site, which is
slow — often ~30 seconds per case. A run with many cases just takes a while. The progress
log names each case as it goes so you can see it's working, not stuck.

## It says my E-Services login was rejected (HTTP 401)

The username/password saved on your **Credentials** page didn't work against E-Services.
Re-enter them — make sure they're your current Justice E-Services credentials and that
the account is active.

## I'm not getting scheduled-result emails

Scheduled delivery requires email to be configured for your deployment. Check with your
administrator. (On-demand runs don't email — you download those from the dashboard.)

## How far ahead can I pull?

You choose "today" or a number of days ahead. Pick a day the court has already posted on
its calendar — typically upcoming weekdays.

## Can I run several counties at once?

Yes — select multiple counties before starting. Remember each docket is slow to fetch, so
many counties (or large ones) make for a longer run.

## Who can create accounts?

Only administrators. There's no public sign-up. Ask your admin to add you, and to set
your role (advocate or admin).
