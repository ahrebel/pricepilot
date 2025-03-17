# FlightWatch

FlightWatch is a simple and effective Python application that helps you track flight prices and receive email alerts when the prices drop below your set threshold. This tool allows you to either:
- Input specific flight details (airline, flight number, connections, etc.) for tracking, **or**
- Define broad search criteria (preferred airlines, max connections, price limit) to automatically track the best flights.

It scrapes Google Flights for real-time price updates and notifies you when a good deal is found.

## Features
- 📌 **Easy-to-use GUI**: Add flights manually or set criteria for automatic tracking.
- ✈ **Automated Web Scraping**: Uses Selenium to fetch flight prices from Google Flights.
- 📉 **Email Alerts**: Get notified when the price drops below your specified maximum.
- 🕒 **Daily Price Check**: Runs every day at 8:00 AM automatically.
- 🗄 **CSV Storage**: Keeps track of all flight entries in a local CSV file.
- 🔎 **Flexible Search Options**: Search by specific flights or broad criteria (airline, connections, price).

## Installation
### Prerequisites
Ensure you have Python installed on your machine. Then install the required dependencies:
```bash
pip install selenium beautifulsoup4 requests schedule smtplib pandas
```
You'll also need **ChromeDriver** for Selenium. Download it from [here](https://sites.google.com/chromium.org/driver/) and place it in your system PATH.

## How to Use
1. **Run the application**:
   ```bash
   python flightwatch.py
   ```
2. **Enter flight details or search criteria**:
   - Origin (e.g., ATL for Atlanta)
   - Destination (e.g., LAX for Los Angeles)
   - Date (format: YYYY-MM-DD)
   - Maximum price you're willing to pay
   - Preferred Airline (optional)
   - Allow Connections? (Yes/No)
   - Email to receive alerts
3. **Click "Add Flight"**: Saves flight details to `flights.csv`.
4. **Click "Start Tracking"**: Begins automatic price checks.
5. If the flight price drops below your max price, you’ll receive an email alert!

## Email Configuration
FlightWatch uses Gmail to send alerts. To use it:
- Enable **Less Secure Apps** or generate an **App Password** for your Gmail account.
- Replace `your_email@gmail.com` and `your_email_password` in the script with your credentials.

## Future Enhancements
🚀 Web-based UI (Flask) for remote tracking
🚀 Multi-source price checking (Expedia, Skyscanner)
🚀 Push notifications instead of emails
🚀 AI-based deal prediction

