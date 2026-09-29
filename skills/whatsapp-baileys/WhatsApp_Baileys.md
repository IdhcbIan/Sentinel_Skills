# WhatsApp Baileys

Use the recipient's existing local Baileys integration. Messages, contacts, groups, media, and linked-device state are private.

- Use only while the account holder is actively interacting with the agent.
- Use the shared local daemon or client, never a second concurrent device socket.
- Do not inspect or modify session files directly.
- Send a message only after the account holder confirms the exact recipient and exact message content in the current session.
- Do not use this skill for scheduled, unattended, or background work.
