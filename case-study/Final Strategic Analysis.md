# **Rakamin Case Study: Workforce Intelligence Platform**

**Role:** Product Manager (AI-Native)

**Client:** Medika Nusantara

## **Deliverable Links**

* **Working Prototype:** \[PASTE YOUR HOSTING LINK HERE\]  
* **Synthetic Datasets (A & B):** \[PASTE YOUR GOOGLE DRIVE LINK HERE\]

## **Part A \- Problem Discovery**

### **1\. The Real Problem Statement**

The CHRO’s request for "AI workforce insights" is a symptom, not the problem. The core problem is **"Institutional Decision Blindness"** caused by a fragmented and semantic-poor data layer. Medika Nusantara cannot execute its digital transformation because its "Workforce Identity" is fractured across three systems. With **40% of skill data missing** and inconsistent job titles, the organization is making high-stakes human capital decisions on "gut feeling" rather than data-driven intelligence.

### **2\. Focus Area Prioritization**

We evaluated three potential PoC areas for the 90-day milestone:

| Focus Area | Feasibility | Business Impact | PoC Speed | Decision |
| :---- | :---- | :---- | :---- | :---- |
| **Attrition Prediction** | Low | High | Slow | **Discarded:** Requires Oracle Payroll data (restricted) for accurate ROI and compensation-linked triggers. |
| **Internal Mobility** | Medium | Medium | Medium | **Secondary:** Difficult to execute without a pre-existing unified skill taxonomy. |
| **Skill Gap Analysis** | **High** | **Very High** | **Fast** | **Prioritized:** AI can fill the 40% data gap via inference. Directly supports the CEO’s 2-year transformation mandate. |

### **3\. Critical Discovery (First 2 Weeks)**

1. **LMS Semantic Audit:** Do Moodle logs track "Time Spent" or just "Status"? (Action: Audit Moodle API for engagement signals).  
2. **Job Title Normalization:** Interview 5 Regional HR Managers to map the responsibilities of "Senior Sales" vs "Sales 2". (Action: Qualitative mapping).  
3. **Identity Key Profiling:** Identify non-sensitive common keys like Personal Email or Phone Number across SAP and Workable. (Action: Data profiling dump).  
4. **Performance Consistency:** Validate if "Custom Tool" ratings are comparable across branches. (Action: Statistical variance analysis).  
5. **Obsolescence Criteria:** Confirm with the CEO's office which roles are considered "at-risk" by digital automation. (Action: Stakeholder interview).

### **4\. Explicit Non-Goals (Out of Scope for 90 Days)**

* **Payroll Integration:** Strictly excluded due to Legal/Privacy governance constraints discovered on Day 30\.  
* **Real-time Prediction:** We will focus on "Point-in-Time" batch analysis for the PoC to ensure data quality before moving to streaming updates.

## **Part B \- Data Strategy**

### **1\. Data Architecture Design (The "Intelligence Layer" Approach)**

We implement a four-layer architecture to bridge the data gap:

* **Ingestion Layer:** Custom connectors for SAP (HRIS), Workable (ATS), and Moodle (LMS).  
* **Harmonization Layer:**  
  * **Semantic Normalizer:** Uses LLMs to map inconsistent branch titles to a Standardized Workforce Ontology.  
  * **Identity Resolver:** Multi-key heuristic matching to merge records into a Unified Employee ID.  
* **Intelligence Layer:** Gradient Boosted models for Skill Inference.  
* **Serving Layer:** Decision Interface (Talent Command Center) for actionable HR insights.

### **2\. Identity Resolution: Geo-fencing & Multi-Key Matching**

Without Oracle IDs, we use **Multi-Key Heuristic Matching**:

* **Primary Key:** Fuzzy Match (Name) + Join Date Range + Current Branch.  
* **Geo-fencing Logic:** We use branch data as a search boundary to resolve common names (e.g., "Budi Santoso").  
* **Risk Mitigation:** Records with conflicting join dates (e.g., HRIS vs ATS discrepancy) or confidence <75% are flagged for Human Verification.

## **Part C \- AI System Design**

### **1\. 90-Day PoC AI Component: The "Skill Inference Engine"**

* **Task:** Predict missing skills for the 40% incomplete records.  
* **Features (Input):** Standardized Job Title, Branch Location, Performance Score, Moodle Course Completion History, and Years of Service.  
* **Output:** A Skill Profile categorizing Verified Skills vs Inferred Skills, with an associated Record-Level Confidence Score.

### **2\. Handling the 40% Missing Data Gap**

We employ **Collaborative Peer-Group Inference**:

* **Mechanism:** If 90% of "Senior Sales" in the Surabaya branch with \>3 years tenure possess "CRM Mastery" and "Negotiation," the model infers these skills for the 10% with blank records.  
* **Guardrail:** All inferred skills are visually labeled as *"Inferred"* in the UI to maintain transparency.

### **3\. Confidence Signaling & Human-in-the-Loop**

* **High Confidence (≥75%):** Automatically designated as "Ready for Reskilling" and unlocks immediate action assignments.  
* **Low Confidence (<75%):** Triggers a **"Human Review Flag" (Verify Button).**  
* **Interaction:** HR Managers can hover over inferred skills to see the exact AI logic, and click a "Verify" button which instantly upgrades the record and provides feedback to the model.

### **4\. Dealing with Model Disagreement (The 82% Accuracy Case)**

If HR managers claim the results "feel wrong":

1. **Explainability Audit:** Use SHAP values to show *why* the AI flagged a person (e.g., "High potential due to advanced Excel completion in Moodle").  
2. **Reinforcement Learning:** Treat HR disagreement as "Ground Truth" labels. If a manager rejects a prediction, the model is retrained to weight that specific feature (e.g., LMS completion) lower.  
3. **Feature Gap Acknowledgment:** Investigate if the lack of Payroll data (compensation) is creating a blind spot in identifying "unhappy" high-performers.

## **Part D \- Product & UX Thinking**

### **1\. Decision Interface: Talent Command Center**

We avoid "Data Dumps." The UI is designed for **Action**:

* **Priority Lists:** Instead of a full directory, we surface "Top 100 Candidates for Reskilling."  
* **Decision Surfaces:** Integrated "Verify" and "Assign to Program" buttons.  
* **Uncertainty Signaling:** We use a "Confidence Meter" (0-100%) next to names to communicate AI certainty without overwhelming the user.

## **Part E \- 90-Day Roadmap**

| Milestone | Timing | Demo-able Output | Business Value |
| :---- | :---- | :---- | :---- |
| **Unified Identity** | Day 30 | **"The Unified Profile"** tool showing resolved data from 3 systems. | Proves data can be merged without Payroll. |
| **Inference Engine Alpha** | Day 60 | **"The Skill Gap Heatmap"** showing 40% filled gaps for the first time. | Visualizes "Hidden Talent" across branches. |
| **Decision Surface PoC** | Day 90 | **"The Reskilling Priority List"** live with HR verification loops. | Direct answer to the CHRO's "Who to reskill?" |

## **Part F \- Platform Strategy (The Moat)**

To transform this from a custom build to a Rakamin Platform:

1. **Configurable Workforce Ontology:** A plug-and-play skill library that can be swapped for other industries (Retail, Banking).  
2. **Modular AI Service (Skill-as-a-Service):** The Inference engine is built as an API, allowing future clients to upload raw titles and get predicted skills instantly.  
3. **Federated Learning (Long-term):** Anonymized skill trends from Medika help improve the base model for the *next* healthcare client, creating a data network effect.

## **Final Note: The "One Decision" Reflection**

The decision I am least confident about is **relying on Moodle (LMS) completion data as a proxy for skill competence.** While it shows intent and learning agility, "completion" does not guarantee "mastery." To validate this, I would need a "Skill Calibration" phase during the first 30 days, taking a sample of 100 employees and comparing the AI's inferred scores with actual qualitative assessments from their direct supervisors to adjust the model's weighting.

**Tools Used:** Claude 3.5 Sonnet (Data Synthesis & Prompt Logic), Antigravity (UI Prototype), Markdown (Document Strategy).