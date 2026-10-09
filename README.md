# AI Text Classification Automation using n8n, Ollama, and Google Sheets

An AI-powered text classification automation built with **n8n, Ollama, and Google Sheets**. This workflow uses a locally running AI model to analyze text, assign a suitable category, and organize the classification results in Google Sheets.

The project demonstrates how AI and workflow automation can be combined to reduce manual text categorization.

## 🚀 Features

* Automatically analyzes text using an AI model.
* Classifies text into predefined categories.
* Uses Ollama to run a local language model.
* Automates the workflow with n8n.
* Stores classification results in Google Sheets.
* Reduces manual effort when organizing text data.
* Avoids paid AI API credits for local model inference.

## 🛠️ Technologies Used

* **n8n** — Workflow automation
* **Ollama** — Local AI model runtime
* **Gemma 3:4b** — AI model for text analysis (if this is the model used in your workflow)
* **Google Sheets** — Storing text and classification results
* **PowerShell** — Running and testing Ollama on Windows

## ⚙️ Workflow

The automation follows this general process:

`Input Text → n8n → Ollama AI Classification → Google Sheets`

The workflow receives text, sends it to the local AI model for classification, and stores the result in a spreadsheet.

## 🔄 How It Works

1. Text is provided to the n8n workflow.
2. n8n passes the text to Ollama.
3. The AI model analyzes the text and assigns a category.
4. n8n processes the classification result.
5. The input text and its category are saved to Google Sheets.

## 🏷️ Example Classification Categories

Depending on the prompt and configuration, categories could include:

* Positive
* Negative
* Neutral
* Feedback
* Complaint
* Question

The actual categories depend on the labels configured in the workflow.

## 📋 Example Output

| Input Text                      | Predicted Category |
| ------------------------------- | ------------------ |
| The service was excellent!      | Positive           |
| I am unhappy with the delivery. | Negative           |
| When will my order arrive?      | Question           |

*Example data for illustration; actual results depend on the model and workflow configuration.*

## 💻 Setup Requirements

* Windows computer
* n8n
* Ollama
* A downloaded Ollama model
* Google account and Google Sheets access

### 1. Install Ollama

Download Ollama from:

https://ollama.com/download/windows

### 2. Download the AI Model

If your workflow uses Gemma 3:4b, run:

```powershell
ollama pull gemma3:4b
```

### 3. Verify the Model

```powershell
ollama list
```

### 4. Configure n8n

* Open your n8n instance.
* Configure the input node used in your workflow.
* Add the AI classification prompt.
* Connect the Ollama Chat Model to the appropriate AI node.
* Configure Google Sheets to store the classification output.

For a locally running Ollama server, the usual API base URL is:

`http://localhost:11434`

If n8n runs in Docker or another container, the connection URL may differ.

### 5. Configure Google Sheets

Connect your Google account and map the workflow output to the appropriate spreadsheet columns, such as:

* Input Text
* Predicted Category
* Classification Result

Column names should match your actual spreadsheet setup.

## 📸 Screenshots

Add your screenshots to a folder named `screenshots`.

### n8n Workflow

![n8n Workflow](screenshots/n8n-workflow.png)

### Google Sheets Results

![Google Sheets Results](screenshots/google-sheets-output.png)

## 🎯 Learning Objectives

* Build AI-powered workflow automations.
* Integrate a local AI model with n8n.
* Practice prompt engineering.
* Understand automated text classification.
* Connect AI outputs to Google Sheets.
* Explore practical applications of NLP and AI automation.

## 🔮 Future Improvements

* Add more classification categories.
* Process multiple text entries automatically.
* Add confidence scores where supported.
* Connect additional data sources.
* Build a dashboard to analyze classification results.
* Improve error handling and output validation.

## 👩‍💻 Author

**Nagina Azhar**

Learning Python, AI, and workflow automation by building practical projects.

---

*This project is part of my journey toward building useful AI automation solutions.*

