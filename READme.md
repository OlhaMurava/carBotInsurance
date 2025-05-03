Telegram Car Insurance Bot 🤖
A smart Telegram bot that helps users easily apply for car insurance by uploading their passport and vehicle documents. It uses OCR to extract data and OpenRouter AI to generate the insurance policy.

🛠️ Setup Instructions
1. Clone the repository

git clone https://github.com/OlhaMurava/carBotInsurance.git

cd telegram-insurance-bot

2. Install dependencies

npm install

3. Configure environment variables
Create a .env file in the root folder and add the following:

TELEGRAM_BOT_TOKEN=your_telegram_bot_token

OPENROUTER_API_KEY=your_openrouter_api_key

RENDER_EXTERNAL_URL=https://your-app-name.onrender.com

PORT=3000

⚠️ Make sure your bot token and API keys are valid.

4. Run the bot locally

node bot.js
Or deploy it on Render or another cloud platform that supports HTTPS.

📦 Dependencies
node-telegram-bot-api – Telegram bot API wrapper

axios – For making HTTP requests

express – Web server for Telegram webhook

body-parser – Middleware for parsing request bodies

dotenv – For loading environment variables

mindee - Mindee is used in my bot to automatically extract user information—like name, birth date, and vehicle ID—from uploaded passport and vehicle document images using OCR.


🔁 Bot Workflow
/start – Initiates the process and asks the user to upload a passport 📸

User uploads passport – Data is extracted using OCR 🧾

Bot requests vehicle document – User uploads it 🚗

/confirm – Bot shows summary and asks for confirmation ✅

"yes" – Policy is generated with OpenRouter AI 🧠

"no" – Bot ends interaction politely ❌

/retry – Restarts the flow 🔄
