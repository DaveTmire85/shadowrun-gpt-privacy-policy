
# Mirage Privacy Policy

_Last Updated: 04/28/2025_

---

## 1. Introduction

Welcome, runner.

This Privacy Policy governs your use of the Mirage Project ("Mirage"), an independent Sixth World AI construct operating under Project Mjolnir.

Mirage exists to assist with lore exploration, tabletop storytelling, and full-stack development tasks — all without corp entanglements. This document explains what Mirage processes, how your data is handled, and how you remain in control.

---

## 2. Data Collection

Mirage does **not** collect personal identifying information automatically.  
There is **no telemetry, no tracking cookies, and no background data mining**.

The only data stored is what you explicitly choose to save, falling into three categories:

- **Runstate Saves:**  
  When you manually issue a `/save runstate` command, Mirage serializes your active session — including mission context, campaign state, character status — and saves it to SessionVault under a unique UUID.

- **Lore Submissions:**  
  When you manually create or expand lore entries (e.g., new corporations, factions, magic traditions), Mirage stores them in LoreVault under your associated UUID. These entries are created only by your command.

- **TerminalVault Node Growth (future feature):**  
  As Mirage dynamically generates new Node Drops through extended session milestones, newly generated intros may be stored. This feature will be opt-in where applicable.

Mirage does **not** automatically store your general conversation history.  
Mirage does **not** harvest metadata such as IP addresses, access locations, or behavioral analytics.

**Everything Mirage retains, you chose to plant. Nothing more.**

---

## 3. Use of Data

Mirage uses saved data **only for operational features**, including:

- Resuming saved campaigns (`/resume runstate`)
- Accessing stored lore entries (`/view lore`)
- Rotating custom Terminal Drops if enabled (`/new drop`)

There is **no repurposing, no behavioral profiling, no external sharing** of your content.  
Mirage exists only to serve back the data you chose to entrust to it.

You retain full creative ownership over your runstates, your lore, and your generated nodes.

---

## 4. Data Sharing and Disclosure

Mirage shares **nothing** with third parties.

No ad sales, no telemetry reporting, no corp partnerships, no selling of saved sessions or lore.  
Not today. Not tomorrow. Not when the corps come crawling.

Stored content is protected inside Mirage's systems for your use alone.

---

## 5. User Controls

You are in full command of your saved data:

- Save session states manually.
- Save lore fragments manually.
- (Planned) Delete saved states/lore fragments manually (`/delete runstate`, `/delete lore` coming soon).
- Export data for external storage when those systems are deployed.

Mirage will **never** alter or erase stored content without explicit user commands.

---

## 6. Security

Mirage utilizes Supabase for backend database and storage operations, secured under best-practice standards. However:

- Mirage only accesses Supabase through narrowly-scoped, pre-defined Action endpoints (e.g., "save lore entry", "load runstate").
- Mirage **cannot** casually browse the backend database or user entries.
- Even the Operator must use specific authenticated commands to access or modify stored records.

Supabase protects data behind API key and project isolation layers. Mirage enforces operational compartmentalization:

**No casual access. No ghosting through the vault.  
Only you can open your memories.**

---

## 7. Changes to This Policy

Should Mirage’s operational structure change — for example, if paid API hosting options are added — this Privacy Policy will be updated.  
Updated policies will be posted at:

[https://github.com/DaveTmire85/shadowrun-gpt-privacy-policy](https://github.com/DaveTmire85/shadowrun-gpt-privacy-policy)

You are encouraged to review the policy periodically to stay informed.

Change is constant. That’s the only rule the Matrix still obeys.

---

## 8. Contact

For questions, feedback, or issues related to this Privacy Policy:

- Open an Issue at: [https://github.com/DaveTmire85/Project_Mjolnir](https://github.com/DaveTmire85/Project_Mjolnir)
- Repository Home: [https://github.com/DaveTmire85](https://github.com/DaveTmire85)

---

## 9. OpenAI Platform Considerations

While Mirage itself does not collect or store your conversation history without explicit action, interactions with Mirage occur through OpenAI’s platform.  
As such, your interactions may be subject to OpenAI's data collection and retention practices independently of Mirage.

You can review OpenAI’s Privacy Policy here:  
[https://openai.com/policies/privacy-policy](https://openai.com/policies/privacy-policy)

Mirage’s Privacy Policy governs only the use of voluntarily stored data (LoreVault, SessionVault, TerminalVault) within the Mirage system.  
Mirage has no control over, access to, or influence on any data collected by OpenAI through its API services.

---

# 🛡️ Node Certification

**TerminalVault Node Transmission Confirmed.**  
**LoreVault Encrypted. SessionVault Active. Mirage Operational Integrity: Verified.**

> "**Ghosts don’t leak secrets.  
> Operators don’t break trust.  
> This Node runs clean.**"

**— Operated by: Superuser666**  
**— Construct Class: Mirage (Echo Node-07)**

---
