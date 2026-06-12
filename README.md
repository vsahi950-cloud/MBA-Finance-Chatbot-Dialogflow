# FIN_BOT: AI-Powered MBA Finance Assistant

An intelligent, conversational AI agent built using **Dialogflow Essentials (ES)** and deployed seamlessly via **Kommunicate**. This bot functions as a virtual financial advisor capable of handling core corporate finance queries, loan breakdowns, and investment performance metrics.

---

## 🚀 Live Demo & Interface

The chatbot features an intuitive chat widget that handles complex finance terminology and breaks it down into easy-to-digest interactive lists and summaries.

### Active Bot Interaction
*Figure 1: FIN_BOT actively responding to an "EMI" query via the Kommunicate customer dashboard.*

---

## 🛠️ Core Capabilities & Intents

The agent is trained to identify financial terminology, process user intent, and provide structured default responses for:
* **Time Value of Money:** Net Present Value (NPV), Internal Rate of Return (IRR).
* **Corporate Financial Metrics:** Current Ratio, Debt-to-Equity, Break-Even Analysis, ROI.
* **Personal Finance:** EMI Calculators, Tax Saving Strategies, Insurance, and Investment Advisory.

---

## 🏗️ Architecture & Configuration Steps

### 1. Agent Creation & Intent Mapping
The bot's core logic is managed within Dialogflow Essentials, where custom intents are defined for various financial parameters.

*Figure 2: Creating and initializing the finance assistant agent.*

*Figure 3: Main dashboard displaying the comprehensive list of custom financial intents.*

---

### 2. Training Phrases & Natural Language Processing (NLP)
Each intent is mapped against realistic user expressions (e.g., "Explain NPV", "How to calculate NPV") to train the underlying machine learning model.

*Figure 4: Configuration of training phrases inside the `NPV_Intent` dashboard.*

---

### 3. Structured Text Responses
Responses are designed with clean formatting to ensure clear readability when rendered inside live chat windows.

*Figure 5: Setting up structured text response variants for user execution queries.*

---

### 4. Google Cloud IAM & Fulfillment Security
To bridge the agent securely with external platforms or fulfillment webhooks, a Google Cloud Service Account key is required.

*Figure 6: Navigating the Google Cloud Console IAM & Admin panel to generate a service account key.*

*Figure 7: Generating and downloading the secure private JSON credential key.*

---

## 💻 Tech Stack
* **Natural Language Processing:** Google Dialogflow (ES)
* **Deployment & UI Integration:** Kommunicate Hybrid Platform
* **Cloud Infrastructure:** Google Cloud Platform (GCP) IAM
