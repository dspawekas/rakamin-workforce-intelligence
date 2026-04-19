# Workforce Intelligence Platform
### Rakamin PM Case Study — Medika Nusantara

A working prototype demonstrating how a data reconciliation and AI enrichment layer transforms fragmented enterprise HR data into actionable workforce intelligence.

---

## 🔗 Live Prototype

**[→ Open Prototype](https://dspawekas.github.io/rakamin-workforce-intelligence/prototype/)**

> Single-file SPA. No login required. Best viewed on desktop (1280px+).

---

## 📁 Repository Structure

```
├── prototype/
│   └── index.html          # Self-contained SPA — all logic & data embedded
│
└── dataset/
    ├── medika_nusantara_dataset_A_messy.json   # 553 raw records across 3 systems
    └── medika_nusantara_dataset_B_clean.json   # 200 unified, AI-enriched records
```

---

## 🧠 What the Prototype Demonstrates

| Feature | Description |
|---|---|
| **Raw ↔ Clean Toggle** | Side-by-side comparison of pre/post data reconciliation |
| **Identity Resolution** | 553 raw records → 200 unique employees via multi-key matching |
| **Date Conflict Detection** | 304+ records with conflicting join dates (HRIS vs ATS) highlighted in real-time |
| **AI Skill Inference** | 45 inference rules with transparent "why" tooltips on each inferred skill |
| **Confidence Scoring** | Per-record scores driving Reskill (≥75%) vs Verify (<75%) action routing |
| **Human-in-the-Loop** | One-click skill verification with model feedback loop |
| **Reskilling Roadmap** | 51 employees auto-triaged into 3 learning tracks |

---

## 📊 Dataset Notes

**Dataset A (Messy)** reflects real enterprise data conditions:
- 44% missing skill fields
- 74 job title variations for 12 actual roles
- 3 incompatible date formats across systems (SAP / Workable / Moodle)
- Duplicate-ish identities with slightly different names and IDs

**Dataset B (Clean)** is the post-processing output:
- Normalized roles against a standard taxonomy
- Skills inferred via collaborative peer-group modeling
- Confidence scores + human review flags on every record

---

## 🛠️ Tech Stack

Built as a single HTML file with zero backend dependencies.

- **UI:** Tailwind CSS (CDN) + Lucide Icons
- **Data:** Hardcoded JSON arrays (production would replace with API)
- **Logic:** Vanilla JavaScript — no frameworks

---

*Submitted as part of the Rakamin AI-Native PM hiring process. Built with Claude (Anthropic) + Antigravity.*
