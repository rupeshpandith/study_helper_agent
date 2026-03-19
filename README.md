# Study Helper AI Agent

An AI agent built with Google ADK and Gemini 2.5 Flash, deployed on Cloud Run.

## What it does
Accepts a topic or pasted text and returns a structured JSON response containing:
- A summary of the topic
- Flashcards for studying
- A multiple choice quiz

## Live endpoint
https://study-helper-agent-366648389389.us-central1.run.app

## Test it
```bash
curl -X POST https://study-helper-agent-366648389389.us-central1.run.app/run \
  -H "Content-Type: application/json" \
  -d '{
    "appName": "study_helper_agent",
    "userId": "u_001",
    "sessionId": "s_001",
    "newMessage": {
      "role": "user",
      "parts": [{ "text": "Topic: Photosynthesis" }]
    }
  }'
```

## Stack
- Google ADK
- Gemini 2.5 Flash via Vertex AI
- Cloud Run
