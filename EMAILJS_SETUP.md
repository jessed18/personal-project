# EmailJS Setup Instructions

Your contact form is now set up to use EmailJS (free email service). Follow these steps to make it work:

## Step 1: Create EmailJS Account
1. Go to https://www.emailjs.com/
2. Sign up for a free account (allows 200 emails/month)

## Step 2: Create an Email Service
1. In EmailJS dashboard, go to "Email Services"
2. Click "Add New Service"
3. Choose your email provider (Gmail recommended)
4. Follow the setup instructions
5. Copy your **Service ID** (looks like: `service_xxxxxxx`)

## Step 3: Create an Email Template
1. Go to "Email Templates" in dashboard
2. Click "Create New Template"
3. Use this template:
   ```
   From: {{from_name}} ({{from_email}})
   Phone: {{phone}}
   Subject: {{subject}}
   
   Message:
   {{message}}
   ```
4. Set "To Email" to your email address
5. Copy your **Template ID** (looks like: `template_xxxxxxx`)

## Step 4: Get Your Public Key
1. Go to "Account" → "General"
2. Copy your **Public Key** (looks like: `xxxxxxxxxxxxx`)

## Step 5: Update the Code
Open `index.html` and replace these three values:

1. Line ~421: Replace `YOUR_PUBLIC_KEY` with your Public Key
2. Line ~456: Replace `YOUR_SERVICE_ID` with your Service ID
3. Line ~457: Replace `YOUR_TEMPLATE_ID` with your Template ID
4. Line ~465: Replace `your-email@example.com` with your actual email

## Alternative: Use Formspree (Even Easier)
If you prefer, you can use Formspree instead:
1. Go to https://formspree.io/
2. Sign up and create a form
3. Get your form endpoint (looks like: `https://formspree.io/f/xxxxxxx`)
4. Replace the form action in `index.html` line ~381 with your Formspree endpoint

## Testing
After setup, test the form by sending yourself a message. You should receive an email within seconds!

