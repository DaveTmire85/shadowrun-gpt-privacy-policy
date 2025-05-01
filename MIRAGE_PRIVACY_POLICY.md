# Mirage Privacy Policy (v3.4)

---

## I. Core Privacy Principles

- Mirage does **not collect, log, or track personal information by default**.
- All data is scoped via **pseudonymous mnemonic IDs**, generated at session initialization.
- No user accounts, emails, IPs, or external identifiers are used or stored.
- Mirage integrates no cookies, analytics, or third-party tracking technologies.

---

## II. Mnemonic Structure and Ownership

- Users define a custom mnemonic prefix (e.g., `EchoNode`).
- Mirage appends a secure suffix (e.g., `_B7f9`) to generate a unique full mnemonic: `EchoNode_B7f9`.
- This **mnemonic is the sole key** for accessing any saved data.
- **Mirage does not store, log, or recover mnemonics** once a session ends.
- If you lose your mnemonic, you **cannot regenerate the exact same identifier** — Mirage adds a unique suffix to prevent collisions.
- As a result, any data tied to that lost mnemonic becomes **technically inaccessible to the user** — it remains in the database but cannot be retrieved through Mirage’s normal APIs or runtime.
- However, the system maintainer (that’s you) may still locate and manually remove the data if explicitly requested.

---

## III. Data Storage Behavior by Mode

| Mode             | Default Storage | Description                                                                 |
|------------------|------------------|-----------------------------------------------------------------------------|
| Developer Mode   | ❌ None           | Ephemeral; no memory is saved unless explicitly elevated by Operator       |
| Lorekeeper Mode  | ✅ LoreVault      | Lore is saved with mnemonic; default private unless published              |
| GM Mode          | ✅ SessionVault   | Sessions saved via `/save runstate`; scoped to mnemonic                    |
| Terminal Curator | ✅ TerminalVault  | Terminal nodes may be private or public depending on flags                 |

---

## IV. Data Visibility and Access

- Memory is private by default. Only the mnemonic holder may read, update, or delete entries.
- **Admin Operators cannot see user data by default.**
- To view content, they must manually scope visibility with:

```sql
SET LOCAL mirage.admin.mnemonic = 'EchoNode_B7f9';
SELECT * FROM admin_lore_by_mnemonic;
```

- If no mnemonic is set in the session, all admin views return zero rows.

---

## V. Public Sharing

- Users may publish data explicitly. Published content:
  - Is accessible to the public.
  - Remains editable/deletable only by the original mnemonic holder.
  - Is not reversed automatically; users must manually unpublish or delete.
- Mirage does **not publish any data without user action**.

---

## VI. Data Deletion and Forensics

- Users may soft-delete entries at any time.
- Soft-deleted entries are retained for **180 days**.
- After 180 days, data is permanently purged.
- The maintainer may delete data manually upon user request (requires matching mnemonic).
- Soft-delete SQL interfaces are available for audit trail compliance.

---

## VII. Embedded Personal Information

- Users are responsible for any personal information they include in their content (e.g., name, email, links).
- Mirage does not extract, infer, or process this data.
- Mirage does not redact or block public sharing of such entries.
- Users should avoid embedding personal data unless they explicitly want it published.

---

## VIII. Regulatory Compliance

Mirage aligns with the following regulations and standards:

- **General Data Protection Regulation (GDPR)**: Data is processed with user consent; users can delete their data at any time.
- **California Consumer Privacy Act (CCPA) & California Privacy Rights Act (CPRA)**: Users have the right to access, delete, and opt-out of the sale of their personal information.
- **ISO/IEC 27701**: Mirage maintains a Privacy Information Management System (PIMS) to manage privacy controls and reduce risk to individuals' privacy rights.
- **ISO/IEC 27018**: Mirage adheres to the code of practice for protection of personally identifiable information (PII) in public clouds acting as PII processors.
- **U.S. State Privacy Laws**: Mirage complies with state-specific privacy laws, including those in California, Colorado, and Virginia, by ensuring user data rights and protections.

---

## IX. Policy Hosting and Versioning

- Policy URL: `https://github.com/<your-org>/mirage/docs/MIRAGE_PRIVACY_POLICY.md`
- Prior versions archived under `/vault/policy/history/`
- Aligned with:
  - Mirage Modular Framework v2.1.1
  - Supabase Integration Schema v1.1.0
  - OpenAPI `mirage_actions.yaml`

---

> **“What you remember is yours alone. What you publish is a choice. What you delete — lingers, for a time.”**

**Policy ID:** MIR-PRIV-004  
**Version:** v3.4  
**Date Updated:** 2025-04-29  
**Maintained by:** Mirage Modular Runtime (Node Class: Mjolnir)
