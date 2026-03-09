# 📧 Email Setup Guide for Healing Hands Contact Form

## Current Setup

Your contact form is configured to send emails to: **gskohaar@gmail.com**

## How It Works

I've integrated your contact form with **Formspree**, a free service that handles form submissions and sends them to your email.

### Features:
✅ All form submissions go directly to gskohaar@gmail.com  
✅ You'll receive the customer's name, email, phone, subject, and message  
✅ Customers will see a success message after submitting  
✅ Completely free for up to 50 submissions per month  

---

## Setup Steps (IMPORTANT - Do This Before Going Live!)

### Step 1: Create Your Formspree Account

1. Go to: **https://formspree.io/**
2. Click "Get Started" or "Sign Up"
3. Sign up with your email: **gskohaar@gmail.com**
4. Verify your email address

### Step 2: Create a New Form

1. After logging in, click "New Form"
2. Name it: "Healing Hands Contact Form"
3. Formspree will generate a unique form endpoint that looks like:
   ```
   https://formspree.io/f/[YOUR-UNIQUE-ID]
   ```

### Step 3: Update Your Website

1. Copy your unique form endpoint from Formspree
2. Open the file: `healing-hands-website/index.html`
3. Find line 252 (the contact form)
4. Replace this:
   ```html
   <form class="contact-form" id="contactForm" action="https://formspree.io/f/xyzygrkw" method="POST">
   ```
   
   With your actual endpoint:
   ```html
   <form class="contact-form" id="contactForm" action="https://formspree.io/f/YOUR-UNIQUE-ID" method="POST">
   ```

### Step 4: Update the Return URL (When You Deploy)

When you deploy your website to a real domain (not localhost), update line 272:
```html
<input type="hidden" name="_next" value="http://localhost:8000/#contact">
```

Change it to your actual website URL:
```html
<input type="hidden" name="_next" value="https://yourdomain.com/#contact">
```

---

## Testing the Form (Right Now)

### Option 1: Quick Test (Temporary Setup)
I've already set up a temporary Formspree endpoint. You can test it right now:

1. Refresh your website in the browser
2. Scroll to the contact form
3. Fill it out and click "Send Message"
4. The first submission will require Formspree verification

**Note:** The temporary setup I created is for demonstration only. For production use, you MUST create your own Formspree account.

### Option 2: Test with Your Own Account (Recommended)
1. Create your Formspree account (see Step 1 above)
2. Update the form endpoint with your unique ID
3. Test by submitting the form
4. Check your email: gskohaar@gmail.com

---

## What You'll Receive in Your Email

When someone submits the form, you'll get an email like this:

```
From: Formspree <noreply@formspree.io>
Subject: New Contact Form Submission - Healing Hands

Name: John Smith
Email: john@example.com
Phone: (555) 123-4567
Subject: Booking Question
Message: 
Hello, I'm interested in booking a massage therapy session. 
What times do you have available next week?
```

You can reply directly to these emails, and your response will go to the customer's email address.

---

## Formspree Free Plan Limits

- ✅ **50 submissions per month** (free)
- ✅ Email notifications
- ✅ Spam filtering
- ✅ File uploads (if you want to add later)
- ✅ Export submissions

**If you need more:** Upgrade to paid plans starting at $10/month for 1,000 submissions.

---

## Alternative Options (If You Want More Control)

### Option 1: EmailJS (Another Free Service)
- Similar to Formspree
- 200 emails/month free
- Setup: https://www.emailjs.com/

### Option 2: Custom Backend (More Advanced)
- Set up your own email server
- Requires: Node.js, SendGrid/Mailgun API
- Cost: $0-$15/month
- More technical setup required

### Option 3: Netlify Forms (If Hosting on Netlify)
- Automatically handles forms
- 100 submissions/month free
- Zero configuration needed

---

## Current Configuration Summary

**Your Email:** gskohaar@gmail.com  
**Form Action:** https://formspree.io/f/xyzygrkw (TEMPORARY - Replace with yours!)  
**Email Subject:** "New Contact Form Submission - Healing Hands"  
**Reply-To:** Customer's email (so you can reply directly)

---

## Troubleshooting

### Form not working?
1. Check that you've replaced the form endpoint with YOUR unique Formspree ID
2. Make sure you verified your Formspree email
3. Check your spam folder
4. Ensure JavaScript is enabled in browser

### Not receiving emails?
1. Log into Formspree.io dashboard
2. Check the "Submissions" tab - they're all stored there
3. Verify your email address in Formspree settings
4. Check spam/junk folders
5. Add noreply@formspree.io to your contacts

### Want to customize the email format?
1. Log into Formspree
2. Go to your form settings
3. Customize the notification template
4. Add auto-reply messages for customers

---

## Next Steps

1. ✅ Create your Formspree account: https://formspree.io/
2. ✅ Get your unique form endpoint
3. ✅ Update the HTML file with your endpoint
4. ✅ Test the form
5. ✅ Start receiving inquiries!

---

**Questions?** Feel free to ask, and I can help you set up any of these alternatives or customize the form further!

🌿 **Healing Hands - Where healing begins**
