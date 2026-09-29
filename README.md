# Sentinel Skills

Shareable, ready-to-adapt skills for SENTINEL. Every published skill is self-contained and safe to clone: credentials, account identifiers, private endpoints, user data, and local paths do not belong in this repository.

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
