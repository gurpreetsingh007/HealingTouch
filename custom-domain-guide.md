# 🌐 Custom Domain Setup Guide for Healing Hands

## Your Goal: `healinghands.com` or `healinghandswellness.com`

---

## 📋 Quick Overview

**Total Cost:** ~$10-15/year (one-time annual payment)  
**Time to Setup:** 15-30 minutes  
**Free Hosting:** Yes (Netlify remains FREE)  
**Professional Email:** Optional (add $6/month for hello@healinghands.com)

---

## 🎯 STEP 1: Check Domain Availability

Let me check which domains are available for "Healing Hands":

### Top Recommendations:

**Option 1: healinghands.com** ⭐ BEST
- Most professional
- Easy to remember
- Short and clean
- Cost: ~$12/year

**Option 2: healinghandswellness.com**
- More descriptive
- Great for SEO
- Cost: ~$12/year

**Option 3: healinghands.co**
- Modern alternative
- Shorter than .com
- Cost: ~$10/year

**Option 4: myhealinghands.com**
- If healinghands.com is taken
- Personal touch
- Cost: ~$12/year

**Option 5: healinghandsmassage.com**
- Service-specific
- Good for local SEO
- Cost: ~$12/year

### Check Availability Now:

1. Go to: **https://www.namecheap.com/domains/registration/results/**
2. Type: `healinghands.com`
3. See if it's available (green checkmark = available!)

---

## 💰 STEP 2: Where to Buy Your Domain (Cheapest & Best)

### 🏆 RECOMMENDED: Namecheap

**Why Namecheap?**
- ✅ **Cheapest prices** ($8.98-$12.98/year for .com)
- ✅ **Free WHOIS privacy** (hides your personal info)
- ✅ **Easy to use** interface
- ✅ **Excellent support**
- ✅ **No hidden fees**
- ✅ **Easy DNS management**

**Prices:**
- `.com` = $12.98/year (first year often discounted to $5.98!)
- `.co` = $9.98/year
- `.net` = $13.98/year

**Link:** https://www.namecheap.com/

---

### Alternative: Porkbun (Slightly Cheaper)

**Prices:**
- `.com` = $10.73/year
- `.co` = $9.46/year

**Link:** https://porkbun.com/

---

### Alternative: Google Domains

**Prices:**
- `.com` = $12/year (no discount)
- Simple interface
- Google integration

**Link:** https://domains.google/

---

## 🛒 STEP 3: Buy Your Domain (Namecheap Example)

### Purchase Process:

1. **Go to Namecheap.com**

2. **Search for your domain:**
   - Enter: `healinghands.com`
   - Click "Search"

3. **Add to cart:**
   - Click "Add to Cart" next to your desired domain
   - **IMPORTANT:** Select **1 year** (not auto-renew unless you want)

4. **Review cart:**
   - Make sure "WhoisGuard" is included (FREE - keeps your info private)
   - Remove any upsells you don't need

5. **Create account:**
   - Sign up with: `gskohaar@gmail.com`
   - Create password
   - Enter payment info

6. **Complete purchase**
   - Cost: ~$12.98 (sometimes discounted to $5.98 first year!)

7. **Confirmation email**
   - Check gskohaar@gmail.com
   - You'll receive domain confirmation

---

## 🔗 STEP 4: Connect Domain to Netlify

### After You Deploy to Netlify:

1. **Deploy your website to Netlify first** (following the deployment guide)
   - Your site will be at: `https://healing-hands.netlify.app`

2. **In Netlify Dashboard:**
   - Go to **"Domain settings"**
   - Click **"Add custom domain"**
   - Enter: `healinghands.com`
   - Click **"Verify"**

3. **Netlify will show DNS instructions:**
   - Copy the DNS records Netlify provides
   - You'll need these for the next step

4. **In Namecheap Dashboard:**
   - Log into Namecheap
   - Go to **"Domain List"**
   - Click **"Manage"** next to healinghands.com
   - Go to **"Advanced DNS"** tab

5. **Add DNS Records:**
   
   **Add these records exactly:**
   
   **Record 1: A Record**
   ```
   Type: A Record
   Host: @
   Value: 75.2.60.5
   TTL: Automatic
   ```
   
   **Record 2: CNAME Record**
   ```
   Type: CNAME Record
   Host: www
   Value: healing-hands.netlify.app
   TTL: Automatic
   ```

6. **Wait for DNS propagation:**
   - Usually takes 5-30 minutes
   - Can take up to 24 hours (rare)
   - Check status: https://www.whatsmydns.net/

7. **SSL Certificate (HTTPS):**
   - Netlify automatically installs FREE SSL
   - Wait a few minutes after DNS updates
   - Your site will have `https://` automatically!

8. **Test your domain:**
   - Go to: `https://healinghands.com`
   - Should show your website!
   - Also test: `https://www.healinghands.com`

---

## 📧 BONUS: Professional Email (Optional)

Instead of using `gskohaar@gmail.com`, you can have:
- **hello@healinghands.com**
- **info@healinghands.com**
- **gurpreet@healinghands.com**

### Option 1: Google Workspace (BEST)

**Cost:** $6/month per email address  
**Includes:**
- Professional email with your domain
- Gmail interface
- 30GB storage
- Calendar, Drive, Meet included
- Professional and reliable

**Setup:**
1. Go to: https://workspace.google.com/
2. Start free 14-day trial
3. Enter your domain: healinghands.com
4. Follow verification steps
5. Create email: hello@healinghands.com

---

### Option 2: Namecheap Email (Cheaper)

**Cost:** $1.18/month ($14.16/year)  
**Includes:**
- Professional email
- 3GB storage
- Webmail access

**Setup:**
1. In Namecheap dashboard
2. Go to domain > Email
3. Add "Private Email"
4. Create: hello@healinghands.com

---

### Option 3: FREE Email Forwarding (Temporary Solution)

**Cost:** FREE  
**How it works:**
- Forward hello@healinghands.com → gskohaar@gmail.com
- You receive emails at Gmail
- Reply shows from Gmail (not professional)

**Setup in Namecheap:**
1. Domain dashboard > Email Forwarding
2. Add forward: hello@healinghands.com → gskohaar@gmail.com
3. Free but not as professional

---

## 💡 STEP 5: Update Your Website

After connecting your domain, update these places:

### 1. Formspree Return URL

In `index.html`, line 272:
```html
<input type="hidden" name="_next" value="https://healinghands.com/#contact">
```

### 2. Social Media Links

Update all your social profiles with:
- Website: `https://healinghands.com`

### 3. Business Cards & Marketing

Use your new domain on:
- Business cards
- Brochures
- Google Business Profile
- Email signatures

---

## 📊 Cost Breakdown

### Basic Setup (Recommended):
- **Domain**: $12/year (healinghands.com)
- **Hosting**: $0/year (Netlify - FREE forever)
- **SSL Certificate**: $0/year (Netlify - FREE)
- **TOTAL**: **$12/year = $1/month** 🎉

### With Professional Email:
- **Domain**: $12/year
- **Hosting**: $0/year (Netlify - FREE)
- **SSL**: $0/year (FREE)
- **Email**: $72/year (Google Workspace)
- **TOTAL**: **$84/year = $7/month**

### Compared to Traditional Hosting:
- **Traditional hosting**: $120-240/year
- **Your setup**: $12-84/year
- **You save**: $100+/year! 💰

---

## ✅ Complete Domain Setup Checklist

### Before You Start:
- [ ] Deploy website to Netlify first
- [ ] Have your Netlify URL ready
- [ ] Have payment method ready ($12)

### Domain Purchase:
- [ ] Check domain availability
- [ ] Create Namecheap account
- [ ] Purchase domain (with WhoisGuard)
- [ ] Verify email confirmation

### DNS Configuration:
- [ ] Add custom domain in Netlify
- [ ] Copy DNS records from Netlify
- [ ] Add A record in Namecheap
- [ ] Add CNAME record in Namecheap
- [ ] Wait for DNS propagation (5-30 min)

### Testing:
- [ ] Test: healinghands.com
- [ ] Test: www.healinghands.com
- [ ] Verify HTTPS works (green lock icon)
- [ ] Test contact form
- [ ] Check mobile version

### Updates:
- [ ] Update Formspree return URL
- [ ] Update Google Business Profile
- [ ] Update social media links
- [ ] Print new business cards

---

## 🆘 Troubleshooting

### "Domain not working after 30 minutes"
1. Check DNS records in Namecheap (exactly as shown)
2. Disable any proxy/CDN services
3. Wait up to 24 hours for full propagation
4. Use https://www.whatsmydns.net/ to check status

### "SSL certificate not showing"
1. Wait 10-15 minutes after DNS is active
2. In Netlify: Domain settings > "Verify DNS configuration"
3. Click "Provision certificate" if needed
4. Clear browser cache

### "www not working"
1. Make sure CNAME record is added
2. In Netlify: Add "www.healinghands.com" as domain alias
3. Wait for DNS update

### "Emails not working"
1. If using forwarding: Wait 1-2 hours for activation
2. Check spam folder
3. Verify forwarding rules in Namecheap
4. Test with external email (send from Gmail)

---

## 🎯 Quick Start Workflow

**The fastest way to get live:**

1. **Now:** Deploy to Netlify (free subdomain)
   - URL: `healing-hands.netlify.app`
   - Takes 5 minutes
   - Website is LIVE!

2. **Within 24 hours:** Buy custom domain
   - Purchase healinghands.com ($12)
   - Takes 15 minutes

3. **Same day:** Connect domain to Netlify
   - Add DNS records
   - Wait 30 minutes
   - Your domain is LIVE!

4. **Optional - Later:** Add professional email
   - Get hello@healinghands.com
   - Takes 30 minutes
   - Can do anytime

---

## 📱 After Setup - Marketing Your Website

### Immediate Actions:
✅ Add to Google Business Profile  
✅ Share on social media  
✅ Add to email signatures  
✅ Tell existing clients  
✅ Print business cards  

### SEO Setup:
✅ Submit to Google Search Console  
✅ Submit to Bing Webmaster Tools  
✅ Create/update Google Business Profile  
✅ List on local directories  
✅ Get initial reviews from happy clients  

---

## 🌟 Domain Alternatives (If .com is Taken)

If `healinghands.com` is not available:

**Good alternatives:**
- healinghandswellness.com ⭐
- healinghandstherapy.com
- healinghands.co (modern)
- gurpreethealinghands.com
- thehealinghands.com
- healinghandsspa.com
- myhealinghands.com

**Check multiple at once:**
Go to Namecheap and search - it will show all variations!

---

## 💼 Your Final Setup

**Website:** `https://healinghands.com`  
**Email:** `hello@healinghands.com` (optional)  
**Cost:** $12/year for domain + $0 for hosting  
**Maintenance:** Update website anytime via Netlify  
**Professional:** Yes! Looks like a million-dollar business  

---

## 🚀 Ready to Buy Your Domain?

**Step-by-step:**
1. Go to Namecheap.com now
2. Search: `healinghands.com`
3. If available: Buy it! ($12/year)
4. Come back and I'll help you connect it to Netlify!

**Want me to help you check if the domain is available first?** I can help you find the perfect domain name!

🌿 **Healing Hands - Professional Domain, Professional Business**
