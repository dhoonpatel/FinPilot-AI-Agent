# FinPilot AI: Personal Finance Decision-Support Agent 🚀

FinPilot AI is an advanced, automated financial decision-support companion built using **n8n** and **Google Gemini (gemini-1.5-flash)**. It helps everyday users securely ingest scattered financial documents and receive data-driven, conversational insights without giving any regulatory-restricted investment advice.

## 🎯 Key Project Features
- **Data Ingestion & Parsing:** Automated processing of bank statements and bills (PDF/CSV).
- **Intelligent Categorization:** Contextually splits financial data into Fixed Obligations (Rent, EMI, Insurance) and Variable Expenses (Dining out, Shopping).
- **Financial Leak Detection:** Proactively scans and alerts users about recurring inactive subscriptions and sudden spending anomalies.
- **Conversational Decision Support:** Users can chat using natural language queries to evaluate financial trade-offs and review monthly summaries.

## 🛠️ Architecture Workflow
The system pipeline follows a strict modular visual layout built inside n8n:
1. **Trigger Module:** Chat Trigger interface for real-time user questions.
2. **AI Core:** LangChain-powered autonomous Agent Node acting as a financial co-pilot.
3. **Brain Component:** Google Gemini LLM utilizing custom-crafted system prompts constraint to strictly avoid stock/trading recommendations.
4. **Memory Layer:** Window Buffer Chat Memory tracking active financial session parameters.

## ⚙️ How to Deploy & Test Locally
To protect active usage, personal API keys have been scrubbed from this repository. To run this agent in your local workspace:
1. Download the `finpilot_agent.json` workflow file from this repository.
2. Open your [n8n Cloud canvas](https://n8n.io).
3. Import the file via the built-in option or use `Ctrl + V`.
4. Double-click the **Google Gemini Node**, create a new credential, and insert your individual `GEMINI_API_KEY`.
5. Tap **Open Chat** and start testing the agent!

---
*Developed for the Product Space 2-Day Generative AI Product Hackathon.*
