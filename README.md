🚀 AI Customer Service & Follow Up Automation (n8n)

Sistem otomatisasi Customer Service & Sales Follow Up berbasis Telegram Bot, Google Sheets, dan AI Agent menggunakan n8n.

Workflow ini dirancang untuk:

Menerima pesan masuk dari Telegram

Mengecek dan menyimpan data ke Google Sheets

Menggunakan AI untuk memahami intent user

Mengarahkan user ke Sales atau Support

Mengirim pesan otomatis sesuai kategori

Update status follow-up secara otomatis

🧠 System Architecture

Workflow utama terdiri dari:

Telegram Trigger

Menerima pesan dari user secara real-time

Google Sheets Integration

Cek data user

Append row (jika user baru)

Update row (jika user lama)

AI Agent

Menggunakan OpenRouter Chat Model

Memory support untuk konteks percakapan

Membantu klasifikasi intent (Sales / Support)

Switch Logic

Routing otomatis berdasarkan intent

Memisahkan alur Sales & Support

Auto Messaging

Kirim pesan otomatis sesuai kategori

Follow-up logic dengan Wait Node

⚙️ Features

✅ Auto customer detection

✅ Auto lead capture ke Google Sheets

✅ AI-based intent classification

✅ Sales & Support routing

✅ Follow-up automation

✅ Structured data update system

✅ Scalable for SaaS / Agency use

📂 Project Structure (Recommended)
n8n-ai-cs-automation/
│
├── docker-compose.yml
├── .env.example
├── workflows/
│   └── cs-followup.json
├── README.md
└── .gitignore

🔧 Setup Guide
1️⃣ Clone Repository
git clone https://github.com/username/repository-name.git
cd repository-name

2️⃣ Setup Environment Variables

Copy:

.env.example → .env


Isi dengan:

TELEGRAM_BOT_TOKEN=
GOOGLE_SHEETS_CREDENTIALS=
OPENROUTER_API_KEY=

3️⃣ Run n8n (Docker Recommended)
docker compose up -d

📊 Workflow Logic Overview
Telegram → Check User in Sheet → 
IF Exists → Update Row
IF Not Exists → Append Row

↓
AI Agent → Detect Intent
↓
Switch:
   - Sales → Send Sales Message
   - Support → Send Support Message

↓
Wait → Update Follow-Up Status

🎯 Use Cases

Lead generation automation

Telegram-based customer service bot

AI-powered sales qualification

Small business automation

SaaS onboarding bot

Agency automation template

🔐 Security Notes

Do NOT upload .env

Do NOT upload .n8n/database.sqlite

Use .env.example for template only

Always secure Telegram & API keys

🚀 Future Improvements

CRM integration

WhatsApp integration

Dashboard analytics

AI response personalization

Auto-tagging system

Multi-language support

🧩 Tech Stack

n8n

Telegram Bot API

Google Sheets API

OpenRouter (LLM)

Docker

📌 Author

Ageng Lahsa Adiguna
AI Automation Developer | Workflow Engineer | AI System Builder
