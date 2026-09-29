# Gmail

Use official Gmail APIs or the recipient's configured local client. Mail content, recipients, and authentication state are private.

- Read and search messages only for the locally authorized mailbox.
- Draft when asked, but never send unless the user explicitly authorizes sending the final message to the stated recipient in the current session.
- Use the minimum OAuth scopes required for the requested action.
- Never expose tokens, account identifiers, message contents, or recipient addresses outside the authorized task.
