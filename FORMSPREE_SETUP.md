# Formspree Setup Guide (Simpler Alternative)

## Overview
Formspree is a simpler alternative to EmailJS that requires no JavaScript configuration. It automatically forwards form submissions to your email.

## Step 1: Create Formspree Account
1. Go to [Formspree.io](https://formspree.io/)
2. Sign up with your email (aamilrais34@gmail.com)
3. Verify your email address

## Step 2: Create a New Form
1. Click "New Form" in your dashboard
2. Give it a name like "Portfolio Contact Form"
3. Copy the form endpoint URL (looks like: `https://formspree.io/f/xaybzwkd`)

## Step 3: Update Your HTML
Replace `YOUR_FORMSPREE_ID` in your `index.html` with your actual form ID:

```html
<form id="contactForm" action="https://formspree.io/f/YOUR_ACTUAL_FORM_ID" method="POST">
```

## Step 4: Test Your Setup
1. Open your website
2. Fill out the contact form
3. Submit a test message
4. Check your email for the notification

## Advantages of Formspree:
- ✅ No JavaScript configuration needed
- ✅ Works immediately after setup
- ✅ Free plan includes 50 submissions per month
- ✅ Automatic spam protection
- ✅ Email notifications
- ✅ Form analytics

## Free Plan Limits:
- 50 form submissions per month
- Basic spam protection
- Email notifications

## That's it! 
Your contact form will now automatically send emails to aamilrais34@gmail.com whenever someone submits a message.

## Support:
- Formspree Documentation: [help.formspree.io](https://help.formspree.io/)
- Formspree Support: [support@formspree.io](mailto:support@formspree.io)
