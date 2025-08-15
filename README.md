<div align="center">

# 🔮 TDS Data Analyst Agent 🔮

**An AI-powered assistant that transforms your raw data and questions into actionable insights, stunning visualizations, and intelligent recommendations in seconds.**

</div>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.9+-blue?logo=python&logoColor=white" alt="Python Version">
  <img src="https://img.shields.io/badge/Framework-FastAPI-green?logo=fastapi" alt="FastAPI">
  <img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT">
  <img src="https://img.shields.io/badge/AI-Google_Generative_AI-orange?logo=google-cloud" alt="AI Engine">
</p>

---

> Tired of tedious data wrangling? Let our AI agent do the heavy lifting. Simply upload your dataset and questions, and watch as it uncovers hidden patterns, generates beautiful charts, and delivers the insights you need. Perfect for analysts, researchers, and data enthusiasts of all levels.

## ✨ Key Features

* **🤖 AI-Driven Analysis:** Leverages the power of Google's Generative AI to provide deep, contextual insights.
* **📊 Interactive Visualizations:** Automatically generates beautiful charts and graphs using Matplotlib & Seaborn.
* **🌐 Web Scraping:** Instantly import and analyze data directly from any URL.
* **📁 Multi-Format Support:** Works seamlessly with `CSV`, `Excel`, `JSON`, `Parquet`, and `TXT` files.
* **⚡ Batch Processing:** Ask multiple questions at once and get a comprehensive report in a single run.
* **💻 Modern UI:** A clean, responsive, and intuitive interface that's beginner-friendly.
* **🚀 Blazing Fast:** Real-time progress updates and optimized computations for quick results.
* **🧪 Dedicated Test Page:** Access the full UI at `/test` for a seamless experience and easy integration with deployments.

## 🚀 Getting Started in 3 Easy Steps

### 1. **Install Dependencies**
Fire up your terminal and run:
```bash
pip install -r requirements.txt
```

### 2. **Configure Your Environment**
Create a `.env` file in the project's root directory and add your Google Generative AI API key.

```env
# You can add up to 10 API keys (gemini_api_1, gemini_api_2, ...)
gemini_api_1=your_google_generative_ai_api_key

# Set the timeout for the language model
LLM_TIMEOUT_SECONDS=150
```

### 3. **Launch the App**
Start the server with this command:
```bash
python app.py
```
Now, navigate to `http://localhost:8000` in your web browser to start analyzing!

## 💡 How to Use

1.  **Prepare Your Questions:** Create a `.txt` file and list all your questions, with one question per line.
2.  **Upload Your Files:**
    * **Required:** Your questions `.txt` file.
    * **Optional:** A dataset file (`.csv`, `.xlsx`, `.json`, etc.).
3.  **Get Insights:** The agent will process your request and generate a report with visualizations and recommendations.
4.  **Test the UI:** Visit `/test` in your browser to access the modern UI for uploading files and interacting with the agent.

## 🛠️ Tech Stack

| Area      | Technologies                                                        |
| :-------- | :------------------------------------------------------------------------ |
| **Backend** | FastAPI, LangChain, Google Generative AI, Pandas, NumPy, Matplotlib, Seaborn |
| **Frontend**| HTML5, CSS3, JavaScript                                                      |

## ☁️ Deployment

You can deploy the agent in various environments.

### Local Development
```bash
python app.py
```

### Production (using Gunicorn)
```bash
  gunicorn app:app -w 4 -k uvicorn.workers.UvicornWorker
```

### Docker
Build and run the container:
```dockerfile
# Use an official Python runtime as a parent image
FROM python:3.9-slim

# Set the working directory
WORKDIR /app

# Copy and install the requirements
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application
COPY . .

# Expose the port and run the app
EXPOSE 8000
CMD ["python", "app.py"]
```

## 🔒 Security

Your data privacy is important.
-   **Local Processing:** All data is processed locally on your machine and is not stored in the cloud.
-   **Secure API Keys:** API keys are managed securely using environment variables.
-   **Configurable CORS:** Cross-Origin Resource Sharing (CORS) can be configured for production environments.

## 📄 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details. Feel free to use, modify, and share!
\n---

<div align="center">
Made with ❤️ for the data community.
</div>