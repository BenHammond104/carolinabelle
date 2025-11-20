# The Carolina Belle Trolley Co. Website

A clean, professional website for The Carolina Belle Trolley Co., offering classic wedding trolley services in Anderson, Greenville, Clemson, and surrounding South Carolina areas.

## Project Overview

This is a static website built with:
- **HTML5** - Semantic, accessible markup
- **Tailwind CSS** - Utility-first CSS framework
- **Netlify Forms** - Form handling for booking and contact
- **Vanilla JavaScript** - Simple interactions (mobile menu, FAQ accordion, gallery filter)

## Pages

- **Home** (`index.html`) - Hero, highlights, how it works, testimonials
- **About** (`about.html`) - Company story, values, trolley specs
- **Pricing** (`pricing.html`) - Packages, pricing, policies
- **Booking** (`booking.html`) - Availability check form with Netlify Forms
- **Gallery** (`gallery.html`) - Photo grid with category filters
- **FAQs** (`faqs.html`) - Accordion-style Q&A
- **Service Area** (`service-area.html`) - Cities served, venue info
- **Contact** (`contact.html`) - Contact info and message form
- **Success Pages** (`booking-success.html`, `contact-success.html`) - Form confirmation

## Brand Colors

- **Cream**: `#F5F3EE` (belle-cream)
- **Gold**: `#D4AF37` (belle-gold)
- **Dark**: `#1A1A1A` (belle-dark)

## Project Structure

```
CarolinaBelle/
├── index.html              # Home page
├── about.html              # About page
├── pricing.html            # Pricing & packages
├── booking.html            # Booking form
├── booking-success.html    # Booking confirmation
├── gallery.html            # Photo gallery
├── faqs.html              # FAQs
├── service-area.html      # Service area info
├── contact.html           # Contact form
├── contact-success.html   # Contact confirmation
├── src/
│   └── input.css          # Tailwind source
├── dist/
│   └── output.css         # Compiled CSS (generated)
├── assets/
│   └── images/            # Place your images here
├── tailwind.config.js     # Tailwind configuration
├── netlify.toml          # Netlify deployment config
├── package.json          # npm dependencies
└── README.md            # This file
```

## Local Development

### Prerequisites
- Node.js 18+ installed

### Setup

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Build CSS:**
   ```bash
   npm run build
   ```

3. **Watch mode (auto-rebuild CSS):**
   ```bash
   npm run dev
   ```

4. **Open in browser:**
   Simply open `index.html` in your browser, or use a local server:
   ```bash
   # Using Python
   python -m http.server 8000

   # Using Node.js http-server (install globally first)
   npx http-server
   ```

## Deployment to Netlify

### Option 1: Netlify Drop (Drag & Drop)

1. Run `npm run build` to generate the CSS
2. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
3. Drag the entire project folder onto the page
4. Your site will be live instantly

### Option 2: Connect to Git (Recommended)

1. **Push to GitHub:**
   ```bash
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin YOUR_GITHUB_REPO_URL
   git push -u origin main
   ```

2. **Deploy on Netlify:**
   - Go to [app.netlify.com](https://app.netlify.com)
   - Click "Add new site" → "Import an existing project"
   - Choose GitHub and select your repository
   - Netlify will auto-detect settings from `netlify.toml`
   - Click "Deploy site"

3. **Netlify Forms Setup:**
   Forms will automatically work once deployed. Submissions will appear in:
   - Netlify Dashboard → Your Site → Forms

### Option 3: Netlify CLI

```bash
# Install Netlify CLI
npm install -g netlify-cli

# Login
netlify login

# Deploy
netlify deploy --prod
```

## Customization

### Adding Your Images

1. Place images in `/assets/images/`
2. Update image sources in HTML files:
   ```html
   <!-- Replace placeholder with actual image -->
   <img src="assets/images/trolley-exterior.jpg" alt="Carolina Belle Trolley exterior">
   ```

### Gallery Images

Replace the placeholder divs in `gallery.html` with actual images:

```html
<!-- Current placeholder -->
<div class="aspect-[4/3] bg-gray-200 rounded-lg...">
    <p>Photo: Trolley Exterior</p>
</div>

<!-- Replace with -->
<div class="gallery-item" data-category="weddings">
    <img src="assets/images/wedding-1.jpg" alt="Bridal party with trolley" class="aspect-[4/3] object-cover rounded-lg cursor-pointer hover:opacity-90 transition">
</div>
```

### Updating Content

All content is in plain HTML. Simply search for the text you want to change and update it directly in the HTML files.

### Changing Colors

Edit `tailwind.config.js`:

```js
colors: {
  'belle-cream': '#F5F3EE',  // Your custom cream
  'belle-gold': '#D4AF37',   // Your custom gold
  'belle-dark': '#1A1A1A',   // Your custom dark
},
```

Then rebuild CSS:
```bash
npm run build
```

## SEO

Each page includes:
- Unique `<title>` tags
- Meta descriptions
- Semantic HTML structure
- Alt text placeholders (add descriptions when you add images)

## Forms

### Booking Form
- Location: `booking.html`
- Action: Posts to Netlify Forms
- Redirects to: `booking-success.html`

### Contact Form
- Location: `contact.html`
- Action: Posts to Netlify Forms
- Redirects to: `contact-success.html`

### Accessing Form Submissions

After deploying to Netlify:
1. Go to your Netlify dashboard
2. Click on your site
3. Navigate to "Forms" in the sidebar
4. View and export submissions

You can also set up email notifications:
- Site Settings → Forms → Form notifications
- Add notification emails

## Browser Support

Modern browsers (Chrome, Firefox, Safari, Edge). Tailwind CSS ensures good compatibility.

## Next Steps

1. **Add actual images** to `/assets/images/`
2. **Replace gallery placeholders** with real photos
3. **Add logo** to navigation (replace text with `<img>` tag)
4. **Set up custom domain** in Netlify
5. **Configure form notifications** in Netlify dashboard
6. **Add Google Analytics** (add tracking code to all pages)
7. **Test forms** after deployment
8. **Add favicon** (`favicon.ico` in root directory)

## Support

For questions about the website code or deployment, refer to:
- [Tailwind CSS Docs](https://tailwindcss.com/docs)
- [Netlify Docs](https://docs.netlify.com)
- [Netlify Forms Guide](https://docs.netlify.com/forms/setup/)

## License

All rights reserved - The Carolina Belle Trolley Co. © 2025
