# FormSubmit.co Setup Guide

## ✅ Contact Form is Now Functional!

Your contact form is now integrated with **FormSubmit.co**, a free service that handles form submissions without requiring a backend server.

## 🚀 How It Works

1. When a visitor fills out the contact form and clicks "Send Message"
2. The form data is sent to FormSubmit.co
3. FormSubmit.co forwards the message to your email
4. The visitor sees a success page

## ⚙️ Initial Setup (Required)

### Step 1: Verify Your Email

**IMPORTANT:** The first time someone submits the form, FormSubmit.co will send a **verification email** to `contact@catelinlefranc.com`.

1. Check the inbox for `contact@catelinlefranc.com`
2. Look for an email from FormSubmit.co
3. Click the verification link in the email
4. After verification, all future submissions will work automatically

### Step 2: Update Email Address

In `index.html`, find this line (around line 252):

```html
<form class="contact-form" id="contactForm" action="https://formsubmit.co/contact@catelinlefranc.com" method="POST">
```

Replace `contact@catelinlefranc.com` with your actual email address:

```html
<form class="contact-form" id="contactForm" action="https://formsubmit.co/YOUR-EMAIL@example.com" method="POST">
```

## 📧 What Happens When Someone Submits

1. Visitor fills out the form with:
   - Their name
   - Their email
   - Their message

2. FormSubmit.co sends you an email with:
   - Subject: "New contact from Portfolio Website"
   - All the form data in a nice table format
   - The visitor's email (so you can reply directly)

3. The visitor is redirected to FormSubmit's default thank you page

## 🎨 Features Already Configured

Your form includes these FormSubmit.co features:

### Hidden Fields Already Added:
- **`_subject`**: Custom email subject line
- **`_captcha: false`**: Disables reCAPTCHA (can enable if you get spam)
- **`_template: table`**: Formats the email nicely
- **`_honey`**: Honeypot field for spam protection

## 🔧 Advanced Customization (Optional)

### Add a Custom Thank You Page

Instead of FormSubmit's default page, redirect to your own:

```html
<input type="hidden" name="_next" value="https://yourdomain.com/thank-you.html">
```

### Enable reCAPTCHA (if you get spam)

Change this line in `index.html`:
```html
<input type="hidden" name="_captcha" value="true">
```

### Add CC (Carbon Copy)

Send a copy to another email:
```html
<input type="hidden" name="_cc" value="another-email@example.com">
```

### Custom Reply-To Email

Set a different reply-to address:
```html
<input type="hidden" name="_replyto" value="your-reply-email@example.com">
```

### Auto-Response to Visitor

Send an automatic reply to the person who submitted:
```html
<input type="hidden" name="_autoresponse" value="Thank you for contacting me! I'll get back to you soon.">
```

## 🎯 Complete Example with All Options

```html
<form class="contact-form" id="contactForm" action="https://formsubmit.co/YOUR-EMAIL@example.com" method="POST">
    <!-- Basic Configuration -->
    <input type="hidden" name="_subject" value="New contact from Portfolio Website">
    <input type="hidden" name="_template" value="table">
    
    <!-- Spam Protection -->
    <input type="hidden" name="_captcha" value="false">
    <input type="text" name="_honey" style="display:none">
    
    <!-- Advanced Options -->
    <input type="hidden" name="_next" value="https://yourdomain.com/thank-you.html">
    <input type="hidden" name="_cc" value="backup@example.com">
    <input type="hidden" name="_autoresponse" value="Thank you for contacting me!">
    
    <!-- Form Fields -->
    <div class="form-group">
        <input type="text" name="name" placeholder="Your Name" required>
    </div>
    <div class="form-group">
        <input type="email" name="email" placeholder="Your Email" required>
    </div>
    <div class="form-group">
        <textarea name="message" rows="5" placeholder="Your Message" required></textarea>
    </div>
    <button type="submit" class="btn btn-primary">Send Message</button>
</form>
```

## 🛡️ Security Features

✅ **Honeypot Field**: Catches spam bots (hidden `_honey` field)  
✅ **Server-Side Processing**: FormSubmit.co handles validation  
✅ **No Email Exposure**: Your email isn't visible in the source code after first submission  
✅ **Optional reCAPTCHA**: Can be enabled if needed  

## 📱 Testing Your Form

### Before Deploying:

1. **Update the email** in `index.html` to your real email
2. **Deploy to GitHub Pages** (form won't work locally)
3. **Submit a test message** from your live site
4. **Check your email** for the verification link
5. **Click the verification link**
6. **Submit another test** to confirm it works

### Test Checklist:

- [ ] Email address updated in HTML
- [ ] Site deployed to GitHub Pages
- [ ] Test form submission sent
- [ ] Verification email received
- [ ] Verification link clicked
- [ ] Second test submission received in inbox
- [ ] Email format looks good
- [ ] Reply-to address works

## 🐛 Troubleshooting

### Not Receiving Emails?

1. **Check spam folder** - FormSubmit emails might go to spam initially
2. **Verify your email** - Make sure you clicked the verification link
3. **Check the email address** - Ensure no typos in the form action
4. **Wait a few minutes** - Sometimes there's a delay

### Form Not Submitting?

1. **Check if deployed** - Form won't work when opening HTML locally
2. **Check browser console** - Look for JavaScript errors (F12)
3. **Verify form action** - Make sure the URL is correct
4. **Check required fields** - All fields must be filled

### Getting Spam?

1. Enable reCAPTCHA: `<input type="hidden" name="_captcha" value="true">`
2. The honeypot field is already active

## 🌟 Benefits of FormSubmit.co

✅ **Completely Free** - No payment required  
✅ **No Registration** - No account needed  
✅ **Simple Setup** - Just one email verification  
✅ **Reliable** - Handles thousands of submissions daily  
✅ **No Backend Required** - Perfect for static GitHub Pages  
✅ **Customizable** - Many configuration options  

## 📚 Additional Resources

- **FormSubmit.co Docs**: https://formsubmit.co
- **GitHub Pages Guide**: See `DEPLOYMENT.md`
- **Form Testing**: Use a temporary email to test

## 🎉 You're All Set!

Your contact form is now fully functional and will:
1. Accept visitor messages
2. Send them to your email
3. Protect against spam
4. Work perfectly on GitHub Pages

Just remember to **verify your email** after the first submission! 🚀
