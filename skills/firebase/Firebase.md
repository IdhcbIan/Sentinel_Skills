# Firebase

Use official Firebase tooling and locally stored credentials. Projects, service accounts, user data, database contents, and deployment details are private.

- Prefer read-only inspection where possible.
- Confirm the exact target and effect before deployment, data writes, deletes, or permission changes.
- Use the least-privileged role and local secret storage.
- Never print or commit service-account material, API keys, project identifiers, or user data.
