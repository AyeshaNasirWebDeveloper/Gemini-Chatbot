# 🤖 Gemini Chatbot with GitHub Authentication

A conversational AI chatbot powered by Google's Gemini Pro, built with Chainlit and secured with GitHub OAuth authentication.

## Features

- 💬 Chat interface with conversational memory
- 🔒 GitHub OAuth login for secure access
- 🧠 Powered by Gemini 2.0 Flash model
- 📜 Maintains conversation history
- 🚀 Easy deployment with Chainlit

## Prerequisites

- Python 3.8+
- Google Gemini API key
- GitHub OAuth credentials (Client ID & Secret)
- Chainlit 2.0+

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/AyeshaNasirWebDeveloper/Gemini-Chatbot.git
   
   cd gemini-chatbot
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # Linux/Mac
   .venv\Scripts\activate    # Windows
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Configuration

1. Create a `.env` file:
   ```env
   GEMINI_API_KEY=your_api_key_here
   OAUTH_GITHUB_CLIENT_ID=your_client_id
   OAUTH_GITHUB_CLIENT_SECRET=your_client_secret
   ```

2. Configure `chainlit.yaml`:
   ```yaml
   # chainlit.yaml
   ui:
     name: "Gemini Chatbot"
     description: "AI assistant powered by Gemini"
     icon: "🤖"

   auth:
     required: true
     providers:
       - github

   oauth_providers:
     github:
       client_id: ${OAUTH_GITHUB_CLIENT_ID}
       client_secret: ${OAUTH_GITHUB_CLIENT_SECRET}
   ```

## Running the Application

Start the chatbot:
```bash
chainlit run main.py -w
```

The application will be available at `http://localhost:8000`

## Project Structure

```
.
├── main.py                # Main application code
├── chainlit.yaml         # Chainlit configuration
├── .env                  # Environment variables
├── requirements.txt      # Dependencies
```

## Dependencies

- `chainlit>=2.4.0`
- `google-generativeai>=0.3.0`
- `python-dotenv>=1.0.0`

## Deployment

### Local Development
```bash
chainlit run app.py
```

## Contributing

Pull requests are welcome! For major changes, please open an issue first.
