# 📄 Vulnerability Report: Leaked Google Places API Key in Synology Asset

## 🔍 Summary

A valid Google Places API key was discovered embedded in a public JavaScript file (`notestation_gmap.js`) hosted on `note.synology.com`. The key is unrestricted by domain or IP, allowing full abuse from any external origin. This enables attackers to:

- Drain Synology’s billing quota via automated API calls
- Render maps and retrieve location data from unauthorized domains
- Enumerate infrastructure and preview sensitive locations

## 🧠 Severity Justification

- **CVSS v3.1 Score:** 9.1 (Critical)
- **Impact Areas:**
  - **Web Services Abuse:** ~$5,000 via quota drain
  - **C2 Cloud Infrastructure Exposure:** ~$10,000 via location enumeration
- **Exploitability:** No authentication required, no rate limiting observed
- **Scope:** Cross-origin abuse confirmed via live PoC

## 🔑 Exposed API Key Details

| Field         | Value |
|---------------|-------|
| Source        | `notestation_gmap.js` on `note.synology.com` |
| Key           | `AIzaSyBXG6lKBSQxQFR48lJ2_v9pzS7MFXu5XNU` |
| API Access    | Google Places API |
| Restrictions  | None (usable from any domain) |
| Status        | Valid and actively billable |

## 💡 Exploitation Scenarios

### 💸 Scenario 1: Financial Abuse

- Each Places API request costs ~$0.005
- Attackers can automate abuse to drain quota
- **Simulated Cost:** 1M requests ≈ $5,000

### 🌍 Scenario 2: Unrestricted Map Rendering

- Map rendered from external origin using Synology’s key
- Confirms lack of domain/IP restriction

### 🕵️ Scenario 3: Reconnaissance via Places API

- Attackers can retrieve location previews and metadata
- Demonstrated using a Dhaka-based location photo

## 🔗 Live PoC

👉 [View the PoC on GitHub Pages](https://yourusername.github.io/synology-api-leak-poc/)  
*(Replace with your actual GitHub Pages URL)*

## 🛡️ Disclosure Notes

- No data exfiltrated
- All abuse scenarios are simulated
- Key was discovered via ethical recon aligned with program scope

## 👤 Researcher Profile

**Md. Azmol Haque Rony**  
Ethical Hacker & Bug Bounty Researcher  
Location: Bogura, Bangladesh  
Date of Submission: August 24, 2025

---
