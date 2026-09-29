# Sentinel Skills conventions

This repository contains portable general-case skills. A skill folder contains exactly:

- `<Skill_Name>.md` - the shareable skill instructions.
- `Manual.md` - user-facing setup, token creation, and first-use instructions.

Do not commit live tokens, OAuth refresh tokens, account identifiers, private URLs, personal data, local absolute paths, `.env` files, certificates, or credential directories. Document variable names and token scopes only. Each skill should state exactly where users place credentials locally and how they can revoke them.

Keep skills narrowly scoped, use lowercase hyphenated folder names, and verify both files before publishing.

The `google-drive` skill covers sharing one existing Drive file with a named recipient. Its manual explains the required account connection; the skill document itself does not grant Drive access.
