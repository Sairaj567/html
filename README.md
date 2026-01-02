# Sairaj Nagargoje - Personal Portfolio

A modern, responsive single-page portfolio website showcasing projects, skills, and professional journey.

## 🚀 Recent Improvements (Jan 2026)

### SEO & Performance
- ✅ Comprehensive meta tags (Open Graph, Twitter Cards)
- ✅ Structured data (JSON-LD for search engines)
- ✅ Image lazy loading for better performance
- ✅ Asset versioning for cache busting
- ✅ robots.txt and sitemap.xml

### Infrastructure
- ✅ Nginx configuration with gzip compression
- ✅ Browser caching headers for static assets
- ✅ Security headers (CSP, X-Frame-Options, etc.)
- ✅ Custom 404 error page
- ✅ Apache .htaccess as alternative config

### CI/CD
- ✅ HTML validation step
- ✅ Automatic nginx reload after deployment
- ✅ Improved error handling in workflow

## 🛠️ Tech Stack

- **Frontend**: Vanilla HTML5, CSS3, JavaScript (ES6+)
- **Styling**: CSS Custom Properties, CSS Grid, Flexbox
- **Icons**: Ionicons 5.5.2
- **Fonts**: Google Fonts (Poppins)
- **Server**: Nginx on OCI VM
- **CI/CD**: GitHub Actions

## 📁 Project Structure

```
html/
├── index.html          # Main portfolio page
├── 404.html           # Custom error page
├── robots.txt         # Search engine directives
├── sitemap.xml        # SEO sitemap
├── nginx.conf         # Nginx server configuration
├── .htaccess          # Apache configuration (alternative)
├── assets/
│   ├── css/
│   │   └── style.css  # Main stylesheet
│   ├── js/
│   │   └── script.js  # Client-side interactions
│   └── images/        # Project images and assets
└── .github/
    └── workflows/
        └── deploy.yml # Automated deployment
```

## 🎯 Key Features

### Design
- Mobile-first responsive design
- Collapsible sidebar on mobile
- Smooth section transitions
- Custom gradient theme

### Functionality
- **Client-side navigation**: No page reloads between sections
- **Portfolio filtering**: Filter projects by category
- **Contact form**: Email client integration
- **Data-driven**: Uses data attributes for all interactions

### SEO
- Semantic HTML5
- Comprehensive meta tags
- Structured data for rich snippets
- Optimized images with alt text

## 🚀 Local Development

1. Clone the repository:
```bash
git clone https://github.com/Sairaj567/html.git
cd html/html
```

2. Serve locally:
```bash
# Using Python
python -m http.server 5500

# Using Node.js
npx serve . -l 5500

# Using PHP
php -S localhost:5500
```

3. Open browser: `http://localhost:5500`

## 📦 Deployment

### Automatic Deployment
Push to `master` branch triggers automatic deployment via GitHub Actions:
- Pulls latest code on OCI VM
- Validates HTML files
- Syncs to `/var/www/html/`
- Reloads Nginx

### Manual Deployment
```bash
ssh user@yourserver
cd /var/www/repo/html
git pull origin master
rsync -av --delete html/ /var/www/html/
sudo nginx -t && sudo systemctl reload nginx
```

## ⚙️ Nginx Setup

1. Copy nginx.conf to your server:
```bash
sudo cp html/nginx.conf /etc/nginx/sites-available/portfolio
sudo ln -s /etc/nginx/sites-available/portfolio /etc/nginx/sites-enabled/
```

2. Update domain name in nginx.conf:
```nginx
server_name yoursite.com www.yoursite.com;
```

3. Test and reload:
```bash
sudo nginx -t
sudo systemctl reload nginx
```

## 🔒 Security Headers

The nginx configuration includes:
- `X-Frame-Options`: Prevents clickjacking
- `X-Content-Type-Options`: Prevents MIME sniffing
- `X-XSS-Protection`: XSS filter
- `Content-Security-Policy`: Restricts resource loading
- `Referrer-Policy`: Controls referrer information

## 🎨 Customization

### Update Personal Info
Edit [html/index.html](html/index.html):
- Lines 40-150: Sidebar (name, contacts, social links)
- Lines 214-265: About section
- Lines 400-460: Experience/Education timeline
- Lines 475-510: Skills percentages
- Lines 561-610: Portfolio projects

### Change Theme Colors
Edit [assets/css/style.css](assets/css/style.css):
- Lines 19-75: `:root` CSS variables
- Modify gradient and solid color values

### Add New Section
1. Create `<article data-page="newsection">` in HTML
2. Add `<button data-nav-link>New Section</button>` to navbar
3. JavaScript auto-wires navigation

## 📊 Performance Optimizations

- **Gzip compression**: Reduces file sizes by ~70%
- **Browser caching**: Static assets cached for 1 year
- **Image lazy loading**: Improves initial load time
- **CSS/JS versioning**: Cache busting on updates
- **Minification ready**: Add build step for production

## 🔮 Future Improvements

- [ ] Add Google Analytics / Plausible
- [ ] Implement dark/light mode toggle
- [ ] Create downloadable PDF resume
- [ ] Add backend for contact form (Formspree/Netlify Forms)
- [ ] Convert images to WebP format
- [ ] Add print stylesheet
- [ ] Implement service worker for PWA

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 📧 Contact

**Sairaj Nagargoje**
- Email: sairajnagargoje567@gmail.com
- LinkedIn: [sairaj-nagargoje](https://www.linkedin.com/in/sairaj-nagargoje/)
- GitHub: [sairaj567](https://github.com/sairaj567)

---

**Last Updated**: January 3, 2026
