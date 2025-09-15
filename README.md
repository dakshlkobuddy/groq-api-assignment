# Groq API Assignment: Conversation Management & Information Extraction

**Author:** Daksh Agarwal
***

## 🚀 Project Overview

This project demonstrates the implementation of two core functionalities using the Groq API and its OpenAI-compatible Python SDK. The primary constraint was to use standard Python libraries without relying on high-level frameworks like LangChain.

The two main tasks are:
1.  **Conversation History Management:** A system to maintain and periodically summarize conversation history to manage context in long-running chats.
2.  **Structured Information Extraction:** A system to parse unstructured chat messages and extract specific user details into a structured JSON format using tool calling.

---

## ✨ Key Features

### Task 1: Conversation History with Summarization
- **Maintain Running History:** Keeps a chronological log of user and assistant messages.
- **Periodic Summarization:** Automatically summarizes the conversation after every `k` turns to keep the context concise.
- **History Replacement:** The detailed history is replaced by a single system message containing the summary, ensuring efficient context management for future turns.

### Task 2: JSON Schema & Information Extraction
- **Structured Output:** Uses a predefined JSON schema to extract five key user details: `name`, `email`, `phone`, `location`, and `age`.
- **Tool Calling:** Leverages the Groq API's tool-calling (function-calling) feature to ensure the model's output conforms to the required schema.
- **Schema Validation:** Includes a function to validate the extracted data against the defined schema, ensuring correctness and handling cases where information is partially available or absent.

---

## 🛠️ Technologies Used

- **Language:** Python
- **Primary API:** Groq
- **SDK:** `groq` (OpenAI-compatible Python client)
- **Environment:** Google Colab
- **Standard Libraries:** `os`, `json`

---

## ⚙️ Setup and Installation

To run these notebooks, you will need a Groq API key.

#### **Prerequisites**
- A Groq account and a valid API key. You can get one from the [Groq Console](https://console.groq.com/keys).

#### **Instructions**

1.  **Clone the Repository (Optional):**
    ```bash
    git clone [https://github.com/dakshlkobuddy/groq-api-assignment.git](https://github.com/dakshlkobuddy/groq-api-assignment.git)
    ```

2.  **Open in Google Colab:**
    Open the `.ipynb` files in Google Colab.

3.  **API Key Configuration (Required):**
    This project uses Colab's Secrets Manager to handle the API key securely.

    > **Note:** To run the notebooks, you must configure your own Groq API key.

    - In the Colab interface, click the **key icon (🔑) on the left sidebar**.
    - Click **"Add a new secret"**.
    - For the **Name**, enter exactly `GROQ_API_KEY`.
    - For the **Value**, paste your personal Groq API key.
    - Ensure the **"Notebook access"** toggle is enabled.

---

## ▶️ How to Run

Once the API key is configured in the Secrets Manager, you can run the notebooks.

1.  Open either `Task_1_Conversation_Summarization.ipynb` or `Task_2_Information_Extraction.ipynb`.
2.  From the top menu, select **`Runtime > Run all`**.
3.  The notebooks will execute from top to bottom, and all outputs will be visible.

---

## 📂 Repository Contents
