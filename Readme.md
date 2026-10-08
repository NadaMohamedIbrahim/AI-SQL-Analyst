# 🚀 [Tips Hindawi](https://www.tipshindawi.com/) Internship (August–October) 2026

> 🎓 This project was built during the [ **Tips Hindawi** ](https://www.tipshindawi.com/) **Internship (August–October) 2026**.

## 👤 Participant

| Field            | Value                                |
| ---------------- | ------------------------------------ |
| Full Name        |     Nada Mohamed Ibrahim                                 |
| Project Name     |    AI SQL Analyst                                   |
| GitHub Username  |   NadaMohamedIbrahim                                   |
| Internship Batch | August–October 2026                  |
| Training Program | Large Language Models (LLMs) Program |
| Organization     | [**Edrak for Ai**](https://edrak4ai.com/en)                         |

---

# 📖 Project Overview

📊 AI SQL Analyst Agent
An end-to-end, AI-powered data analysis pipeline that allows users to query relational databases using natural language. This project leverages a locally-hosted Large Language Model (Mistral-Nemo-Instruct) to dynamically introspect database schemas, write and execute secure SQL queries, and generate automated business insights alongside Python-based data visualizations.The system is built on a decoupled architecture, separating the heavy LLM inference and database execution (FastAPI) from the user-facing interface (Streamlit).

---

# ✨ Features

* Decoupled Client/Server Model: A lightweight Streamlit frontend communicates via REST API to a FastAPI backend handling GPU inference.

* Low-VRAM Compatibility: Quantized to 4-bit precision, enabling the pipeline to run efficiently on free Kaggle/Colab T4 GPUs.

* Strict JSON Output Enforcement: Employs defensive prompt engineering and Regex fallbacks to ensure the LLM consistently returns parsable visualization code and analysis.

* Automated Data Cleaning: Normalizes messy CSV column headers (handling spaces and special characters) to prevent SQL execution failures.

---

# 🛠️ Technologies Used

* Large Language Model: Mistral-Nemo-Instruct-2407

* Model Optimization: BitsAndBytes (4-bit Quantization), Accelerate, PyTorch

* AI Orchestration: LangChain (Custom LLM Wrappers, PromptTemplates, StructuredOutputParsers)

* Backend: FastAPI, Uvicorn, SQLite, Pandas

* Frontend: Streamlit, Matplotlib, Pyngrok

---

# ⚙️ Installation

This project is packaged as a single Jupyter Notebook optimized for free-tier GPU environments like Google Colab or Kaggle.

* Launch the Environment: Click the "Open in Colab" badge above to load the notebook directly into Google Colab, or clone the repository and upload the .ipynb file to Kaggle. Ensure your runtime hardware accelerator is set to T4 GPU.

* Install Dependencies: Run the first cell to install the required libraries (streamlit, pyngrok, transformers, bitsandbytes, langchain, etc.).
  
* Build the Application: Run the second cell to write the unified Streamlit application (app.py) to the instance's local storage.
  
* Authenticate & Run: Execute the final cell. You will be prompted to securely enter your Ngrok Authtoken. Once entered, the script will launch the backend server and generate a public URL to access your live application.

---

# 🚀 Usage

* Access the Interface: Click the generated Ngrok public_url in the notebook output to open the Streamlit web app.

* Upload Data: In the left sidebar, click "Browse files" and upload any flat CSV dataset. The app will automatically sanitize the column headers and ingest the data into a local SQLite database in the background.

* Review Schema: The sidebar will update to display the dynamically extracted database schema (tables and columns), confirming the data is ready to query.

* Chat with your Data: Type natural language questions into the chat input (e.g., "What is the total revenue grouped by product line, sorted descending?" or "Show me a summary of sales by city").

* Analyze Outputs: The agent will execute the pipeline and display:
    * The generated SQL query.

    * The raw data results in a Pandas DataFrame.

    *  A synthesized business takeaway.

    * A rendered Matplotlib chart based on the query results.

---

# 📸 Demo

**Data Source Upload**

![Upload Interface](Demo/Screenshot%202026-10-08%20060437.png)


**SQL Generation and Results**

![SQL Query](Demo/Screenshot%202026-10-08%20060754.png)


**Automated Business Analysis**

![Business Analysis](Demo/Screenshot%202026-10-08%20061053.png)


**Dynamic Visualization**

![Visualization Chart](Demo/Screenshot%202026-10-08%20061145.png)

---

# 📈 Results

* Frictionless Deployment: Consolidated the backend LLM inference and frontend Streamlit GUI into a single executable notebook, allowing users to spin up a fully functional AI agent in under two minutes without local environment configuration.

* Optimized Hardware Utilization: Leveraged BitsAndBytes 4-bit quantization on the Mistral-Nemo-Instruct-2407 model, enabling a high-parameter agent to run smoothly within the 16GB VRAM constraints of a free cloud GPU.

* Defensive Pipeline Architecture: Engineered strict PromptTemplates and Regex fallback parsers to mitigate common LLM hallucinations, ensuring stable SQL execution, accurate Pandas column mapping, and reliable JSON output generation.

* Automated Data Sanitization: Built a pre-processing ingestion layer that automatically normalizes messy CSV headers, preventing execution failures caused by spaces or special characters in SQL queries.

---

# 🔮 Future Improvements

* Multi-Turn Conversational Memory: Integrate LangChain's ConversationBufferMemory so the agent can remember previous queries and apply iterative filters (e.g., "Now show me that previous chart, but only for female customers").

* Multi-Table Relational Support: Upgrade the file uploader to accept multiple CSVs simultaneously, automatically mapping primary and foreign keys to support complex JOIN queries.

* Report Export Functionality: Add a utility for users to download the generated SQL, DataFrames, and Matplotlib charts as a consolidated PDF or HTML business report.

---

# 📚 About the Internship

This project was developed as part of the [**Tips Hindawi**](https://www.tipshindawi.com/) **Internship (August–October) 2026**, and it will be showcased on the official [Tips Hindawi](https://www.tipshindawi.com/) website.

[Tips Hindawi](https://www.tipshindawi.com/) is the internships department of [**Edrak for Ai**](https://edrak4ai.com/en), and the internship encourages participants to build real-world projects, apply practical skills, and showcase their work through GitHub.

For more information about the internship, training programs, and upcoming batches, visit the official [Tips Hindawi](https://www.tipshindawi.com/) website.

---

# 📄 License

This project is shared for educational and portfolio purposes.
