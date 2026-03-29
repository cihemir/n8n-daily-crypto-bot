# n8n Daily Crypto and Market Tracking Bot

This project is an autonomous data retrieval and notification automation developed using the **n8n (Workflow Automation)** platform. The system triggers every morning at a scheduled time, connects to an external financial API, processes the incoming data, and delivers a report to the user via Telegram.

## Technologies Used
- **n8n:** Visual workflow design and scheduling (Cron jobs).
- **JavaScript:** Data parsing and string manipulation.
- **RESTful API:** Real-time data retrieval via GET requests from the CoinGecko API.
- **JSON:** Data transfer and structural configuration.
- **Telegram Bot API:** Instant push notification delivery to the user.

## How It Works
1. **Schedule Trigger:** The system initiates autonomously every morning at 09:00 (or at a user-defined interval).
2. **HTTP Request:** Connects to the CoinGecko API to retrieve real-time Bitcoin and Ethereum prices in JSON format.
3. **Code Node (JavaScript):** The complex incoming JSON data is filtered; specific price information is assigned to variables and transformed into a readable string template.
4. **Telegram Integration:** The final processed text is sent to the user's personal ID via a dedicated Telegram bot.
