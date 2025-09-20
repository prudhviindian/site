# Deployment Guide for PhysioTime Website

## Free Hosting Options

### 1. GitHub Pages (Recommended for beginners)

**Step 1**: Push your code to GitHub
```bash
git add .
git commit -m "PhysioTime website ready for deployment"
git push origin main
```

**Step 2**: Enable GitHub Pages
1. Go to your repository on GitHub
2. Click "Settings" tab
3. Scroll down to "Pages" section
4. Under "Source", select "Deploy from a branch"
5. Choose "main" branch and "/ (root)" folder
6. Click "Save"
7. Your site will be live at: `https://yourusername.github.io/site`

## Free .in Domain Options

### 1. Free .in Domain Providers

**Option A: Freenom (.tk, .ml, .ga, .cf)** - Unfortunately doesn't offer .in domains
**Option B: Student Programs**
- GitHub Student Pack includes free domain credits
- Some educational institutions provide free .in domains

**Option C: Promotional Offers**
- BigRock India sometimes offers free .in domains with hosting
- HostGator India promotional offers
- GoDaddy India first-year free promotions

### 2. Affordable .in Domain Options (₹99-₹499/year)
- **BigRock**: Often ₹99 for first year
- **GoDaddy India**: ₹149-₹299 first year
- **Namecheap**: ~$3-5 USD annually
- **HostGator India**: ₹199 first year

### 3. Free Hosting with Custom .in Domain

**Option A: GitHub Pages + Custom Domain**
1. Buy .in domain from above providers
2. Host on GitHub Pages (free)
3. Point domain to GitHub Pages

**Option B: Netlify + Custom Domain**
1. Host on Netlify (free tier)
2. Add your .in domain in Netlify dashboard
3. Update DNS settings

**Option C: Infinity Free (000webhost alternative)**
1. Sign up at infinityfree.net
2. Get free subdomain or use custom .in domain
3. Upload your files via FTP

### 4. Complete Free Setup Guide (.in domain)

**Step 1**: Get a .in domain
```
Recommended: BigRock India - Often has ₹99 first year offers
URL: www.bigrock.in
```

**Step 2**: Choose free hosting
```
Best options:
1. GitHub Pages (recommended)
2. Netlify 
3. Vercel
4. InfinityFree (traditional hosting)
```

**Step 3**: Connect domain to hosting
- For GitHub Pages: Add CNAME file with your domain
- For Netlify: Add domain in site settings
- For Vercel: Add domain in project settings

### 2. Netlify (Easiest drag-and-drop)

**Option A**: Drag and Drop
1. Go to [netlify.com](https://netlify.com)
2. Sign up for free account
3. Drag your project folder to the deploy area
4. Get instant live URL

**Option B**: Git Integration
1. Connect your GitHub repository
2. Automatic deployments on every push
3. Custom domain support available

### 3. Vercel (Great for developers)

**Step 1**: Install Vercel CLI (optional)
```bash
npm install -g vercel
```

**Step 2**: Deploy
```bash
vercel --prod
```

Or connect your GitHub repository at [vercel.com](https://vercel.com)

### 4. Firebase Hosting

**Step 1**: Install Firebase CLI
```bash
npm install -g firebase-tools
```

**Step 2**: Initialize and deploy
```bash
firebase login
firebase init hosting
firebase deploy
```

## Local Development

### Option 1: Python (if you have Python installed)
```bash
python -m http.server 8000
```
Then visit: http://localhost:8000

### Option 2: Node.js
```bash
npm install
npm run start-node
```

### Option 3: VS Code Live Server
1. Install "Live Server" extension in VS Code
2. Right-click on `index.html`
3. Select "Open with Live Server"

## Custom Domain Setup

### For .in Domain with GitHub Pages:
1. **Buy .in domain** (₹99-₹499/year from BigRock, GoDaddy India, etc.)
2. **Add CNAME file** to your repository:
   ```
   Create file: CNAME
   Content: yourdomain.in
   ```
3. **Configure DNS** with your domain provider:
   ```
   Type: A Record
   Name: @
   Value: 185.199.108.153
   Value: 185.199.109.153
   Value: 185.199.110.153
   Value: 185.199.111.153
   
   Type: CNAME
   Name: www
   Value: yourusername.github.io
   ```

### For .in Domain with Netlify:
1. Go to Site Settings > Domain Management
2. Add custom domain: yourdomain.in
3. Update DNS records as shown in Netlify dashboard:
   ```
   Type: A Record
   Name: @
   Value: 75.2.60.5
   
   Type: CNAME
   Name: www
   Value: your-site-name.netlify.app
   ```

### For .in Domain with Vercel:
1. Go to project settings > Domains
2. Add your .in domain
3. Update DNS records:
   ```
   Type: A Record
   Name: @
   Value: 76.76.19.61
   
   Type: CNAME
   Name: www
   Value: cname.vercel-dns.com
   ```

## Budget-Friendly Indian Hosting Options

### Traditional Hosting with .in Domain (₹200-₹500/year)
1. **HostGator India**: Often bundles free .in with hosting
2. **BigRock**: Complete packages starting ₹199/year
3. **GoDaddy India**: Economy plans with free domain
4. **A2Hosting India**: Good performance, includes domain

### Custom Domain Setup

### For GitHub Pages:
1. Buy domain from provider (Namecheap, GoDaddy, etc.)
2. Add CNAME file to repository with your domain
3. Configure DNS settings with your domain provider

### For Netlify/Vercel:
1. Go to domain settings in dashboard
2. Add your custom domain
3. Update DNS records as instructed

## Performance Tips

### Before Deployment:
- [ ] Test on mobile devices
- [ ] Check all links work
- [ ] Validate HTML/CSS
- [ ] Test contact form
- [ ] Optimize images (if added)
- [ ] Test loading speed

### After Deployment:
- [ ] Test live site on different devices
- [ ] Check contact form submission
- [ ] Set up analytics (Google Analytics)
- [ ] Submit to search engines
- [ ] Set up monitoring

## SEO Checklist

- [ ] Add meta descriptions
- [ ] Set up Google Search Console
- [ ] Create sitemap.xml
- [ ] Add robots.txt
- [ ] Optimize page titles
- [ ] Add alt text to images
- [ ] Set up structured data

## Maintenance

### Regular Updates:
- Update contact information
- Add new services
- Update team member information
- Refresh testimonials
- Update business hours

### Security:
- Keep dependencies updated
- Monitor for broken links
- Regular backups
- SSL certificate (auto with most hosts)

## Support

If you need help with deployment:
1. Check the hosting provider's documentation
2. Join their community forums
3. Contact their support team

Most hosting providers offer excellent free tiers and support for static websites like this one.
