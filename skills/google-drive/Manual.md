# Google Drive setup

This skill contains instructions, not an account connection. Each user connects their own Google account before an agent can share files.

## Preferred setup: connected integration

Connect the Google Drive integration in the agent's environment and grant its requested access to the account that owns or can share the file. Verify that the integration supports reading file metadata and creating user permissions. If it does not support permission creation, use the API setup below.

## API setup

1. In a Google Cloud project you control, enable the Google Drive API, configure the OAuth consent screen, and create an OAuth client for the local application you will use.
2. Authorize the Drive account interactively and store the client credentials and refresh state in local ignored storage or a secret manager. Never place them in this repository or send them to the agent in chat.
3. Request the narrowest useful scope. `https://www.googleapis.com/auth/drive.file` can modify files created or explicitly opened with the app; it will not automatically expose every existing Drive file. Use a broader Drive scope only when the user understands and needs that access.
4. Check that the client can read the intended file's metadata and `capabilities.canShare`. Then share only the specified file with the specified email and verify the permission.

The file owner can revoke the app's access in their Google Account's third-party connections and revoke a recipient's access in the file's Drive sharing settings. Delete local OAuth credentials and refresh state when retiring the setup.

Official references: [sharing files](https://developers.google.com/workspace/drive/api/guides/manage-sharing), [permission creation](https://developers.google.com/workspace/drive/api/reference/rest/v3/permissions/create), and [Drive scopes](https://developers.google.com/workspace/drive/api/guides/api-specific-auth).
