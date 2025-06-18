🎯 The Problem
In any data-driven project, 80% of the work is often data preparation. Messy, inconsistent, and incomplete data leads to inaccurate analysis and unreliable AI models. Traditional cleaning methods are manual, time-consuming, and struggle with complex, context-specific errors.

✨ Our Solution
The AI-Powered Data Cleaning System tackles this challenge head-on. It provides an intuitive web interface to ingest data from multiple sources (Files, Databases, APIs) and leverages a dual-engine approach to cleaning:

Robust Rule-Based Cleaning: Handles the common, predictable issues like missing values, duplicates, and formatting inconsistencies.
Intelligent AI-Powered Cleaning: Utilizes LangChain AI Agents to understand the context of your data and perform complex transformations that rules alone cannot handle.
This system is designed to drastically reduce cleaning time, improve data quality, and empower you to focus on what truly matters: deriving insights from your data.

🚀 Key Features
✅ Multi-Source Ingestion: Pull data from CSV/Excel files, live SQL queries, or REST API endpoints.
✅ AI-Driven Cleaning: Employs LangChain Agents for intelligent, context-aware data transformation.
✅ Automated Preprocessing: Systematically handles missing values, removes duplicates, and standardizes formats.
✅ Interactive Web UI: A clean and user-friendly interface built with Streamlit for effortless interaction.
✅ High-Performance Backend: Powered by FastAPI for fast, asynchronous request handling.
✅ Real-Time Preview: Instantly see a side-by-side comparison of your raw and cleaned data.

⚙️ System Architecture
The application operates on a simple yet powerful client-server architecture.

Frontend (Streamlit): The user interacts with the Streamlit UI to select a data source and submit it. The frontend sends a request to the FastAPI backend.
Backend (FastAPI): The backend receives the request and orchestrates the cleaning process. It fetches data if necessary (from a DB or API), applies the rule-based and AI-powered cleaning pipelines, and returns the cleaned data.
AI Agent (LangChain): The LangChain agent, powered by a Large Language Model (LLM), performs sophisticated transformations on the data before it's finalized.
Data Flow: User -> Streamlit UI -> FastAPI Backend -> LangChain Agent -> FastAPI -> Streamlit UI -> User


🏁 Getting Started
Follow these instructions to get a copy of the project up and running on your local machine.

Prerequisites

Python 3.9+
An API key from an LLM provider (e.g., OpenAI) added to your environment variables.
1. Clone the Repository

Bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
2. Create and Activate a Virtual Environment

This keeps your project dependencies isolated.

Bash
# Create the environment
python -m venv venv

# Activate it
# On Windows:
venv\Scripts\activate
# On MacOS/Linux:
source venv/bin/activate
3. Install Dependencies

 This command installs all the necessary Python packages.

Bash
pip install -r requirements.txt
4. Configure Environment Variables

Create a .env file in the root directory of the project and add your API keys.

Code snippet
# .env file
OPENAI_API_KEY="your-api-key-here"
DATABASE_URL="postgresql://user:password@host:port/dbname"
5. Run the Application

You'll need to run the backend and frontend in two separate terminals.

Terminal 1: Start the FastAPI Backend
<!-- end list -->

Bash
uvicorn scripts.backend:app --reload
The backend will be available at http://127.0.0.1:8000.

Terminal 2: Start the Streamlit UI
<!-- end list -->

Bash
streamlit run app/app.py
The frontend will open automatically in your browser at http://127.0.0.1:8501.

🚀 Usage
Once the application is running, open your web browser to the Streamlit URL.

Choose a Data Source from the sidebar (Upload File, SQL Query, or API).
Provide the Input (upload the file or enter the required text).
Click "Clean Data".
Review the Results: The application will display the original data and the AI-cleaned data side-by-side for comparison.
(Optional: Consider adding a GIF here showing the application in action!)

