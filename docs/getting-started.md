# Getting started

## Getting an account

Accounts are created by an **administrator** — there's no public sign-up. Ask your
admin to add you. You'll be set up with one of two roles:

- **Advocate** — run scrapes, set your own schedule, manage your own credentials.
- **Admin** — all of the above, plus creating and managing other users.

## Signing in

Open the app and sign in one of two ways, depending on how your account was created:

- **Email + password** — the credentials your admin gave you. Change your password
  from the **Change Password** page after your first login.
- **Single sign-on (Google or Microsoft)** — click the SSO button; the email on your
  identity provider must match the email your admin used.

!!! tip "Forgot your password?"
    Use the **Forgot Password** link on the sign-in page to get a reset link by email
    (if email is enabled for your deployment).

## Add your E-Services credentials

To fetch dockets, the app signs in to **Nebraska Justice E-Services as you**, using
credentials you provide once:

1. Go to the **Credentials** page.
2. Enter your **E-Services username and password**.
3. Save.

Your E-Services password is **encrypted at rest** — it's stored only so the app can
fetch dockets on your behalf, and it's never shown back to you in plain text.

Without valid E-Services credentials, the calendar step can still find cases, but the
docket step will fail (you'll see a login-rejected error).

Next: **[Run a scrape](running-a-scrape.md)**.
