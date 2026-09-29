# Google Calendar manual

1. Create a project in the official Google Cloud console and enable Google Calendar API access.
2. Create OAuth client credentials for the local client type you use.
3. Complete authorization locally and save credential state in an ignored local directory or secret manager.
4. Configure a default calendar and time zone locally, outside this repository.
5. Test a read-only listing before allowing event writes.

Request the smallest suitable scope. Revoke authorization from the Google account security settings if the device or token is exposed.
