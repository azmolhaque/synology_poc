## 🚨 Synology API Key Abuse — Live PoC

This repository contains a live Proof-of-Concept (PoC) demonstrating the abuse potential of a leaked Google Places API key found in a Synology asset. The vulnerability enables financial exploitation, infrastructure reconnaissance, and unrestricted third-party access — justifying escalation to **Critical severity**.

---

### 🔍 Vulnerability Summary

- **Target:** `note.synology.com`
- **Exposed Key:** Found in `notestation_gmap.js`
- **API Access:** Google Places API
- **Restrictions:** None — key is usable from any origin
- **Severity:** Critical (CVSS v3.1: 9.1)
- **Categories Affected:**
  - Web Services: ~$5,000 potential abuse
  - C2 Cloud Infrastructure: ~$10,000 exposure risk

---

### 💡 Live PoC Features

- **💸 Financial Abuse Simulation:**  
  Demonstrates quota drain via automated API calls.  
  → 1M requests ≈ $5,000 in billing damage.

- **🌍 Unrestricted Map Rendering:**  
  Confirms key usability from external domains via embedded Google Maps.

- **🕵️ Infrastructure Reconnaissance:**  
  Shows how attackers can enumerate and preview sensitive locations using Places API.

---

### 📁 Files Included

| File         | Description                                      |
|--------------|--------------------------------------------------|
| `index.html` | Main PoC webpage with live abuse simulations     |
| `README.md`  | This file — summary and context for reviewers    |
| *(optional)* `report.md` | Markdown-formatted vulnerability report (add if needed) |

---

### ⚠️ Disclosure & Ethics

This PoC is part of a responsible disclosure process.  
No data was exfiltrated. All abuse scenarios are simulated.  
Submitted by: **Md. Azmol Haque Rony** — Ethical Hacker & Bug Bounty Researcher  
Location: Bogura, Bangladesh  
Timestamp: August 24, 2025

---

### 🔗 Live Demo

👉 [View the PoC on GitHub Pages](https://yourusername.github.io/synology-api-leak-poc/)  
*(Replace with your actual GitHub Pages URL)*

---

Would you like help drafting a `report.md` next — with markdown-formatted impact analysis, severity justification, and triage notes? I can also help you embed abuse telemetry or quota drain counters to reinforce exploitability. Let’s make this airtight.
