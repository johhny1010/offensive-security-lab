# Security and publication policy

This repository is an offensive-security lab reference project for disposable, explicitly scoped owned guests. It ships offline analysis and a command planner; no network scanning, hypervisor access, target deployment, exploitation or policy modification occurs when running the Python code.

The planner emits private addresses supplied by the operator. Do not publish its output. The scope declaration is a local input constraint, not an independent authorization service or a containment mechanism. RFC1918 addresses are not automatically safe targets; ownership, isolation and exclusions must still be established.

Public fixtures use documentation-only addresses. The synthetic mode is refused by the live command planner. Real target addresses, VLAN IDs, bridge IDs, guest IDs, GPU UUIDs, OPNsense exports, Proxmox configuration, credentials, browser sessions, cookies and raw captures are excluded.

The parser uses only a bounded subset of XML and report fields. This reduces accidental disclosure but is not a general anonymizer or forensic authenticity check. Source hashes and alias-only service information remain metadata; review them before sharing. No report field should be interpreted as proof of a vulnerability or completed remediation.

Run the tests and `python scripts/check_publication.py`, inspect staged changes, and use a maintained secret scanner over the complete Git history before publishing. The supplied checker is intentionally limited and may produce false positives. `.gitignore` does not protect already tracked files. If a credential is exposed, rotate it promptly; deleting the latest copy does not erase history.

Do not post real vulnerability details, private logs or credentials in public issues. Use a private reporting channel appropriate to the affected system owner. This project has no separate managed disclosure service or production support commitment.
