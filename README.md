# CS5001 Final Project: Scratch One More!

## Description

**Scratch One More!** is an interactive, gamified productivity web application built with Streamlit. It is designed to help you make progress on difficult tasks by breaking them up into manageable chunks and gamifying getting stuff done. 

The application offers two main modes accessed from the main menu:

1. **Strategic Planning (AI Coach)**: 
   Have a big, overwhelming goal? Enter your goal and how much time you have available. The AI Coach will use Google's Gemini AI to break your large goal down into simple, manageable steps, and guide you through completing them with a built-in timer.
2. **Quick Daily Tasks (Task Manager)**: 
   A simple, gamified TODO list where you can add, remove, and complete tasks. Completing tasks rewards you with encouraging feedback, compliments, and balloons!

## Prerequisites

- Python 3.13 or higher
- [uv](https://github.com/astral-sh/uv) (Extremely fast Python package installer and resolver)
- A Google Gemini API Key (required for the AI Coach functionality)

## Setup and Installation

1. Clone the repository and navigate to the project directory.
2. Fetch all required dependencies using `uv`:
   ```bash
   uv sync
   ```
3. Create a `.env` file in the root directory (or use environment variables) and add your Gemini API Key:
   ```env
   GEMINI_API_KEY=your_api_key_here
   ```

## Running the Application

To start the Streamlit web server and view the app in your browser, run:
```bash
uv run streamlit run main.py
```

## Running Tests

To run the unit tests for the task management logic, run:
```bash
uv run pytest test_task_app.py
```

## Structure

* `main.py` - The main entry point for the Streamlit web application.
* `task_app.py` - Core logic and state management for the conventional Task Manager side.
* `ai_task_coach/` - The AI Coach subsystem, which includes integration with the Gemini AI model, UI components, and session storage.
* `quotes.py` / `compliment_quotes.py` - Static definitions of motivational quotes and rewards.