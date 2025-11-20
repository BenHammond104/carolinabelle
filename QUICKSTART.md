# Quick Start Guide

## Immediate Next Steps

### 1. Add Your Images

Replace the gray placeholder boxes in the Gallery page with actual photos:

**Where to place images:**
- Put all images in `/assets/images/`

**Gallery photos needed:**
- 12+ wedding trolley photos
- Mix of: trolley exterior, bridal parties, interior details, venue shots

### 2. Add Your Logo

Replace the text in the navigation with your logo:

**In all HTML files**, find:
```html
<div class="text-2xl font-serif font-bold text-belle-dark">
    The Carolina Belle Trolley Co.
</div>
```

**Replace with:**
```html
<img src="assets/images/logo.png" alt="The Carolina Belle Trolley Co." class="h-12">
```

### 3. Deploy to Netlify

**Easiest method (Drag & Drop):**

1. Make sure CSS is built:
   ```bash
   npm run build
   ```

2. Go to: https://app.netlify.com/drop

3. Drag your entire `CarolinaBelle` folder onto the page

4. Your site is live!

**Forms will automatically work** once deployed to Netlify.

### 4. Set Up Form Notifications

After deploying:

1. Go to Netlify Dashboard → Your Site
2. Click "Forms" in the sidebar
3. Click "Settings and usage"
4. Add email notifications for `info@carolinabelletrolley.com`

Now you'll get emails when someone books or contacts you!

### 5. Custom Domain (Optional)

In Netlify Dashboard:
1. Go to "Domain settings"
2. Click "Add custom domain"
3. Follow the instructions to connect your domain

---

## Testing Checklist

Before going live, test:

- [ ] All navigation links work
- [ ] Mobile menu opens/closes
- [ ] Booking form submits successfully
- [ ] Contact form submits successfully
- [ ] FAQ accordion expands/collapses
- [ ] Gallery filter buttons work
- [ ] All phone/email links work
- [ ] Site looks good on mobile
- [ ] Replace all placeholder images with real photos
- [ ] Add your logo to navigation
- [ ] Update any remaining ALL-CAPS placeholders
- [ ] Test on multiple browsers

---

## File Overview

### Pages to Update with Images:

1. **index.html** - Hero section, featured photos (6 images)
2. **gallery.html** - Main gallery grid (12+ images)
3. **All pages** - Logo in navigation

### Contact Information:

All pages already have:
- **Email:** info@carolinabelletrolley.com
- **Phone:** 864-332-9043
- **Location:** Anderson, SC

### Forms:

Both forms are ready to go:
- **Booking form:** `/booking.html` → `/booking-success.html`
- **Contact form:** `/contact.html` → `/contact-success.html`

---

## Need Help?

**Common issues:**

1. **CSS not loading?**
   - Run `npm run build`
   - Check that `/dist/output.css` exists

2. **Forms not working locally?**
   - Forms only work when deployed to Netlify
   - Use Netlify CLI or deploy to test forms

3. **Images not showing?**
   - Check file paths: `assets/images/your-image.jpg`
   - Make sure images are in the correct folder

---

**You're ready to launch!** 🚀
