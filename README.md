# Stocker - Cloud-Based Stock Trading Platform

A cloud-native stock trading platform built with Flask and AWS services.

## Tech Stack
- **Backend:** Python Flask
- **Database:** AWS DynamoDB
- **Notifications:** AWS SNS
- **Hosting:** AWS EC2
- **Frontend:** HTML, CSS, Bootstrap

## Features
- Secure user authentication (Trader & Admin roles)
- Real-time stock browsing and trading
- Buy and sell stocks with portfolio tracking
- Admin dashboard to monitor traders, transactions, and portfolios
- Email notifications via AWS SNS for login, signup, and transactions

## AWS Services Used
- **EC2** - Hosts the Flask application
- **DynamoDB** - Stores users, stocks, transactions, portfolios
- **SNS** - Sends email notifications

## DynamoDB Tables
- `stocker_users` - User accounts
- `stocker_stocks` - Available stocks
- `stocker_transactions` - Buy/sell transaction records
- `stocker_portfolio` - User portfolio holdings

## Installation & Setup

### 1. Clone the repository
```bash
git clone https://github.com/Shanmukha8/stocker-main.git
cd stocker-main
```

### 2. Create virtual environment
```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Configure AWS
Make sure your EC2 instance has an IAM role with:
- AmazonDynamoDBFullAccess
- AmazonSNSFullAccess

### 5. Run the application
```bash
python3 app.py
```

### 6. Access the app
```
http://YOUR_EC2_PUBLIC_IP:5000
```

## Project Structure
```
stocker-main/
├── app.py                  # Main Flask application
├── setup_dynamodb.py       # DynamoDB table setup script
├── requirements.txt        # Python dependencies
├── templates/              # HTML templates
│   ├── index.html
│   ├── login.html
│   ├── signup.html
│   ├── dashboard_admin.html
│   ├── dashboard_trader.html
│   ├── buy_stock.html
│   ├── sell_stock.html
│   └── service-details-1 to 5.html
└── static/                 # CSS, JS, images
    ├── css/
    ├── js/
    └── vendor/
```

## Usage

### Trader
- Sign up as a Trader
- Browse available stocks
- Buy and sell stocks
- View portfolio and transaction history

### Admin
- Login as Admin
- View all registered traders
- Monitor all transactions
- View all trader portfolios
