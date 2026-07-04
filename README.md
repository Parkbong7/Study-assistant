# Study Assistant 🎓

An AI-powered Study Assistant built with **Gradio** and **Google's Gemini API**. Ask any question and get an explanation tailored to your preferred learning style — friendly and beginner-focused, or strictly academic.

🔗 **Live Demo:** [Add your Hugging Face Space link here]

## Features

- Ask any question and get a clear, structured explanation
- Choose between two AI personalities:
  - **Friendly** – enthusiastic, encouraging, uses simple analogies
  - **Academic** – formal, precise, uses academic terminology
- Follow-up questions included in every response to reinforce understanding
- Powered by Google's `gemini-2.5-flash` model

## Tech Stack

- [Gradio](https://www.gradio.app/) – web interface
- [google-genai](https://pypi.org/project/google-genai/) – Gemini API client

## Setup & Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/<your-username>/<repo-name>.git
   cd <repo-name>
   ```

2. **Create a virtual environment (recommended)**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up your API key**

   Get a Gemini API key from [Google AI Studio](https://aistudio.google.com/apikey), then set it as an environment variable:
   ```bash
   export GEMINI_KEY="your-api-key-here"   # On Windows: set GEMINI_KEY=your-api-key-here
   ```

   Alternatively, create a `.env` file in the project root:
   ```
   GEMINI_KEY=your-api-key-here
   ```

5. **Run the app**
   ```bash
   python app.py
   ```

   The app will launch locally (Gradio will print a local URL, typically `http://127.0.0.1:7860`).

## Usage

1. Type your question into the text box.
2. Select a personality — **Friendly** or **Academic**.
3. Click submit and read your personalized explanation.

## Project Structure

```
.
├── app.py              # Main application logic and Gradio UI
├── requirements.txt    # Python dependencies
└── README.md
```

## Troubleshooting

- **`NameError: name 'types' is not defined`** — Make sure to import the `types` module from the Gemini SDK at the top of `app.py`:
  ```python
  from google.genai import types
  ```
- **`GEMINI_KEY` not found** — Ensure the environment variable is set correctly before running the app, or that your `.env` file is loaded (you may need `python-dotenv` for local `.env` support).

## License

[Add your license here, e.g., MIT]

## Acknowledgements

Built with [Gradio](https://www.gradio.app/) and [Google Gemini](https://ai.google.dev/).
