# **🤖 Telegram Customer Support Bot**  

**A smart and interactive Telegram bot** for handling client inquiries, collecting service requests, and redirecting users to managers when needed.  

---

## **✨ Features**  

✅ **Interactive Menu System** – Easy navigation with buttons  
✅ **Service Catalog** – Detailed descriptions of all offerings  
✅ **Request Collection** – Gathers project details before forwarding  
✅ **Manager Redirection** – Seamlessly connects clients with support  
✅ **User-Friendly** – Simple and intuitive interface  

---

## **⚙️ Setup & Installation**  

### **Prerequisites**  
- Python 3.6+  
- A Telegram bot token (get it from [@BotFather](https://t.me/BotFather))  
- The manager’s Telegram **Chat ID** (use [@userinfobot](https://t.me/userinfobot) to find it)  

### **Installation Steps**  

1. **Clone the repository** (if applicable):  
   ```bash
   git clone https://github.com/IvanZhutyaev/ScriptSquadBot.git
   cd telegram-support-bot
   ```

2. **Install dependencies**:  
   ```bash
   pip install pyTelegramBotAPI python-dotenv
   ```

3. **Set up environment variables**:  
   - Rename `.env.example` to `.env`  
   - Fill in your details:  
     ```ini
     BOT_TOKEN=your_telegram_bot_token
     MANAGER_CHAT_ID=123456789  # Replace with actual manager's chat ID
     MANAGER_USERNAME=@manager_username  # Optional: Public contact
     ```

4. **Run the bot**:  
   ```bash
   python bot.py
   ```

---

## **📂 Project Structure**  

```
telegram-support-bot/
├── bot.py            # Main bot logic
├── .env              # Configuration (keep private!)
├── .env.example      # Template for environment variables
├── requirements.txt  # Python dependencies
└── README.md         # This documentation
```

---

## **📌 Usage Guide**  

### **For Users**  
- Start the bot with `/start`  
- Browse services using the **interactive menu**  
- Submit requests with descriptions (or skip)  
- Get confirmation when the request is forwarded  

### **For Admins**  
- The bot automatically forwards requests to the manager’s chat  
- Each request includes:  
  - Service type  
  - User details (username, Telegram ID)  
  - Project description (if provided)  

---

## **🔧 Customization**  

### **Modifying Services**  
Edit the `service_names` dictionary in `bot.py` to update:  
- Service categories  
- Descriptions  
- Button layouts  

Example:  
```python
service_names = {
    'web_dev': '🌐 Custom Website Development',
    'bot_creation': '🤖 Telegram Bot Development',
    # Add more services here
}
```

### **Changing Manager Details**  
Update in `.env`:  
```ini
MANAGER_CHAT_ID=123456789  # New manager's chat ID
MANAGER_USERNAME=@new_manager_username
```

---

## **🚀 Deployment Options**  

### **1. Local Testing**  
```bash
python bot.py
```

### **2. Cloud Hosting (Recommended)**  
- **VPS (DigitalOcean, Linode, AWS Lightsail)**  
  - Run in a `screen` or `tmux` session  
  - Use a process manager like `pm2` or `systemd`  

- **Serverless (AWS Lambda, Google Cloud Functions)**  
  - Requires additional setup (webhooks)  

### **3. Docker (Advanced)**  
```dockerfile
FROM python:3.9-slim
WORKDIR /app
COPY . .
RUN pip install -r requirements.txt
CMD ["python", "bot.py"]
```

---

## **🔒 Security Notes**  

⚠️ **Never expose your bot token or `.env` file publicly!**  
✅ **Best practices:**  
- Use environment variables (not hardcoded tokens)  
- Restrict bot access if needed  
- Regularly update dependencies  

---

## **📈 Future Improvements**  

🔹 **Database integration** (SQLite/PostgreSQL for request tracking)  
🔹 **Admin dashboard** (web interface for managing requests)  
🔹 **Multi-language support** (English/Russian/other languages)  
🔹 **Auto-responses** (FAQ handling before human takeover)  

---

## **📞 Contact & Support**  

For questions or custom development:  
- **Telegram:** [@IvanZhutyaev](https://t.me/zhutyaevivan)  
- **Email:** ivan.zhutyaev@mail.ru  
- **GitHub:** [Open My Git Hub](https://github.com/IvanZhutyaev)  

---

### **🎉 Ready to Deploy!**  
Replace all placeholders (`your-repo`, `@manager_username`, etc.) with your actual details, and your bot is good to go!  

🚀 **Happy automating!**
