# Deployment Guide - Aarins Barbershop Website

This guide provides step-by-step instructions for deploying the Aarins Barbershop website to production.

## Pre-Deployment Checklist

### 1. Content Review ✓
- [ ] All business information is accurate
- [ ] Phone number: (916) 754-2165
- [ ] Address: 7837 Stockton Blvd, Sacramento, CA 95823
- [ ] Business hours are correct
- [ ] Booking link works: https://aarinthebarber.booksy.com
- [ ] All service descriptions and pricing are current
- [ ] About section reflects Aaron's story accurately

### 2. Images ✓
- [ ] Add professional logo (`assets/images/logo.png`)
- [ ] Add hero section image (`assets/images/hero-barber.jpg`)
- [ ] Add Aaron's photo (`assets/images/aaron-barber.jpg`)
- [ ] Add gallery images (6 images in `assets/images/gallery/`)
- [ ] Add Open Graph image (`assets/images/og-image.jpg`)
- [ ] Add favicon (`assets/images/favicon.ico`)
- [ ] Add Apple touch icon (`assets/images/apple-touch-icon.png`)
- [ ] Optimize all images for web (compress to under 500KB each)

### 3. Technical Configuration ✓
- [ ] Update domain name in `sitemap.xml`
- [ ] Update canonical URLs in `index.html`
- [ ] Update Open Graph URLs
- [ ] Configure .htaccess file for your domain
- [ ] Test all internal links
- [ ] Test external links (Booksy, Google Maps, social media)

### 4. SEO Configuration ✓
- [ ] Verify schema markup is correct
- [ ] Check meta descriptions are unique and compelling
- [ ] Ensure all images have alt text
- [ ] Test sitemap.xml format
- [ ] Verify robots.txt is accessible

## Deployment Steps

### Step 1: Domain and Hosting Setup
1. **Purchase Domain**: Register `aarinsbarbershop.com` or your chosen domain
2. **Choose Hosting**: Select a reliable web hosting provider
3. **SSL Certificate**: Ensure HTTPS is enabled
4. **DNS Configuration**: Point domain to hosting server

### Step 2: File Upload
1. **Upload Files**: Transfer all website files to your web server
2. **Set Permissions**: Ensure proper file permissions (644 for files, 755 for directories)
3. **Test Access**: Verify website loads at your domain

### Step 3: Configuration Updates
1. **Update URLs**: Replace all instances of `aarinsbarbershop.com` with your actual domain
2. **Test .htaccess**: Ensure Apache modules are available
3. **Check Redirects**: Test HTTPS redirects and trailing slashes

### Step 4: Third-Party Integrations
1. **Google Analytics**: 
   - Create Google Analytics account
   - Add tracking code to `index.html`
   - Test tracking implementation
2. **Google Search Console**:
   - Verify domain ownership
   - Submit sitemap.xml
   - Monitor indexing status
3. **Google My Business**:
   - Claim/verify business listing
   - Ensure NAP consistency
   - Add website URL to listing

### Step 5: Testing
1. **Browser Testing**: Test on Chrome, Firefox, Safari, Edge
2. **Mobile Testing**: Test on various mobile devices
3. **Speed Testing**: Use Google PageSpeed Insights
4. **SEO Testing**: Use Google Search Console
5. **Accessibility Testing**: Use WAVE or similar tools

## Post-Deployment Tasks

### Immediate (Day 1)
- [ ] Submit sitemap to Google Search Console
- [ ] Test all contact forms and booking links
- [ ] Check website loads correctly on mobile devices
- [ ] Verify Google Analytics is tracking visits
- [ ] Test 404 error page functionality

### First Week
- [ ] Monitor Google Search Console for crawl errors
- [ ] Check website performance metrics
- [ ] Review initial analytics data
- [ ] Test all social media links
- [ ] Verify local business listings are updated

### First Month
- [ ] Monitor search engine rankings
- [ ] Review and optimize page load speeds
- [ ] Update business hours if needed
- [ ] Add more gallery images as available
- [ ] Collect and add customer testimonials

## Domain-Specific Updates

### Update These Files:
1. **sitemap.xml**: Replace `aarinsbarbershop.com` with your domain
2. **index.html**: Update canonical URLs and Open Graph URLs
3. **.htaccess**: Update domain references in hotlink protection
4. **404.html**: No changes needed (uses relative paths)

### Search and Replace:
Replace `https://aarinsbarbershop.com` with your actual domain in:
- sitemap.xml (all `<loc>` tags)
- index.html (canonical and Open Graph meta tags)
- .htaccess (hotlink protection rules)

## Analytics Setup

### Google Analytics 4
1. Create GA4 property
2. Get Measurement ID
3. Add tracking code before `</head>` in index.html:

```html
<!-- Google tag (gtag.js) -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

### Google Search Console
1. Add property for your domain
2. Verify ownership via HTML file or DNS
3. Submit sitemap: `https://yourdomain.com/sitemap.xml`
4. Monitor indexing and search performance

## Security Checklist

### Pre-Launch Security
- [ ] SSL certificate installed and working
- [ ] HTTP to HTTPS redirects enabled
- [ ] Security headers configured in .htaccess
- [ ] Content Security Policy implemented
- [ ] File permissions set correctly
- [ ] Sensitive files protected

### Ongoing Security
- [ ] Regular backups scheduled
- [ ] Keep software updated
- [ ] Monitor for security vulnerabilities
- [ ] Use strong admin passwords
- [ ] Implement 2FA where possible

## Performance Optimization

### Before Launch
- [ ] Optimize images (compress, resize, use appropriate formats)
- [ ] Enable GZIP compression
- [ ] Configure browser caching
- [ ] Minify CSS and JavaScript if needed
- [ ] Use CDN for external resources

### After Launch
- [ ] Monitor Core Web Vitals
- [ ] Optimize Largest Contentful Paint
- [ ] Minimize Cumulative Layout Shift
- [ ] Improve First Input Delay
- [ ] Regular performance audits

## Troubleshooting

### Common Issues
1. **Images not loading**: Check file paths and permissions
2. **Styles not applying**: Verify CSS file paths
3. **404 errors**: Check .htaccess configuration
4. **Mobile issues**: Test responsive design
5. **Slow loading**: Optimize images and enable compression

### Testing Tools
- **Google PageSpeed Insights**: Performance testing
- **GTmetrix**: Detailed performance analysis
- **Google Search Console**: SEO and indexing issues
- **WAVE**: Accessibility testing
- **Responsive Design Checker**: Mobile compatibility

## Maintenance Schedule

### Weekly Tasks
- [ ] Check website uptime
- [ ] Monitor Google Analytics
- [ ] Review contact form submissions
- [ ] Update gallery with new photos
- [ ] Check booking system functionality

### Monthly Tasks
- [ ] Review SEO rankings
- [ ] Update testimonials
- [ ] Check for broken links
- [ ] Review and update content
- [ ] Backup website files

### Quarterly Tasks
- [ ] Comprehensive performance review
- [ ] Security audit
- [ ] Update business information
- [ ] Review and optimize SEO
- [ ] Plan content updates

## Support and Maintenance

### Technical Support
- **Hosting Provider**: Contact for server issues
- **Domain Registrar**: For domain-related issues
- **Developer**: For code modifications
- **SEO Specialist**: For optimization improvements

### Regular Updates
- Keep business information current
- Add new services or pricing changes
- Update gallery with recent work
- Refresh testimonials regularly
- Monitor and respond to reviews

## Launch Announcement

### Marketing Checklist
- [ ] Update Google My Business with new website
- [ ] Announce on social media platforms
- [ ] Send email to existing customers
- [ ] Update business cards and marketing materials
- [ ] Submit to local business directories
- [ ] Consider press release for local media

### Success Metrics
- Website traffic (Google Analytics)
- Online bookings through Booksy
- Phone call inquiries
- Local search rankings
- Social media engagement
- Customer feedback and reviews

---

**Congratulations on your new website! 🎉**

Your Aarins Barbershop website is now ready to help grow your business and serve your customers better. Remember to keep content fresh and monitor performance regularly for the best results. 