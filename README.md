# 🚀 AI-Driven Intelligent Churn Prediction & Retention System

An end-to-end automated customer retention workflow that leverages RFM analysis on SQL Server and orchestrates AI-driven personalized engagement using n8n and Google Gemini API.

## 📌 Project Overview
Customer churn is a critical challenge in FMCG and e-commerce retail. This system automatically identifies "At Risk" customers based on RFM segmentation, evaluates their customer lifetime value, generates tailored re-engagement offers using Generative AI, and logs operations into Google Sheets with strict rate-limit handling.

## 🛠️ Tech Stack & Architecture
- **Database:** Microsoft SQL Server (RFM Calculation & `vw_AtRiskCustomers` View)
- **Orchestration:** n8n Workflow Automation
- **AI Model:** Google Gemini API (`gemini-1.5-flash`)
- **Data Destination:** Google Sheets (Campaign Logging & Audit Trail)

## ⚡ Key Technical Features & Challenges Solved
1. **RFM Customer Segmentation:** SQL-driven logic segmenting high-value vs. standard at-risk customers.
2. **Dynamic AI Prompting:** Tailored discounts and tone generation based on total customer spend ($Total\_Spent$).
3. **Rate-Limit Management (15 RPM):** Implemented a robust `Loop Over Items` + `Wait Node` architecture in n8n to ensure seamless sequential execution without API quota errors.
4. **Automated Audit Logging:** Appending customer data, AI text, and execution timestamps into Google Sheets.

## 📂 Repository Contents
- `n8n-retention-workflow.json`: The complete exportable n8n workflow pipeline.
- `vw_AtRiskCustomers.sql`: SQL scripts for RFM views and data extraction.
- ## 🎥 Demo & Execution
Here is a quick walkthrough of the automated workflow running in n8n and logging data into Google Sheets:

![Workflow Demo](https://github.com/user-attachments/assets/cd786599-93e4-4b91-b2b9-0fe17e719f81)

## 📷 Workflow Architecture
*(Insert your n8n workflow screenshot here)*
