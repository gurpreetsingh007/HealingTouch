# 🔗 Connect Squarespace Domain to Netlify

## You Already Have a Domain from Squarespace - Great!

This guide will help you connect your existing Squarespace domain to your new Healing Hands website hosted on Netlify (FREE).

---

## 📋 What You Need

- ✅ Your Squarespace domain name (e.g., healinghands.com)
- ✅ Access to your Squarespace account
- ✅ Your website deployed to Netlify (we'll do this first)

**Important:** You do NOT need to pay for Squarespace hosting. You're only using the domain name from them.

---

## 🎯 Two Options for You

### **Option 1: Keep Domain at Squarespace** ⭐ RECOMMENDED
- Keep domain registered with Squarespace
- Point it to Netlify (change DNS settings)
- Easier - no transfer needed
- Takes 30 minutes

### **Option 2: Transfer Domain to Another Provider**
- Move domain away from Squarespace
- More control, possibly cheaper renewal
- Takes 5-7 days
- More complex process

**I recommend Option 1** - it's faster and simpler!

---

## 🚀 STEP-BY-STEP: Connect Squarespace Domain to Netlify

### **STEP 1: Deploy Your Website to Netlify First**

Before connecting your domain, let's get your website live on Netlify:

1. **Go to Netlify.com**
   - Sign up with: gskohaar@gmail.com

2. **Deploy your site**
   - Click "Add new site" > "Deploy manually"
   - Drag and drop your `healing-hands-website` folder
   - Wait 30 seconds - your site is live!

3. **Get your Netlify URL**
   - You'll get something like: `amazing-site-123456.netlify.app`
   - Change it to: `healing-hands.netlify.app`
   - (Go to Site settings > Change site name)

4. **Test it works**
   - Visit your Netlify URL
   - Make sure website looks good
   - Test contact form

✅ **Your website is now live on Netlify!** Now let's connect your Squarespace domain...

---

### **STEP 2: Add Custom Domain in Netlify**

1. **In your Netlify dashboard:**
   - Go to **"Domain settings"**
   - Click **"Add custom domain"**

2. **Enter your Squarespace domain:**
   - Type: `yourdomain.com` (your actual Squarespace domain)
   - Click **"Verify"**

3. **Netlify will show DNS records:**
   - You'll see instructions with specific DNS settings
   - **Keep this page open** - you'll need these values!

**You should see something like:**
```
Add these DNS records:

A Record:
Name: @
Value: 75.2.60.5

CNAME Record:
Name: www
Value: your-site-name.netlify.app
```

---

### **STEP 3: Update DNS Settings in Squarespace**

Now let's point your Squarespace domain to Netlify:

1. **Log into Squarespace**
   - Go to: https://login.squarespace.com/

2. **Navigate to Domains**
   - Click **Settings** (gear icon)
   - Click **Domains**
   - Click on your domain name

3. **Go to DNS Settings**
   - Look for **"DNS Settings"** or **"Advanced Settings"**
   - Click **"Manage"** or **"Edit"**

4. **Update A Record:**
   - Find the **A Record** pointing to Squarespace
   - **Change it** to point to Netlify:
   ```
   Type: A
   Host: @
   Points to: 75.2.60.5
   TTL: 3600 (or auto)
   ```

5. **Update CNAME Record:**
   - Find the **CNAME Record** for `www`
   - **Change it** to:
   ```
   Type: CNAME
   Host: www
   Points to: your-site-name.netlify.app
   TTL: 3600 (or auto)
   ```

6. **Remove conflicting records:**
   - If you see other A or CNAME records pointing to Squarespace
   - Delete them (but keep MX records if you have email!)

7. **Save changes**
   - Click **"Save"** or **"Apply"**

---

### **STEP 4: Wait for DNS Propagation**

**Timeline:**
- Minimum: 5-30 minutes
- Typical: 1-2 hours
- Maximum: 24-48 hours (rare)

**Check propagation status:**
- Go to: https://www.whatsmydns.net/
- Enter your domain
- Select "A" record type
- You should see `75.2.60.5` around the world

**What to expect:**
- First few minutes: Old site (Squarespace) still shows
- After propagation: New site (Netlify) appears!
- SSL certificate: Netlify auto-installs (takes extra 10-15 min)

---

### **STEP 5: Enable SSL Certificate (HTTPS)**

After DNS is updated (and you can see your site on your domain):

1. **In Netlify dashboard:**
   - Go to **Domain settings**
   - Find your domain
   - Click **"Verify DNS configuration"**

2. **Provision SSL:**
   - Click **"Provision certificate"** (if needed)
   - Wait 5-10 minutes
   - SSL will be automatically installed!

3. **Test HTTPS:**
   - Go to: `https://yourdomain.com`
   - You should see a green lock 🔒 in the browser
   - Your site is now secure!

---

## 🔍 Finding Your DNS Settings in Squarespace

Squarespace interface has changed over time. Here are different ways to find DNS settings:

### **Method 1: Settings Menu**
1. Home Menu → Settings → Domains
2. Click your domain
3. Click "DNS Settings" or "Advanced Settings"

### **Method 2: Domain Panel**
1. Home Menu → Domains
2. Click your domain name
3. Scroll down to "Advanced Settings"
4. Click "DNS Settings"

### **Method 3: If Using External DNS**
- If your domain is registered with Squarespace but DNS is managed elsewhere
- You may need to update DNS at the external provider
- Check your domain's nameservers

**Can't find it?** Look for:
- "Manage DNS"
- "DNS Records"
- "Advanced DNS"
- "Custom Records"

---

## ⚠️ Important: Don't Delete Email Records!

**If you use email with your domain:**

When updating DNS records, **DO NOT DELETE**:
- **MX Records** (mail exchange - for email)
- **TXT Records** (email verification)
- **SPF/DKIM records** (email security)

**Only update:**
- A Records (website)
- CNAME Records (www subdomain)

**Example of what to KEEP:**
```
Type: MX
Host: @
Points to: mail.squarespace.com
Priority: 10

Type: TXT
Host: @
Value: "v=spf1 include:_spf.squarespace.com ~all"
```

---

## 💰 Cost Breakdown

**What you're paying:**
- Squarespace domain renewal: ~$20/year (varies by domain)
- Netlify hosting: **$0/year (FREE forever)**
- SSL certificate: **$0/year (FREE from Netlify)**

**What you're NOT paying:**
- Squarespace website plan: $16-49/month ❌ NOT NEEDED!
- You're ONLY using the domain from Squarespace

**Annual savings:** $192-588/year by hosting on Netlify instead! 💰

---

## 🎯 Alternative: Cancel Squarespace Completely

If you don't need Squarespace for anything else:

### **Option A: Keep Domain at Squarespace (Easiest)**
- Cancel Squarespace website subscription
- Keep the domain-only service (~$20/year)
- Point domain to Netlify (as described above)

### **Option B: Transfer Domain Away from Squarespace**

**Where to transfer:**
- Namecheap ($12/year - cheaper!)
- Google Domains ($12/year)
- Porkbun ($10/year - cheapest)

**Transfer process:**
1. Unlock domain in Squarespace
2. Get transfer authorization code
3. Initiate transfer at new registrar
4. Wait 5-7 days for transfer
5. Update DNS at new registrar

**Saves:** $8-10/year on domain renewal

---

## ✅ Complete Setup Checklist

### Before You Start:
- [ ] Have Squarespace login credentials
- [ ] Know your domain name
- [ ] Website ready to deploy

### Deploy to Netlify:
- [ ] Sign up for Netlify account
- [ ] Deploy website to Netlify
- [ ] Change site name to something memorable
- [ ] Test Netlify URL works

### Connect Domain:
- [ ] Add custom domain in Netlify
- [ ] Copy DNS records from Netlify
- [ ] Log into Squarespace
- [ ] Update A record in Squarespace DNS
- [ ] Update CNAME record in Squarespace DNS
- [ ] Save DNS changes
- [ ] Wait for propagation (30 min - 2 hours)

### Verify & Test:
- [ ] Check DNS propagation (whatsmydns.net)
- [ ] Visit your domain - see new site?
- [ ] Enable SSL in Netlify
- [ ] Test HTTPS works (green lock)
- [ ] Test contact form
- [ ] Check on mobile device

### Update Website:
- [ ] Update Formspree return URL to your domain
- [ ] Update Google Business Profile
- [ ] Update social media links
- [ ] Inform clients of new website

---

## 🆘 Troubleshooting

### "I can't find DNS settings in Squarespace"
1. Check if domain is actually registered with Squarespace
2. Look under: Domains → [Your Domain] → Advanced Settings
3. If managed externally, DNS is at the external provider
4. Contact Squarespace support - they can guide you

### "My domain still shows the old Squarespace site"
1. Wait longer - DNS can take up to 24 hours
2. Clear browser cache (Ctrl+Shift+Delete)
3. Try incognito/private browsing
4. Check DNS propagation on whatsmydns.net
5. Verify DNS records are correct in Squarespace

### "I see 'SSL certificate error'"
1. This is normal immediately after DNS updates
2. Wait 15-30 minutes after domain starts working
3. In Netlify: Domain settings → Verify DNS → Provision certificate
4. Don't visit site for 15 minutes (let SSL provision)
5. Clear browser cache and try again

### "Website works but www.domain.com doesn't"
1. Check CNAME record for www is correct
2. In Netlify: Add domain alias for www.yourdomain.com
3. Wait for DNS to propagate
4. Enable SSL for both versions

### "Email stopped working after DNS change"
1. You deleted MX records (email records)
2. In Squarespace DNS: Re-add MX records
3. Contact Squarespace support for correct email DNS records
4. Or set up new email (Google Workspace, etc.)

---

## 📧 What About Email?

**If you have email@yourdomain.com through Squarespace:**

**Option 1: Keep Squarespace Email**
- Keep MX records pointing to Squarespace
- Continue using Squarespace email
- No changes needed!

**Option 2: Switch to Google Workspace**
- More professional and reliable
- $6/month per email
- Update MX records to Google
- Get Gmail interface with your domain

**Option 3: Use Email Forwarding**
- Forward yourdomain@.com → gskohaar@gmail.com
- Free with most domain registrars
- Simple but less professional for replies

---

## 🎓 Quick Reference: DNS Records for Netlify

**What you need to add/change in Squarespace DNS:**

```
A Record:
Type: A
Name: @ (or blank)
Value: 75.2.60.5
TTL: 3600

CNAME Record:
Type: CNAME
Name: www
Value: your-site-name.netlify.app
TTL: 3600
```

**Replace `your-site-name` with your actual Netlify subdomain!**

---

## 💡 Pro Tips

1. **Take screenshots** of current DNS settings before changing
2. **Make changes during off-hours** (less traffic if something goes wrong)
3. **Test on multiple devices** after going live
4. **Keep Netlify URL** as backup (healing-hands.netlify.app)
5. **Set calendar reminder** for domain renewal (don't let it expire!)

---

## 🚀 Next Steps

**Right now:**
1. Tell me your Squarespace domain name
2. Let's deploy your site to Netlify together
3. Then we'll connect your domain!

**What's your domain name?** I'll help you get it connected! 🌿

---

## 📱 After Your Domain is Connected

### Update these:
✅ Formspree return URL in contact form  
✅ Google Business Profile  
✅ Social media profiles (Instagram, Facebook, etc.)  
✅ Business cards and marketing materials  
✅ Email signatures  

### Start marketing:
✅ Submit to Google Search Console  
✅ Announce new website on social media  
✅ Email existing clients  
✅ Create Google Business Profile (if not done)  
✅ Get initial reviews  

---

🌿 **Healing Hands - Your Domain, Your Free Website, Your Success!**

**Ready to connect your Squarespace domain?** Let's do it! What's your domain name?
