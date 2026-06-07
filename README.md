# AI Chatbot Project

This project implements a simple, interactive AI chatbot. It uses **Streamlit** for the frontend user interface, **Google Gemini** (specifically `gemini-2.5-flash-lite`) as the Large Language Model (LLM), and **LangGraph** to manage the conversation flow and state.

## Project Structure

*   `streamlit_frontend.py`: The entry point for the application. It handles the web interface, user input, and displaying the conversation history using Streamlit.
*   `langgraph_backend.py`: Contains the core logic for the chatbot. It defines the state graph using LangGraph, integrates the Google Gemini model, and manages conversation history using an in-memory saver.
*   `requirements.txt`: Lists all Python dependencies required to run the project.
*   `.env` (Not tracked by Git): A file where you should store your API keys.

## Features

*   **Interactive Web UI:** Built with Streamlit for a smooth chatting experience.
*   **Stateful Conversation:** Remembers previous messages in the current session using LangGraph's checkpointer.
*   **Google Gemini Integration:** Utilizes the powerful `gemini-2.5-flash-lite` model for generating responses.

## Setup Instructions

### Prerequisites

Ensure you have Python installed on your system.

### 1. Clone the repository

```bash
git clone <repository_url>
cd ai-chatbot
```

### 2. Install dependencies

It is recommended to use a virtual environment. Install the required packages using pip:

```bash
pip install -r requirements.txt
```

### 3. Configure Environment Variables

Create a file named `.env` in the root directory of the project. Add your Google API key to this file:

```
GOOGLE_API_KEY=your_api_key_here
```
*(Note: Replace `your_api_key_here` with your actual Google Gemini API key)*

## Running the Application

To start the chatbot, run the Streamlit frontend script:

```bash
streamlit run streamlit_frontend.py
```

This will launch a local web server, and you can interact with the chatbot in your browser.