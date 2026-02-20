# 🤖 WhatsApp Booking Bot & Time Collision Engine

## 📌 Overview
This repository showcases an automated appointment booking system built with **Google Apps Script**. It acts as a Webhook for WhatsApp, utilizing a **State Machine** to guide users through a conversational booking flow while securely managing temporal session data. 

Developed as a core module for a service-industry CRM (Mi Data Flow).

## 💡 Engineering Highlights
Building a chatbot that just replies is easy; building one that remembers context and handles real-world scheduling constraints is complex. This module demonstrates:

1. **State Machine Logic:** Uses `CacheService` to remember exactly where the user is in the conversation flow (e.g., waiting for location, waiting for date, waiting for time), creating a seamless session without needing an external database.
2. **Time Collision Algorithm:** Implements a robust mathematical check (`verificarDisponibilidad`) to convert hours to minutes and detect overlapping time blocks. It prevents double-booking across different staff members in real-time.
3. **Data Sanitization:** Cleans and parses user inputs (handling both 12h and 24h formats intelligently).

## 🛠️ Tech Stack & APIs
* **Google Apps Script (ES6)**
* **CacheService:** For temporary, fast-access session storage (in-memory caching).
* **SpreadsheetApp API:** Used as the persistent database for final booking records.
* **REST APIs / Webhooks:** `doPost(e)` implementation to catch incoming JSON payloads from the WhatsApp Business API provider.

## 💼 Business Value
* **24/7 Automation:** Replaces manual receptionist work by guiding clients through the entire funnel autonomously.
* **Zero Double-Booking:** The collision engine guarantees operational efficiency.
* **Serverless Architecture:** Completely hosted within the Google Workspace ecosystem, reducing server costs to zero.

---
*Built to solve real business bottlenecks with smart, serverless automation.*
