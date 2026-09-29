# WhatsApp Baileys manual

1. Install the documented Baileys integration and its dependencies locally.
2. Start one local daemon or client process.
3. Link the device by scanning its QR code from the account holder's WhatsApp application.
4. Store all linked-device state in an ignored local `auth/` directory.
5. Verify connection status with the local integration before use.

Never copy, commit, inspect manually, or share the session directory. The account holder can remove access through WhatsApp linked-device settings.
