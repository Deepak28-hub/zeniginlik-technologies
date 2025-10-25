# 📧 Email Setup Guide for Zenginlik Technologies Website

## Current Status
The contact form is now configured to send real emails, but you need to set up EmailJS to make it work.

## 🚀 Quick Setup (5 minutes)

### Step 1: Create EmailJS Account
1. Go to [https://www.emailjs.com/](https://www.emailjs.com/)
2. Sign up for a free account
3. Verify your email address

### Step 2: Add Email Service
1. In EmailJS dashboard, go to "Email Services"
2. Click "Add New Service"
3. Choose "Gmail" (or your preferred email provider)
4. Connect your Gmail account
5. Copy the **Service ID** (looks like: `service_xxxxxxx`)

### Step 3: Create Email Template
1. Go to "Email Templates"
2. Click "Create New Template"
3. Use this template:

```
Subject: New Contact Form Submission - Zenginlik Technologies

From: {{from_name}} <{{from_email}}>
Phone: {{phone}}
Service Interest: {{service}}

Message:
{{message}}

---
This message was sent from the Zenginlik Technologies website contact form.
```

4. Save and copy the **Template ID** (looks like: `template_xxxxxxx`)

### Step 4: Get Public Key
1. Go to "Account" → "General"
2. Copy your **Public Key** (looks like: `user_xxxxxxxxxxxxxxxx`)

### Step 5: Update Your Website
Replace these values in `script.js`:

```javascript
// Line 132: Replace YOUR_PUBLIC_KEY
emailjs.init("YOUR_PUBLIC_KEY"); 

// Line 153: Replace YOUR_SERVICE_ID
'YOUR_SERVICE_ID'

// Line 154: Replace YOUR_TEMPLATE_ID  
'YOUR_TEMPLATE_ID'
```

## 📧 Alternative Options

### Option 2: Formspree (Even Easier)
1. Go to [https://formspree.io/](https://formspree.io/)
2. Create account and get form endpoint
3. Replace the form action in HTML:

```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

### Option 3: Netlify Forms (If hosting on Netlify)
1. Add `netlify` attribute to form
2. Add hidden input field
3. No additional setup needed

### Option 4: Backend Solution
- PHP with mail() function
- Node.js with Nodemailer
- Python with SMTP
- Requires server setup

## 🎯 Recommended: EmailJS Setup

**Why EmailJS?**
- ✅ No backend required
- ✅ Works with any email provider
- ✅ Free tier: 200 emails/month
- ✅ Easy to set up
- ✅ Secure and reliable

## 📞 Support
If you need help with setup, the EmailJS documentation is excellent:
- [EmailJS Docs](https://www.emailjs.com/docs/)
- [Quick Start Guide](https://www.emailjs.com/docs/tutorial/overview/)

## 🔧 Current Configuration
The website is ready - you just need to:
1. Set up EmailJS account (5 minutes)
2. Replace 3 values in the code
3. Test the form

**Your contact form will then send real emails to your Gmail!** 📧✅
