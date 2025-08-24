# 🚨 Multi-Vector Vulnerability Disclosure

## 🎯 Target Asset
**Synology Web Services & C2 Cloud Infrastructure**

## 🧠 Severity
- **CVSS v3.1 Score:** 9.1 (Critical)
- **Categories Affected:**
  - Web Services Abuse: ~$5,000
  - C2 Cloud Infrastructure Exposure: ~$10,000

---

## 🔑 Exposed API Key

| Field       | Value |
|-------------|-------|
| Source      | `notestation_gmap.js` on `note.synology.com` |
| Key         | `AIzaSyBXG6lKBSQxQFR48lJ2_v9pzS7MFXu5XNU` |
| API Access  | Google Places API |
| Restrictions| None — usable from any domain |
| Status      | Valid and billable |

---

## 💡 Exploitation Scenarios

### 💸 Scenario 1: Financial Abuse Simulation
- Each Places API request costs ~$0.005
- Attackers can automate abuse to drain Synology’s quota
- **Live Simulation:** 10,000 requests
- **Estimated Cost:** $0.00 (simulated)
- **At Scale:** 1M requests ≈ $5,000

### 🌍 Scenario 2: Unrestricted Access
- Map rendered from external origin using Synology’s key
- Confirms lack of domain/IP restriction

### 🕵️ Scenario 3: Reconnaissance via Places API
- Attackers can retrieve location previews and metadata
- Demonstrated using a Dhaka-based location photo

---

## ⚠️ Responsible Disclosure Statement

This PoC is part of a responsible disclosure process.  
No data was exfiltrated. All abuse scenarios are simulated.  
All testing was conducted within ethical boundaries and program scope.

---

## 👤 Researcher Profile

**Md. Azmol Haque Rony**  
Ethical Hacker & Bug Bounty Researcher  
Location: Bogura, Bangladesh  
Timestamp: August 24, 2025
