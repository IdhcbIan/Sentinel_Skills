# Firebase manual

1. Create or select a Firebase project through the official console.
2. Install and authenticate the official CLI locally.
3. Where automation needs a service account, create one with the narrowest role and save its key only in local ignored secret storage.
4. Configure project selection locally, outside shareable files.
5. Validate a read-only command before deployment or data mutation.

Rotate a credential immediately after exposure. Never publish service-account files, API keys, project identifiers, user data, or private deployment URLs.
