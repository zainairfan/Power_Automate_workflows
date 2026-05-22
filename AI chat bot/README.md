# 💬 AI Chatbot using Power Automate Desktop + Gemini API

A simple AI chatbot built using Power Automate Desktop (PAD) that integrates with Google Gemini API to generate real-time AI responses. The user types a question, PAD sends it to Gemini API, receives the response, and shows it in a message box. The chatbot can be stopped anytime by typing "exit".

## Features
This chatbot provides a simple input dialog where the user can ask questions. It connects with Google Gemini 2.5 Flash model using a REST API POST request. The response is returned in JSON format, parsed inside PAD, and the AI answer is displayed in a message box.

## Technologies Used
Power Automate Desktop (PAD), Google Gemini API, HTTP Web Service (POST Request), and JSON Parsing are used in this project.

## Setup Instructions
First, generate your API key from https://aistudio.google.com/ and copy it. Then in your PAD flow, replace %ApiKey% with your actual Gemini API key. The API endpoint used is https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash:generateContent?key=YOUR_API_KEY.

## How It Works
The user enters a prompt in an input dialog. If the user types "exit", the flow stops. Otherwise, the input is sent to Gemini API. The API returns a JSON response, and the chatbot extracts the answer from candidates[0].content.parts[0].text. The extracted response is then shown in a message box.

## Request Body
The API request body contains:
{
  "contents": [
    {
      "parts": [
        {
          "text": "USER_INPUT"
        }
      ]
    }
  ]
}

## Example
User: What is AI?
Bot: Artificial Intelligence is the simulation of human intelligence in machines that are programmed to think and learn.

## Exit Command
Type "exit" to stop the chatbot.

## Workflow
Input Dialog → API Request → JSON Response → Parse Response → Display Message

## Future Improvements
This project can be improved by adding continuous chat mode, saving chat history, improving error handling, enhancing UI, and adding multi-language support.

## Author
Built using Power Automate Desktop and Google Gemini API.
