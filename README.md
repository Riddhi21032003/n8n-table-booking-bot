# n8n-table-booking-bot
AI-powered restaurant table booking bot built with n8n, Groq, and Google Sheets.
# 🍽️ AI Table Booking Bot (n8n)

🚀 A production-ready AI-powered restaurant booking system built using **n8n**, **Groq LLM**, and **Google Sheets**.

This project demonstrates how to design an **AI agent workflow** that handles real-world constraints like availability checking and conflict prevention—without writing backend code.

---

## 🎯 Project Highlights

* Built an **AI-driven booking system** using n8n workflows
* Designed an **agent-based decision system** (not just simple automation)
* Implemented **conflict detection logic** (no double bookings)
* Integrated **LLM (Groq)** with structured tools (Google Sheets)
* Created a **chat-first user experience**
* Demonstrates **no-code + AI engineering skills**

---

## 🧠 How It Works

1. User sends a booking request via chat
2. AI Agent extracts:

   * Name
   * Date
   * Time
   * Number of people
3. Agent checks existing bookings in Google Sheets
4. Decision logic:

   * If slot exists → reject + ask for new time
   * If slot free → add booking + confirm

---

## 🏗️ Architecture Diagram

*(Add this image after uploading to your repo — instructions below)*

```
User → Chat Trigger → AI Agent
                      ↓
              ┌───────────────┐
              │   Memory      │
              └───────────────┘
                      ↓
        ┌─────────────┴─────────────┐
        ↓                           ↓
Read Bookings Tool        Add Bookings Tool
(Google Sheets)           (Google Sheets)
        ↓                           ↓
            → Decision Logic →
                Response to User
```

---

## 📸 Screenshots

### 🔹 Workflow Overview with Chat Interface

<img width="2048" height="1092" alt="workflow" src="https://github.com/user-attachments/assets/85166f1d-159e-4eac-9641-80123a2d6978" />

---

### 🔹 Excel Sheet Preview

<img width="1164" height="420" alt="Excel sheet" src="https://github.com/user-attachments/assets/cf19fdf6-c078-44a0-9900-a2329b34f233" />

---

## 🧩 Workflow Components

| Component          | Purpose                        |
| ------------------ | ------------------------------ |
| Chat Trigger       | Starts conversation            |
| AI Agent           | Core logic + decision making   |
| Memory             | Maintains conversation context |
| Read Bookings Tool | Fetches existing bookings      |
| Add Bookings Tool  | Writes new bookings            |
| Groq Model         | Powers AI reasoning            |

---

## 🛠️ Tech Stack

* **Automation:** n8n
* **AI Model:** Groq LLM
* **Database:** Google Sheets
* **Architecture:** Tool-augmented AI Agent

---

## ⚙️ Setup Guide

### 1. Import Workflow

* Open n8n
* Go to **Workflows → Import from File**
* Upload `table-booking-bot-n8n.json`

### 2. Configure Credentials

* Add **Groq API Key**
* Connect **Google Sheets OAuth**

### 3. Setup Google Sheet

Create columns:

```
Name | Date | Time | Number of People
```

### 4. Update Nodes

* Select your Google Sheet in both tools
* Map fields correctly

### 5. Activate Workflow

* Enable workflow
* Open Chat Trigger URL

---

## 💬 Example Interaction

### User

```
Book a table for Sarah on Friday at 8 PM for 2 people
```

### AI Response (Available)

```
Your table has been successfully booked.
```

### AI Response (Conflict)

```
That time slot is already taken. Please choose another time.
```

---

## 📁 Project Structure

```
n8n-table-booking-bot/
├── n8n-table-booking-bot.json
├── README.md
├── assets/
│   ├── workflow.png
│   └── excel sheet.png
├── .gitignore
└── LICENSE
```

---

## 🧑‍💻 What This Project Shows

* AI Agent design (not just prompt usage)
* Real-world constraint handling
* Tool integration with LLMs
* Workflow automation skills
* Practical AI application building

---

## ⭐ Future Improvements

* Add calendar integration
* Add booking cancellation flow
* Add WhatsApp / Telegram interface
* Store data in database (PostgreSQL / Firebase)
* Add time-slot suggestions

---
