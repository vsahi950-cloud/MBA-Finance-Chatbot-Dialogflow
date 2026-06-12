# MBA Finance Assistance Bot (FIN_BOT)

An AI-powered conversational agent designed to provide instant explanations, calculations, and advisory responses for core financial concepts like EMI, NPV, IRR, and Credit Scores. Built using **Dialogflow Essentials (ES)** and integrated with **Kommunicate** for a seamless, interactive user interface.

---

## 🚀 Features
* **Core Finance Explanations:** Instant breakdown of complex concepts (NPV, IRR, Break-Even Point).
* **Interactive Advisory:** Dedicated intents for budgeting, loan advice, and investment strategies.
* **Kommunicate Integration:** Clean, web-ready chat widget for real-time user engagement.

---

## 🛠️ Step-by-Step Implementation & Screenshots

### 1. Dialogflow Agent & Intent Architecture
The bot's intelligence is built on modular intents mapping to specific financial queries. Training phrases ensure high intent-matching accuracy.

<p align="center">
  <img src="./screenshots/Agent_Creation.png" alt="Agent Creation" width="800"/>
  <br><i>Figure 1: Initializing the Dialogflow Finance Assistance Agent</i>
</p>

<p align="center">
  <img src="./screenshots/Intent_List.png" alt="Intent List" width="800"/>
  <br><i>Figure 2: Complete List of Configured Financial Intents</i>
</p>

---

### 2. Deep Dive: Intent Configurations & Responses
Each intent (e.g., `NPV_Intent`) contains specialized user expressions and structured text responses explaining financial dynamics clearly to the end user.

<p align="center">
  <img src="./screenshots/NPV_Intent.png" alt="NPV Intent Configuration" width="800"/>
  <br><i>Figure 3: Training Phrases mapped for Net Present Value (NPV) Queries</i>
</p>

<p align="center">
  <img src="./screenshots/Response.png" alt="Text Responses" width="800"/>
  <br><i>Figure 4: Defining Clear, Structured Text Outputs for the Agent</i>
</p>

---

### 3. Google Cloud IAM & Service Account Authentication
To securely connect Dialogflow with external platforms like Kommunicate, a Google Cloud Service Account key is generated.

<p align="center">
  <img src="./screenshots/Service_Account.png" alt="Service Account Panel" width="800"/>
  <br><i>Figure 5: Navigating to Service Account Keys within Google Cloud Console</i>
</p>

<p align="center">
  <img src="./screenshots/JSON_Key.png" alt="Generating JSON Key" width="800"/>
  <br><i>Figure 6: Generating and Downloading the Private JSON Key for Authentication</i>
</p>

---

### 4. Kommunicate Integration & Live Demo
The downloaded JSON key is uploaded to the Kommunicate dashboard to sync the Dialogflow fulfillment engine with the frontend chat widget interface.

<p align="center">
  <img src="./screenshots/Kommunicate_Setup.png" alt="Kommunicate Chat Widget Live" width="800"/>
  <br><i>Figure 7: Live Interaction with FIN_BOT rendering structured EMI details in Kommunicate</i>
</p>

---

## 📦 How to Run Locally
1. Clone this repository.
2. Export your Dialogflow Agent zip bundle and import it into your own Dialogflow Console.
3. Setup a Google Cloud Service account and download your credentials key.
4. Integrate with Kommunicate via their **Bot Integrations** dashboard using the JSON key.
