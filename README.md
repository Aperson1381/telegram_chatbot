
# 🤖 Saleh's AI Telegram Chatbot

A Persian-speaking AI-powered Telegram chatbot built using Python, OpenAI API (via Gilas.io), and the `python-telegram-bot` library. The bot responds to users intelligently, logs messages from private and group chats, and can be deployed on any Telegram bot token.

## 🧠 Features

- 💬 Supports private chats, groups, supergroups, and channels (when mentioned).
- 🤖 Intelligent replies powered by GPT (via Gilas API).
- 🇮🇷 Replies in Persian by default.
- 📁 Logs all messages from private and group chats.
- ✅ Custom system prompt for friendly, informative, and helpful interactions.
- 📜 Message history tracking for contextual conversations.
- 🛡 Filters out spam and inappropriate requests (e.g. admin commands).

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/telegram-ai-bot.git
cd telegram-ai-bot
```

### 2. Install Dependencies

This project uses `python-telegram-bot`, `openai`, and `python-dotenv`:

```bash
pip install python-telegram-bot openai python-dotenv
```

### 3. Set up Environment Variables

Create a `.env` file and include your OpenAI API key and bot token:

```env
TELEGRAM_TOKEN=your_telegram_bot_token
OPENAI_API_KEY=your_openai_or_gilas_api_key
```

> ⚠️ **Never hardcode sensitive information like API keys or bot tokens directly in your source code.**

### 4. Run the Bot

```bash
python bot.py
```

You should see:

```bash
starting bot...
polling...
```

Your bot is now live and polling messages!

## 📂 Project Structure

```
├── bot.py                 # Main bot logic
├── .env                  # Environment variables (do not share publicly)
├── private_messages.log  # Log of private messages
├── group_messages.log    # Log of group/supergroup messages
├── requirements.txt      # Optional: dependencies list
```

## ⚙️ Bot Behavior

- **Commands**:
  - `/start` – Greets the user.
  - `/help` – Explains how to use the bot.
  - `/custom` – A placeholder command for future features.

- **Message Handling**:
  - Replies to private messages directly.
  - Replies in groups or channels only if mentioned using `@saleh_helper_bot`.
  - Uses the last 10 messages for contextual response generation.
  - Applies a detailed system prompt to shape personality and behavior.

## 📌 System Prompt Highlights

The bot is instructed to:

- Respond only in Persian unless English is necessary.
- Be friendly, informative, and emoji-using.
- Reject admin command requests politely.
- Say who created it when asked:  
  `"من یک ربات هوش مصنوعی هستم که توسط صالح با آیدی @a_person0_0 دولوپ شدم."`

## 📒 Logs

All incoming messages (except from channels) are logged:

- `private_messages.log` – Logs user ID and messages from private chats.
- `group_messages.log` – Logs user ID and messages from groups with group name if available.

## 🛑 Security Notes

- **DO NOT expose your bot token or OpenAI API key** in code or public repositories.
- Always use environment variables (`.env`) to store sensitive information.

## 🧑‍💻 Developer

Developed by **Saleh**  
Telegram: [@a_person0_0](https://t.me/a_person0_0)  
Bot Username: [@saleh_helper_bot](https://t.me/saleh_helper_bot)

---
