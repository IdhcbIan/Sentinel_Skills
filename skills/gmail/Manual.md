# Gmail manual

1. Enable Gmail API access in an official Google Cloud project.
2. Create OAuth client credentials for your local application.
3. Complete the authorization flow locally and save resulting credential state in ignored storage.
4. Begin with read-only scopes; add compose or send access only if your workflow requires it.
5. Test a read-only request before using a draft or send action.

Revoke the OAuth grant through account-security settings when access should end. Do not place account names, tokens, messages, or recipients in this repository.
