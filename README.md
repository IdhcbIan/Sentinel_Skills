# Sentinel Skills

Shareable, ready-to-adapt skills for SENTINEL. Every published skill is self-contained and safe to clone: credentials, account identifiers, private endpoints, user data, and local paths do not belong in this repository.

## Available skills

| Skill | What it covers | Setup |
| --- | --- | --- |
| [Firebase](skills/firebase/Firebase.md) | Working with Firebase projects and data using local credentials. | [Manual](skills/firebase/Manual.md) |
| [Gmail](skills/gmail/Gmail.md) | Reading, drafting, and sending mail through an authorized account. | [Manual](skills/gmail/Manual.md) |
| [Google Calendar](skills/google-calendar/Google_Calendar.md) | Reading calendars and managing events. | [Manual](skills/google-calendar/Manual.md) |
| [Google Drive](skills/google-drive/Google_Drive.md) | Sharing a specific Drive file with a named person. | [Manual](skills/google-drive/Manual.md) |
| [LaTeX compilation](skills/latex-compilation/LaTeX_Compilation.md) | Compiling and checking LaTeX documents. | [Manual](skills/latex-compilation/Manual.md) |
| [Modal GPU](skills/modal-gpu/Modal_GPU.md) | Running requested workloads on Modal. | [Manual](skills/modal-gpu/Manual.md) |
| [WhatsApp Baileys](skills/whatsapp-baileys/WhatsApp_Baileys.md) | Using an existing local Baileys integration during an active conversation. | [Manual](skills/whatsapp-baileys/Manual.md) |

## Repository layout

```text
Sentinel_Skills/
├── skills/             Sanitized, general-purpose skills ready to share
│   ├── google-calendar/
│   ├── whatsapp-baileys/
│   ├── gmail/
│   ├── google-drive/
│   ├── modal-gpu/
│   ├── firebase/
│   └── latex-compilation/
├── Skill_Folder/       Copy this folder to start a new skill
│   ├── Skill_Template.md
│   └── Manual.md
└── Docs/               Repository conventions
```

Every published skill folder contains exactly two files: `<Skill_Name>.md`, containing the skill, and `Manual.md`, containing setup instructions. The collection is deliberately general: users bring their own account, local configuration, and tokens as described in the manual.

To create another skill, copy `Skill_Folder`, rename the skill document, and complete its `Manual.md`. See [the template manual](Skill_Folder/Manual.md) for setup and sharing rules.
