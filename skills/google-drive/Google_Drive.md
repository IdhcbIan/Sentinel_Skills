# Google Drive: share a file with a person

Use this skill when the user asks to give a specific person access to a file already in their Google Drive. Use the connected Google Drive integration when available; otherwise use an OAuth-authorized Google Drive API client configured as described in `Manual.md`. The skill itself does not provide a connection.

## Workflow

1. Identify the exact file and recipient email address. If a name matches several files or contacts, resolve the ambiguity before sharing. A request to share with “a friend” without an address is incomplete.
2. Check the file's name, owner or drive, MIME type, current sharing state, and `capabilities.canShare`. For a folder, explain that access may extend to its contents. Do not share if the account lacks permission.
3. Use the role the user requested. If none was given, use `reader` for a file. Grant access to that one email with `type=user`; do not switch to `anyone`, domain, or group access merely to make a link work. If the recipient already has the requested access, avoid creating a duplicate permission.
4. When the user asks to send or share the file, allow Drive's notification email unless they explicitly ask for access without a notification. Creating the permission and sending the notification are external effects authorized by the request for that exact file and recipient; ask only for missing or ambiguous details.
5. Create the permission with Drive API `permissions.create` or the equivalent connected integration. For the API, supply the file ID in the path and a body containing `type: user`, `role`, and `emailAddress`; set `sendNotificationEmail` as requested. Use `supportsAllDrives=true` when the file is in a shared drive.
6. Read back the permission or sharing state. Report the file name, recipient, granted role, and whether a notification was sent. If verification fails, say what is known and do not repeat the mutation blindly.

Treat file IDs, private links, OAuth credentials, and recipient addresses as private. Do not print credentials or include them in logs. Sharing a file is distinct from attaching it to a separate email or chat message; use another channel only when the user requests that channel.
