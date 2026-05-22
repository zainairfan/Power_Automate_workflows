# 📧 AI Email Classification Automation using Power Automate Desktop + Google Gemini AI

## 📌 Project Overview

This project automates the process of reading unread emails from Microsoft Outlook, sending them to Google Gemini AI for intelligent classification, and displaying the predicted department/category.

The system automatically categorizes emails into HR, Finance, Sales, Support, Technical, Legal, and Unclassified using AI.

It is built using Power Automate Desktop (PAD) and integrates with Google Gemini API for smart email classification.

---

## ⚙️ Tools & Technologies

Power Automate Desktop (PAD), Microsoft Outlook, Google Gemini API (Gemini 2.5 Flash), Web Service (HTTP POST), JSON Parsing.

---

## 🚀 Workflow

The automation starts by launching Outlook and retrieving all unread emails from the Inbox (Account: zaina.irfan@devspro.com). Each email is marked as read after retrieval.

For every email, the Subject and Body are extracted and combined into a single text format:

Subject: <Email Subject>  
Body: <Email Body>

This text is then sent to the Gemini API using an HTTP POST request with the prompt:

“You are an email classifier. Classify into ONE category only: HR, Finance, Sales, Support, Technical, Legal, Unclassified. Return only one word.”

The API response is returned in JSON format, and the classification is extracted from:

candidates[0].content.parts[0].text

Finally, a message box displays the email content along with the predicted department.

---

## 🧠 Example Output

Subject: Job Interview Invitation  
Body: You are invited for an interview on Monday at 10 AM...  

Department: HR

---

## 📂 Project Structure

Email-Classification-Automation/  
├── Flow (Power Automate Desktop file)  
├── Screenshots (workflow screenshots)  
└── README.md  

---

## ✨ Key Features

Automated Outlook email reading, AI-based email classification using Google Gemini, real-time department detection, and zero manual sorting required.

---

## ⚠️ Requirements

Outlook must be configured and logged in, a valid Google Gemini API key is required, and an active internet connection is needed for API calls.

---

## 👩‍💻 Author

Zaina Irfan 
