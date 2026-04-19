### 

### **CASE STUDY**

### **Product Manager**

## **Rakamin — Workforce Intelligence Platform**

**Role:** Product Manager (AI-Native)

**Submission window:** 5–7 business days from receipt

**Format:** Your choice — but three deliverables are required (see below)

This case study is designed to be hard. It reflects actual problems we face.

Use AI tools freely. We expect it. What we’re evaluating is your thinking, not your typing speed.

---

## **Background: Who We Are**

Rakamin is building a **Workforce Intelligence Platform** for large Indonesian enterprises. We operate a hybrid consulting \+ product model: we go deep into a client’s HR data mess, standardize it, build AI on top, and surface decision intelligence that HR teams can actually act on.

Our 2026 strategy is centered on one core insight:

Enterprise companies have spent billions on HR technology — but HR decisions are still made on spreadsheets.

The biggest gap isn’t the tool. It’s the data layer underneath.

We are not replacing existing HR systems. We integrate with them, fix what’s broken at the data layer, and build intelligence above it. Our moat is the accumulated workforce datasets, AI models, and use-case library we build across every engagement.

---

## **The Scenario**

### **Client: Medika Nusantara**

A healthcare distribution company. **15,000 employees**, 90 branches nationwide.

Their HR tech stack:

| System | Vendor | Known Issue |
| :---- | :---- | :---- |
| HRIS | SAP SuccessFactors | Incomplete historical data, low adoption |
| ATS | Workable | Disconnected from HRIS — no shared IDs |
| LMS | Moodle | Poor skill taxonomy, inconsistent categories |
| Performance | Custom internal tool | Inconsistent rating scales across branches |
| Payroll | Oracle | Restricted access — HR cannot query directly |

Additional data reality:

* **40% of employee records have missing or blank skill fields**  
* Job titles are inconsistent — “Senior Sales” in Surabaya \= “Sales 2” in Makassar  
* Employee IDs differ across systems (HRIS: EMP-2938, ATS: candidate\_918, Payroll: MN-444)  
* Historical performance data before 2022 is largely unreliable

**The trigger:** The CEO announced a “Digital Transformation Initiative.” The CHRO has been given 6 months to deliver AI-driven workforce decision-making. She wants to know:

* Which employees should be reskilled?  
* Which teams are at productivity or attrition risk?  
* Which roles will become obsolete in the next 2 years?

She has refused to replace any of the existing systems.

**The engagement:** Rakamin has been contracted for **Rp 2.5B over 12 months**. You are the PM. The first C-suite milestone is in **90 days**.

---

## **The Complication (Read carefully — this matters)**

On Day 30 of your engagement, you discover something that changes your data plan:

The Oracle Payroll system cannot be accessed by the HR team. Legal has flagged it as a privacy risk under the company’s internal data governance policy. You will not get payroll data for this engagement.

You must adapt. Your solution and roadmap must reflect this constraint.

---

## **What You Must Deliver**

Three deliverables. All three are required.

---

### **Deliverable 1 — Document**

A structured written document or slide deck (your format preference) covering:

**Part A — Problem Discovery**

1. The CHRO asked for “AI workforce insights.” That is not a product problem. What is the actual problem you are solving — and why did you choose it over alternatives?  
2. You must evaluate at least three possible focus areas (e.g., attrition prediction, skill gap analysis, internal mobility, workforce planning) and justify which one you’re prioritizing based on data availability, business impact, feasibility, and speed of PoC.  
3. What are the 5–7 most critical things you must learn in your first two weeks? For each: what would you do to get the answer?  
4. What are you explicitly NOT solving in 90 days, and why?

**Part B — Data Strategy**

1. How do you get to usable data when 40% of records are incomplete, IDs are inconsistent across systems, and payroll is off-limits?  
2. Design your data architecture — from ingestion through to AI-ready output. You don’t need to be an engineer, but you need to demonstrate you understand the layers and their interdependencies.  
3. Employee identity resolution is your first hard problem. An employee exists as EMP-2938 in SuccessFactors, candidate\_918 in Workable, and MN-444 in Oracle. Oracle is now inaccessible. How do you approach matching across the remaining three systems?

**Part C — AI System Design**

1. What AI component are you building for the 90-day PoC? Be specific: what does the model do, what features does it use, what does it output?  
2. How do you handle missing data — especially the 40% with no skill records?  
3. Your model outputs something like: Employee A → 78% attrition risk. Design the confidence signaling. What does the user see when confidence is high? When it’s low? What triggers a human review flag?  
4. On Day 75, your attrition model shows **82% accuracy on test data**. But three HR managers tell you the results feel wrong — the people it flags are not who they’d expect. What do you do?

**Part D — Product Design**

1. What does the decision interface look like? Design for an HR manager, not a data analyst. They should be able to act on what they see without understanding the model.  
2. How do you communicate uncertainty in the UI without destroying user trust?

**Part E — 90-Day Roadmap**

Break the 90 days into milestones. Each milestone must be a demo-able output — not a phase like “data collection.” What does the C-suite see at Day 30, Day 60, Day 90?

**Part F — Platform Strategy**

The killer question:

If this PoC works, how do you turn it into a reusable Rakamin platform — not just a custom build for Medika Nusantara?

Think about: reusable data models, modular AI services, configurable skill taxonomy, what gets reused across the next 5 clients. This is the difference between a consulting project and a product company.

---

### **Deliverable 2 — Working Prototype**

Build a working UI prototype that demonstrates your core product concept. It must:

* **Run in a browser** — single HTML file, multi-page HTML, or a deployed app. Your choice.  
* **Load and display your synthetic data** (Deliverable 3 — see below)  
* **Show a meaningful difference** between the messy dataset and the clean dataset — not just different numbers, but different quality of insight and confidence  
* **Demonstrate at least one “decision surface”** — something an HR manager would actually act on

You are expected to use AI coding tools (Claude, Cursor, GitHub Copilot, etc.) to build this. This is not a test of coding ability. It is a test of whether you can use AI tools to make your ideas concrete.

The prototype does not need to be production-ready. It needs to be real enough that an engineer looking at it would understand exactly what you’re building and why.

**Design taste is assessed here.** We evaluate your prototype not just for functional correctness, but for the quality of your design judgment. A PM at Rakamin works closely with UI/UX designers — you don’t need to be a designer, but you need strong enough taste to recognize good design, give meaningful direction, and push back when something is off. Your prototype should reflect that standard:

* Layout and information hierarchy feel intentional, not accidental  
* Data density is calibrated — nothing is shown that doesn’t need to be there  
* Confidence levels, risk flags, and uncertainty signals are communicated clearly without overwhelming the user  
* The visual language is consistent — spacing, color, and typography follow a system, even a simple one  
* It feels like something a real HR manager would open without confusion

A prototype that works but looks like it was thrown together tells us you’ll struggle to collaborate with designers productively. We’re not expecting pixel-perfect — we’re expecting taste.

**Minimum viable prototype:**

* Loads two datasets (messy vs. clean — from Deliverable 3\)  
* Shows the decision output for each  
* Highlights where confidence drops, where data is missing, and where human review is flagged

---

### **Deliverable 3 — Synthetic Data**

Create two CSV or JSON datasets representing Medika Nusantara employee data.

Dataset A — Messy (Enterprise Reality)

This should reflect what you’d actually find when you connect to their systems:

* \~200 employee records  
* 40%+ have missing skill fields  
* Inconsistent job titles across locations (same role, different names)  
* Incomplete performance history (some employees have 3 years of data, others have none)  
* Duplicate-ish records from different systems (slightly different names, different IDs)  
* Some records with conflicting data (e.g., different start dates in HRIS vs. ATS)

Dataset B — Ideal (Post-Contextualization)

The same 200 employees after your data processing layer has run:

* Normalized job titles against a standard taxonomy  
* Skills inferred or populated where possible (explain your inference logic)  
* Identities resolved across systems  
* Confidence scores attached to records where data was incomplete or inferred  
* Records flagged for human review where confidence is below your threshold

The Comparison

In your document (Deliverable 1\) or prototype (Deliverable 2), show what happens when each dataset is fed into your AI model concept:

* What changes in prediction quality?  
* Where does accuracy or confidence drop on Dataset A?  
* Which employees would be wrongly flagged or missed entirely?  
* What does this tell us about the value of the data layer (not just the AI layer)?

This is the core argument Rakamin makes to every enterprise client. We need PMs who can demonstrate it, not just explain it.

---

## **Evaluation Rubric**

We’ll share our scoring notes with you during the User Interview.

| Dimension | Weight | What We’re Looking For |
| :---- | :---- | :---- |
| **Problem Framing** | 20% | Did you reframe the CHRO’s request into an actual product problem? Did you draw principled scope boundaries? Did you justify your problem selection over alternatives? |
| **Data Architecture & Literacy** | 20% | Do you understand the data layers and their interdependencies? Is your identity resolution approach realistic? Does your synthetic data reflect genuine enterprise messiness? |
| **AI System Design** | 20% | Do you design for uncertainty — missing data, low confidence, model disagreement? Did you handle the 82% accuracy / “feels wrong” scenario correctly? |
| **Product & UX Thinking** | 15% | Did you design decision products, not dashboards? Can a non-technical HR manager act on what you built? |
| **Prototype Quality & Design Taste** | 15% | Does the prototype make your idea concrete? Does it demonstrate the data quality gap? Would an engineer understand what to build from this? Does the design reflect intentional judgment — hierarchy, clarity, consistency? Would a designer trust this PM to give meaningful direction? |
| **Strategic Scalability** | 10% | Did you think beyond one client? Is there a platform angle? Does your roadmap sequence for learning and reuse, not just delivery? |

---

## **Ground Rules**

**Use AI tools for everything.** Document which tools you used and how. We’re not looking for AI-free thinking — we’re looking for someone who’s developed strong judgment about when and how to use AI.

**Cite your assumptions.** When you don’t have data, say what you assumed and why. Uncited assumptions are the thing that kills projects.

**Be direct and opinionated.** A clear position we can challenge is more valuable than a balanced view that hedges every bet. We’ll push back in the interview — that’s the point.

**Show your reasoning, not just your conclusions.** We care as much about how you got there as where you landed.

---

## 

## **Submission**

Submit a **single PDF** via the hiring portal. Compile all three deliverables into this one document:

1. **Document** — your written analysis and strategy (inline)  
2. **Prototype** — include a working link (GitHub Pages, deployed URL, or any public URL). The prototype must be accessible without login.  
3. **Synthetic data** — include a link to your dataset files (Google Drive, GitHub, or equivalent). Ensure the link is publicly accessible.

Include a short note (3–5 sentences) at the end of the PDF: **What’s the one decision in your submission you’re least confident about, and what would you need to validate it?**

---

