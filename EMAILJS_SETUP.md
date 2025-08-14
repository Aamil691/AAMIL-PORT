# EmailJS Setup Guide for Contact Form

## Overview
This guide will help you set up EmailJS so that when someone submits a message through your contact form, you receive an email notification at `aamilrais34@gmail.com`.

## Step 1: Create EmailJS Account
1. Go to [EmailJS.com](https://www.emailjs.com/) and sign up for a free account
2. Verify your email address

## Step 2: Set Up Email Service
1. In your EmailJS dashboard, go to "Email Services"
2. Click "Add New Service"
3. Choose "Gmail" (or your preferred email provider)
4. Connect your Gmail account (aamilrais34@gmail.com)
5. Note down the **Service ID** (you'll need this later)

## Step 3: Create Email Template
1. Go to "Email Templates" in your dashboard
2. Click "Create New Template"
3. Use this template content:

**Subject:**
```
New Message from {{from_name}} - {{subject}}
```

**Email Body:**
```
Hello Aamil,

You have received a new message from your portfolio website:

**Name:** {{from_name}}
**Email:** {{from_email}}
**Subject:** {{subject}}

**Message:**
{{message}}

---
This message was sent from your portfolio contact form.
```

4. Save the template and note down the **Template ID**

## Step 4: Get Your Public Key
1. Go to "Account" → "API Keys" in your dashboard
2. Copy your **Public Key**

## Step 5: Update Your Code
Replace the placeholder values in `script.js`:

```javascript
// Replace YOUR_EMAILJS_PUBLIC_KEY with your actual public key
emailjs.init("YOUR_EMAILJS_PUBLIC_KEY");

// Replace YOUR_EMAILJS_SERVICE_ID with your service ID
// Replace YOUR_EMAILJS_TEMPLATE_ID with your template ID
emailjs.send('YOUR_EMAILJS_SERVICE_ID', 'YOUR_EMAILJS_TEMPLATE_ID', templateParams)
```

## Step 6: Test Your Setup
1. Open your website
2. Fill out the contact form
3. Submit a test message
4. Check your email (aamilrais34@gmail.com) for the notification

## Important Notes:
- **Free Plan Limits:** EmailJS free plan allows 200 emails per month
- **Security:** Your public key is safe to use in frontend code
- **Gmail:** If using Gmail, you may need to enable "Less secure app access" or use App Passwords
- **Spam Protection:** Consider adding CAPTCHA or rate limiting for production use

## Alternative: Using Formspree
If you prefer a simpler solution, you can also use Formspree:
1. Go to [Formspree.io](https://formspree.io/)
2. Create a new form
3. Replace the form action with your Formspree endpoint
4. No JavaScript changes needed

## Troubleshooting:
- Check browser console for error messages
- Verify all IDs and keys are correct
- Ensure your email service is properly connected
- Check spam folder for test emails

## Support:
- EmailJS Documentation: [docs.emailjs.com](https://docs.emailjs.com/)
- EmailJS Support: [support@emailjs.com](mailto:support@emailjs.com)
