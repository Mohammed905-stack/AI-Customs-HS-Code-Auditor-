# # AI-Powered Customs & HS Code Classification Auditor

An automated workflow built in **n8n** utilizing the **Google Gemini AI Agent** to streamline international trade compliance, classify products into Harmonized System (HS) chapters, and flag regulatory watch-outs.

---

## 🚀 Project Overview
Navigating international customs regulations and identifying accurate Harmonized System (HS) codes is a manual, time-consuming bottleneck in logistics and supply chain management. This project automates the initial classification audit by feeding product descriptions through a specialized LLM agent trained in global trade compliance.

---

## 🛠️ Tech Stack & Architecture
* **Automation Platform:** n8n (Local Instance)
* **Core Engine:** n8n AI Agent Node
* **LLM Provider:** Google Gemini API (`gemini-3.6-flash` / Gemini Chat Model)
* **Design Pattern:** Prompt-engineered persona with modular parameters.

### Workflow Pipeline:
1. **Trigger Interface:** Accepts raw, unstructured product descriptions.
2. **AI Agent Processing:** Evaluates the item using custom system instructions focused on international trade laws.
3. **Structured Output Generation:** Returns a comprehensive multi-tier compliance report covering HS chapters, regulatory flags, and required documentation.

---

## 🔒 Security & Credential Management (For Evaluators)
This repository contains the workflow structure without hardcoded keys. To run or test this automation locally:
1. Import the `workflow.json` file into your local n8n instance.
2. Create your own **Google Gemini API Credential** within n8n using your personal Google AI Studio key.
3. Link your credential to the **Google Gemini Chat Model** node to ensure your private keys remain secure and isolated.

---

## 📂 Repository Structure
* `workflow.json`: The raw n8n automation blueprint.
* `hs_code_compliance_project_documentation.pdf`: Complete step-by-step project report, architecture breakdown, and execution logs.

---

## 📊 Sample Execution Output
> **Input:** *"Cotton knitted men's shirts"*  
> **Output Summary:**  
> * **Primary HS Code:** `6105.10` (Of cotton, knitted or crocheted)  
> * **Chapter Breakdown:** Chapter 61 (Articles of apparel and clothing accessories, knitted or crocheted)  
> * **Regulatory Watch-Outs:** UFLPA compliance, textile import quotas, and country-specific labeling rules.  
> * **Required Documentation:** Commercial Invoice, Packing List, Certificate of Origin, Bill of Lading.AI-Customs-HS-Code-Auditor-
