# 🌾 AgriPrompt: Smart Farm Management Using Prompt-Engineered LLMs and IoT Data Streams

**AgriPrompt** is an intelligent backend system designed to assist farmers with smart farm management by integrating **IoT data streams** and **Large Language Models (LLMs)**.
It leverages **prompt-engineered LLMs**, **simulated IoT data**, and a **knowledge-augmented retrieval system (RAG)** to generate actionable insights — such as irrigation scheduling, fertilizer suggestions, and pest control alerts.

---

## 🚀 Features

* 🌱 **IoT Data Simulation** – Generate real-time farm sensor data (soil moisture, temperature, humidity, pest detection).
* 🤖 **Prompt-Engineered LLM Advisory** – Context-aware suggestions for farm management.
* 📚 **Knowledge Base (RAG)** – Retrieve crop-specific agricultural insights from curated datasets.
* 🔔 **Real-Time Alerts** – Automatic irrigation or pest warnings via SMS/WhatsApp/Email.
* 🧑‍🤖 **LLM Integration** – OpenAI API or open-source LLMs (e.g., Mistral, LLaMA).
* ⚡ **REST API** – FastAPI-based backend serving farm insights to dashboards or apps.

---

## 🏧 System Architecture

```
IoT Data Simulation → Data Preprocessing → Vector Knowledge Base → LLM Engine → Alerts/API
```

### Architecture Overview

1. **IoT Data Simulation** – Python scripts emulate soil & weather sensors.
2. **Preprocessing Pipeline** – Cleans and structures incoming data for analysis.
3. **Vector Knowledge Base** – Uses FAISS/Chroma to store agricultural embeddings.
4. **Prompt Engine** – Combines IoT readings with knowledge base context.
5. **LLM Advisory System** – Generates natural language recommendations.
6. **Alert Module** – Sends SMS/WhatsApp/email notifications on threshold triggers.
7. **REST API** – Exposes data endpoints and insights for external integration.

---

## 🧬 Tech Stack

| Component            | Technology Used                       |
| -------------------- | ------------------------------------- |
| Programming Language | Python 3.10+                          |
| Framework            | FastAPI / Flask                       |
| Database             | SQLite / PostgreSQL                   |
| Vector Store         | FAISS / Chroma / Pinecone             |
| LLM                  | OpenAI GPT / HuggingFace Transformers |
| Alerts               | Twilio / SMTP                         |
| Data Simulation      | MQTT / Faker                          |
| Scheduler            | APScheduler / Schedule                |
| Containerization     | Docker                                |

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/Sasmithere/AgriPrompt.git
cd AgriPrompt
```

### 2️⃣ Create Virtual Environment

```bash
python -m venv venv
source venv/bin/activate   # For Mac/Linux
venv\Scripts\activate      # For Windows
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Configure Environment Variables

Create a `.env` file:

```bash
OPENAI_API_KEY=your_openai_api_key
TWILIO_SID=your_twilio_sid
TWILIO_AUTH_TOKEN=your_auth_token
```

### 5️⃣ Run the Server

```bash
uvicorn app.main:app --reload
```

---

## 🧠 Example Workflow

1. Simulate IoT sensor data (soil moisture, temperature).
2. Preprocess and store readings in the database.
3. Query LLM with structured prompts:

   ```
   "Crop: Tomato, Soil Moisture: 18%, Weather: Dry — What irrigation advice should I follow?"
   ```
4. Retrieve context from knowledge base.
5. Generate natural language recommendation.
6. Send alert or expose result via API endpoint.

---

## 🧪 Example API Endpoints

| Endpoint          | Method | Description                    |
| ----------------- | ------ | ------------------------------ |
| `/data/simulate`  | GET    | Generate simulated IoT data    |
| `/recommendation` | POST   | Get crop advisory from LLM     |
| `/alerts`         | GET    | Trigger and check alert system |

---

## 🧰 Requirements

* Python 3.10+
* OpenAI API key (or local HuggingFace model)
* (Optional) Twilio account for alerts
* Basic command-line and Git knowledge

---

## 🤩 Folder Structure

```
AgriPrompt/
│
├── app/
│   ├── main.py               # FastAPI app entry point
│   ├── data_pipeline.py      # Data preprocessing & simulation
│   ├── llm_engine.py         # LLM + RAG integration
│   ├── knowledge_base.py     # Vector DB setup
│   ├── alerts.py             # Notification system
│   └── config.py             # Environment variables & settings
│
├── data/
│   ├── sensors.csv
│   ├── knowledge_base/
│
├── requirements.txt
├── .env.example
├── README.md
└── LICENSE
```

---

## 🌍 Future Enhancements

* ✅ Add multimodal input (text + images for crop disease detection).
* ✅ Integrate weather APIs (OpenWeather, NASA POWER).
* ✅ Build lightweight web dashboard.
* ✅ Support multilingual prompts for local farmers.
* ✅ Fine-tune small open-source LLMs for domain adaptation.

---

<!-- This is a single-line comment.## 🧑‍🤝 Contributors

| Name                | Role                             |
| ------------------- | -------------------------------- |
| [Your Name]         | Project Lead / Backend Developer |
| [Collaborator Name] | LLM & Prompt Engineer            |
| [Collaborator Name] | IoT Simulation / Data Engineer   |

---
-->
## 📜 License

This project is licensed under the **MIT License** — free to use and modify.

---

## ⭐ Acknowledgements

This project draws insights from:

* *AgroLLM: Connecting Farmers and Agricultural Practices through LLMs (2025)*
* *Foundation Models in Smart Agriculture (2024)*
* *Enhancing Agricultural Intelligence with LLMs (2025)*

---

🌾 *AgriPrompt — Harnessing AI to make farming smarter, sustainable, and more accessible for everyone.*
