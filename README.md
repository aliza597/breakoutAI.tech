Custom-Email-Sender
This project is a custom email-sending application that enables users to send personalized emails using data from a Google Sheet or CSV file. Key features include email scheduling, throttling, tracking, and real-time analytics.

Features
Import Email Data: Import email data from Google Sheets or CSV files.
Customizable Email Content: Personalize email content using dynamic fields (e.g., recipient names, company names).
Email Scheduling: Schedule emails for immediate sending or future delivery.
Throttling: Control the rate at which emails are sent to avoid spam filters.
Tracking: Track delivery statuses and interactions via SendGrid.
Real-Time Analytics: Monitor sent emails, delivery statuses (Sent, Delivered, Opened, Bounced), and errors through a dashboard.
Technologies Used
Backend: Flask (Python Web Framework)
Task Queue: Celery (with Redis as the broker for asynchronous task processing)
Database: SQLAlchemy (for relational database management)
Email Service: SendGrid (for email sending and tracking)
Frontend: HTML, CSS (for the real-time dashboard interface)
Others: Redis (for Celery task queue)
Prerequisites
Python 3.7+
Redis (for Celery)
SendGrid account (for email sending and tracking)
Installation
Clone the repository:

bash

git clone https://github.com/your-username/Custom-Email-Sender.git
cd Custom-Email-Sender
Create and activate a virtual environment:

bash

python3 -m venv venv
source venv/bin/activate  # On Windows, use venv\Scripts\activate
Install dependencies:

bash

pip install -r requirements.txt
Set up Redis (required for Celery):

Install Redis and start the server locally, or use a hosted Redis service.
Configuration
Create a .env file in the project root and add the following environment variables:

makefile

SECRET_KEY=your-secret-key
GOOGLE_SHEET_ID=your-google-sheet-id
SENDGRID_API_KEY=your-sendgrid-api-key
DATABASE_URL=sqlite:///emails.db  # Use a production-ready database like PostgreSQL for deployment
REDIS_URL=redis