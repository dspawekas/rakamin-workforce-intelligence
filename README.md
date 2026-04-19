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
│   └── index.html                              # Self-contained SPA — all logic & data embedded
│
└── dataset/
    ├── medika_nusantara_dataset_A_messy.json   # 553 raw records across 3 systems
    ├── medika_nusantara_dataset_A_messy.csv    # CSV version of Dataset A
    ├── medika_nusantara_dataset_B_clean_v2.json  # 200 unified, AI-enriched records + inference_reason
    └── medika_nusantara_dataset_B_clean_v2.csv   # CSV version of Dataset B
```

---

## 🧠 What the Prototype Demonstrates

| Feature | Description |
|---|---|
| **Raw ↔ Clean Toggle** | Side-by-side comparison of pre/post data reconciliation |
| **Identity Resolution** | 553 raw records → 200 unique employees via multi-key matching |
| **Date Conflict Detection** | Records with conflicting join dates (HRIS vs ATS vs LMS) highlighted in real-time |
| **AI Skill Inference** | 45 inference rules with transparent "why" tooltips on each inferred skill |
| **3-Tier Confidence System** | AI Verified (≥80%) · Needs Validation (70–80%) · Data Incomplete (<70%) |
| **Human-in-the-Loop** | One-click skill verification with model feedback loop and full audit trail |
| **Reskilling Roadmap** | Employees auto-triaged into 3 learning tracks based on role and skill profile |

---

## 📊 Dataset Notes

**Dataset A (Messy)** reflects real enterprise data conditions:
- ~40% missing skill fields
- Multiple inconsistent job title variants for the same role (e.g., "BM", "Kepala Cabang", "Manager Cabang", "Branch Mgr" — all referring to Branch Manager)
- 3 incompatible date formats across systems (SAP / Workable / Moodle)
- Duplicate-ish identities with slightly different names and IDs across systems

**Dataset B v2 (Clean)** is the post-processing output:
- Normalized roles against a standard workforce taxonomy
- Skills inferred via collaborative peer-group modeling
- `inference_reason` field attached to every inferred skill — explaining the pattern logic behind each inference
- Confidence scores (0.0–1.0) + human review flags on every record

---

## 🛠️ Tech Stack

Built as a single HTML file with zero backend dependencies.

| Layer | Technology |
|---|---|
| **Structure** | HTML5 (Semantic) |
| **Styling** | Vanilla CSS (Custom Design System, Dark Mode, Glassmorphism) |
| **Logic** | Vanilla JavaScript (ES6+) |
| **Data** | JSON (dataset loading & parsing) |
| **Charts / Viz** | Chart.js |
| **Icons** | Lucide Icons |
| **Fonts** | Google Fonts (Inter) |
| **Hosting** | GitHub Pages |

---

*Submitted as part of the Rakamin AI-Native PM hiring process. Built with Claude Sonnet 4.6 (Anthropic) + Antigravity model Claude Sonnet 4.6.*