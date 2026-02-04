
---

# 🚀 AutoTag-AI: Intelligent Support Ticket Classifier

**AutoTag-AI** is a high-performance automated classification system designed to streamline customer support workflows. By utilizing **Llama 3.3** via the **Groq LPU Engine**, it transforms messy, unstructured support tickets into actionable, categorized data in milliseconds.

---

## 💡 The Problem

In modern support systems, manual tagging is slow, prone to human error, and creates bottlenecks. **AutoTag-AI** solves this by providing:

* **Contextual Understanding:** Goes beyond keyword matching to understand the *intent* (e.g., recognizing "motherboard" as *Hardware*).
* **Ranked Accuracy:** Instead of a single guess, it provides a **Top-3 ranking**, ensuring high reliability for complex queries.
* **Hybrid Learning:** Supports both **Zero-Shot** (general knowledge) and **Few-Shot** (example-based) classification modes.

---

## 🛠️ Key Features

### 1. Zero-Shot vs. Few-Shot Engine

Toggle between standard AI logic and specialized "Few-Shot" learning where the model is provided with "Gold Standard" examples to align with your specific domain vocabulary.

### 2. Dual-Mode Interface (Gradio)

* **Single Ticket Labeller:** A "sandbox" for support agents to verify individual queries manually.
* **Bulk Batch Processor:** Upload a CSV of 1,000+ tickets and receive a fully tagged dataset in one click.

### 3. High-Speed Inference

Powered by Groq's LPU architecture, achieving near-instantaneous processing compared to traditional cloud-hosted models.

---

## 📂 Project Architecture

```text
AutoTag-AI/
├── AutoTag_AI.ipynb   # Full development & deployment notebook
├── env.example        # Configuration template (Never push real keys!)
├── .gitignore         # Critical security file for env.txt
└── README.md          # Project documentation

```

---

## 🚀 Getting Started

### 1. Prerequisites

* Python 3.10+
* A Groq API Key (Get it at [console.groq.com](https://console.groq.com))

### 2. Installation & Setup

```bash
# Clone the repo
git clone https://github.com/youmna-saifullah/AutoTag-AI.git
cd AutoTag-AI

# Install dependencies
pip install groq python-dotenv gradio pandas

```

### 3. API Configuration

Create a file named `env.txt` in the root directory:

```text
GROQ_API_KEY=gsk_your_actual_key_here

```

### 4. Running the App

Open `AutoTag_AI.ipynb` in VS Code or Jupyter and run the Gradio cell. A local URL (and a public shareable link) will be generated.

---

## 📊 Sample Test Sentences

Try these in the UI:

* **Ticket:** "The RSA key generation is failing with a timeout." → **Pred:** `['Cryptography', 'Other', 'Other']`
* **Ticket:** "My Mac won't chime at startup." → **Pred:** `['Mac Hardware', 'Other', 'Other']`

---

## 🤝 Contributing

Contributions are welcome! If you'd like to improve the prompt engineering or add new UI features, feel free to fork the repo and open a Pull Request.

---

*Created as part of the DeveloperHub AI Internship Phase 2.*

---


```
