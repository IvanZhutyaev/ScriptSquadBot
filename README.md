# Telegram Bot for Client Communication and Manager Redirection

This Telegram bot is designed to automate initial client interactions, provide service information, and redirect clients to appropriate managers.

## Bot Features

- Welcomes new users
- Provides information about various service categories
- Collects client requests
- Forwards requests to managers
- Interactive menu with buttons for convenient navigation

## Installation and Setup

1. Ensure you have Python 3.6 or higher installed
2. Install required dependencies:
   ```bash
   pip install pyTelegramBotAPI
   ```
3. Create a `config.py` file and add your credentials:
   ```python
   TOKEN = 'YOUR_TELEGRAM_BOT_TOKEN'
   MANAGER_CHAT_ID = 123456789  # Manager's chat ID
   ```
4. Run the bot:
   ```bash
   python bot.py
   ```

## Configuration

Before launching:

1. Replace `'YOUR+BOT_TOKEN'` with your actual bot token
2. Specify the correct manager's `chat_id` in:
   ```python
   manager_chat_id = 0  # Replace with actual manager's chat ID
   ```

## Project Structure

- `bot.py` - main bot logic file
- `config.py` - configuration file (bot token, manager ID)

## Technologies Used

- [python-telegram-bot](https://github.com/eternnoir/pyTelegramBotAPI) - Telegram Bot API library
- Python standard libraries

## Service Categories

The bot handles these main service types:
- 📢 Advertising services
- 🛠 Custom services (with subcategories):
  - 🌐 Websites
  - 🤖 Bots
  - 🎮 Games
  - 📈 Marketing
  - 📢 Channel management
  - 💻 Software
  - 👥 Inviting
  - ❓ Other services
- 🤝 Partnership opportunities

## Expansion Possibilities

1. Add database integration for request storage
2. Connect to CRM systems
3. Implement notification system for managers
4. Add multi-language support

## Contacts

For customization or collaboration inquiries: @IvanZhutyaev
