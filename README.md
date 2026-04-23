# 🐦 Internet Speed Complaint Bot (Python Automation)

A Python automation project that monitors your internet connection quality and automatically tweets at your Internet Service Provider (ISP) if your speeds are lower than what you are paying for.

The program uses Selenium to run a test on Speedtest.net, captures the download and upload results, and compares them against your "Promised Speeds." If the connection is underperforming, the bot logs into Twitter (X) and posts a public complaint tagging the provider.

This project demonstrates automated web testing, data extraction, conditional logic, and social media integration via browser automation.

---

## 🚀 Features

- 🏎️ Automated internet speed testing via Speedtest.net
- 📊 Real-time data extraction of Download and Upload speeds
- ⚖️ Conditional logic to compare actual speed vs. promised speed
- 🔐 Automated Twitter (X) login workflow
- 📝 Dynamic tweet generation with custom speed metrics
- 🛠️ Modern Selenium 4 implementation (Automatic Driver Management)

---

## 🛠 Technologies Used

- Python 3
- Selenium WebDriver
- Chrome WebDriver
- Time Library (Standard Python)

---

## 📂 Project Structure

speed-complaint-bot/
│
├── main.py           # Main automation script (OOP Class)
├── .gitignore        # Git ignored files
│
└── README.md

---

## ⚙️ Requirements

Ensure Python is installed:
python --version

Install Selenium:
pip install selenium

Note: Ensure you have Chrome installed. Selenium 4+ manages the ChromeDriver automatically so no manual path setup is required.

---

## 🚀 How to Run the Project

### Clone the Repository
git clone https://github.com/adebayoadesugba/speed-complaint-bot.git

### Navigate into the Project Folder
cd speed-complaint-bot

### Run the Script
python main.py

---

## 🔑 Configuration Setup

Before running the script, update the following variables in main.py:

PROMISED_DOWN = 150  # Set your contracted download speed
PROMISED_UP = 10     # Set your contracted upload speed
TWITTER_EMAIL = "your_email@example.com"
TWITTER_PASSWORD = "your_secret_password"

---

## ⚙️ How It Works

1️⃣ Initialization: The bot initializes a Chrome browser and sets internal variables for upload and download speeds to zero.

2️⃣ Speed Test Phase:
   - Navigates to Speedtest.net.
   - Clicks the "GO" button using a CSS Selector.
   - Waits for 60 seconds to allow the test to complete.
   - Scrapes the final numerical results using specific XPATHs.

3️⃣ Decision Phase: In the main execution, the script checks if the results are lower than the defined constants.

4️⃣ Twitter Phase: 
   - Navigates to the Twitter login page.
   - Enters credentials and navigates past security prompts.
   - Locates the tweet composition box.
   - Types a pre-formatted message: "Hey Internet Provider, why is my internet speed [Actual]down/[Actual]up when I pay for [Promised]down/[Promised]up?"
   - Clicks the "Tweet" button and closes the browser.

---

## 📊 Example Output

# Console output during run:
Speedtest started...
Testing complete.
Download: 45.2 Mbps
Upload: 2.1 Mbps
Speed is lower than promised! Initiating complaint tweet...
Login successful.
Tweet posted successfully.

---

## ⚠️ Security Warning

- Warning: Be careful with your login credentials. Use environment variables (.env) if you plan to share this code.
- Frequent automated logins may trigger Twitter's security verification (CAPTCHA or Email Code).
- Ensure your XPATHs are up to date, as social media platforms change their site structure frequently.

---

## 🧠 Key Concepts Demonstrated

- Object-Oriented Programming (Class-based structure)
- Browser Automation & Web Scraping
- Handling multi-site workflows in one script
- Dynamic string formatting (f-strings)
- Explicit and Implicit waiting strategies

---

## 🔮 Future Improvements

- Add logic to run the bot on a schedule (Cron Job)
- Integrate a database to log speed history over time
- Create a visual dashboard (Matplotlib) to show speed fluctuations
- Add multi-account support for different social media platforms

---

## 👨‍💻 Author

Adebayo Adesugba (Dev Bayo)

Full Stack Developer  
Python | JavaScript | React | Node.js | AI Development  

---

## ⭐ Support

If you like this project:
- ⭐ Star the repository
- 🍴 Fork it
- 🧑‍💻 Contribute

---

## 📜 License

This project is open-source and available under the MIT License.
