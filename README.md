# Finance Assistant Chatbot (FIN_BOT)

An AI-powered Finance Assistant Chatbot built using **Dialogflow Essentials (ES)** and integrated into a web interface via **Kommunicate**. The bot is designed to assist users with core financial concepts, including calculations and definitions for EMI, Net Present Value (NPV), Break-Even analysis, and tax-saving advice.

---

## 🚀 Features & Capabilities

The chatbot is pre-trained to handle a variety of financial intents:
* **Loan & EMI Guidance:** Explains Equated Monthly Installments, what parameters alter EMI values, and provides contextual loan calculations.
* **Capital Budgeting & Evaluation:** Defines and interprets **Net Present Value (NPV)**, Internal Rate of Return (IRR), and Return on Investment (ROI) to help users understand project viability.
* **Financial Health & Ratios:** Provides advice on budgeting, credit scores, debt-to-equity metrics, and liquidity ratios (Current Ratio).
* **Tax & Insurance Advisory:** Guides users on tax-saving instruments and optimal insurance policies.

---

## 🛠️ System Architecture & Workflow

The integration flow operates seamlessly from user input to natural language processing response:

1. **User Interaction:** The end-user sends a message via the **Kommunicate Web Chat Widget**.
2. **Platform Routing:** Kommunicate acts as the middleware channel and securely forwards the text payload to Google Dialogflow via the authenticated **GCP Service Account**.
3. **Intent Matching:** Dialogflow's Natural Language Understanding (NLU) engine parses the user's expression, matches it against predefined training phrases, and extracts the corresponding intent.
4. **Response Delivery:** The structured static text response or fulfillment data maps back through Kommunicate and renders instantly on the user's UI.

---

## 📋 Configuration & Setup Guide

### 1. Dialogflow ES Agent Configuration
* Create a Dialogflow ES Agent named `mbafinanceassistance-rjdd`.
* Create the custom intents listed under the workspace (e.g., `NPV_Intent`, `EMI_Calculator`, `Break_Even_Intent`, `Budgeting advice`).
* **Example - NPV Intent:**
  * **Training Phrases:** Add variations such as *"What is NPV"*, *"Explain NPV"*, *"Net present value"*, and *"How to calculate NPV"*.
  * **Responses:** Define static text explaining the decision criteria (e.g., *If NPV is positive $\rightarrow$ Project may be accepted*).

### 2. Google Cloud Platform (GCP) Authentication
To allow Kommunicate or a custom backend to communicate securely with your Dialogflow agent, you must provision access:
1. Navigate to the **GCP Console $\rightarrow$ IAM & Admin $\rightarrow$ Service Accounts**.
2. Select your specific Dialogflow service account (`dialogflow@mbafinanceassistance-rjdd.iam.gserviceaccount.com`).
3. Click on the **Keys** tab $\rightarrow$ **Add Key** $\rightarrow$ **Create new key**.
4. Select **JSON** format and click **Create**. A private key file will download automatically to your system. Keep this file secure as it gives full conversational access to your agent.

### 3. Kommunicate Integration
1. Log in to the **Kommunicate Dashboard**.
2. Navigate to **Bot Integrations** and select **Dialogflow**.
3. Upload the downloaded **GCP Service Account JSON key** to establish a handshake connection.
4. Name your bot (`FIN_BOT`), customize its avatar, and copy the provided demo script code snippet to embed into any web application HTML file.

---

## 📸 Deployment Results & Screenshots

The following sequence showcases the configuration backend running live into production:

### Dialogflow Console & Intent mapping
* **Intent List Workspace:** A complete overview of the custom financial intents built into the agent.
* **Intent Deep-Dive:** Inside the `NPV_Intent` panel depicting the operational training phrases alongside the structured diagnostic response testing terminal window.

### GCP IAM Credential Handshake
* **Service Account Key Generation:** Generation window displaying the final selection steps of downloading the private `JSON` configuration key token required for backend authentication.

### Live Chat Integration (End-User View)
* **Kommunicate Live Preview Interface:** Demonstrates the responsive, front-facing `FIN_BOT` chat widget successfully mapping and answering queries regarding **EMI parameters** flawlessly.
* **Agent Dashboard Live Chat Monitoring:** Shows the actual conversations flowing into the support agent interface for real-time human-handoff capabilities.
