# Google Calendar

Use the official Google Calendar API or the recipient's configured local client. Event data and authentication state are private.

- Read calendar data directly when the user asks.
- Before creating, changing, or deleting an event, confirm the exact calendar, timing, and effect when they are not already explicit.
- Use the user's configured time zone and default calendar unless they specify otherwise.
- Read credentials from local secret storage only. Never print, commit, or include them in requests or reports.
