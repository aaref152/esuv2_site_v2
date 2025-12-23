# Service Platform Website v2

A modern, multilingual service marketplace platform with support for English and Thai languages.

## 🌐 Languages

- 🇬🇧 English (Default)
- 🇹🇭 Thai

## ✨ Features

- **Multilingual Support**: Easy language switching between English and Thai
- **Responsive Design**: Works perfectly on desktop, tablet, and mobile devices
- **Modern UI**: Built with Tailwind CSS for a clean, professional look
- **Service Categories**: 8 different service categories including:
  - Transportation Services
  - Construction & Household Services
  - Cleaning Services
  - Automotive Services
  - Health & Beauty
  - Social & Personal Services
  - Pet Care
  - Computer Services
- **For Executors**: Special section for service providers with registration and benefits
- **Legal Documents**: Privacy policy, user agreement, and public offer in multiple languages

## 🚀 Quick Start

### Local Development

1. Clone this repository:
```bash
git clone https://github.com/YOUR_USERNAME/esuv2_site_v2.git
cd esuv2_site_v2
```

2. Open `index.html` in your web browser, or use a local server:
```bash
# Using Python
python -m http.server 8000

# Using PHP
php -S localhost:8000

# Using Node.js (http-server)
npx http-server -p 8000
```

3. Visit `http://localhost:8000` in your browser

### Deploy to GitHub Pages

See [GITHUB_SETUP_GUIDE.md](GITHUB_SETUP_GUIDE.md) for detailed instructions on:
- Creating a GitHub repository
- Pushing your code
- Enabling GitHub Pages
- Configuring custom domains

## 📁 Project Structure

```
esuv2_site_v2/
├── index.html                 # Main homepage (multilingual)
├── privacy-policy.html        # Privacy policy (Russian)
├── privacy-policy-en.html     # Privacy policy (English)
├── user-agreement.html        # User agreement (Russian)
├── user-agreement-en.html     # User agreement (English)
├── public-offer.html          # Public offer (Russian)
├── public-offer-en.html       # Public offer (English)
├── assets/                    # Images and media files
│   ├── Логотип СУ.jpg
│   ├── client_avatar_example.jpg
│   └── favicon-sy.ico
├── js/
│   └── translations.js        # Multilingual translation system
├── css/
│   └── styles.css
├── CNAME                      # Custom domain configuration
├── docker-compose.yml         # Docker configuration
├── robots.txt                 # SEO file
├── sitemap.xml                # SEO file
├── GITHUB_SETUP_GUIDE.md      # Deployment guide
└── README.md                  # This file
```

## 🎨 Technologies Used

- **HTML5**: Semantic markup
- **Tailwind CSS 3.4.16**: Utility-first CSS framework (via CDN)
- **Vanilla JavaScript**: For multilingual support and interactions
- **Remix Icon 4.6.0**: Icon library
- **Google Fonts**: Pacifico font for branding

## 🌍 How Multilingual Support Works

The website uses a JavaScript-based translation system:

1. **translations.js**: Contains all translations for English and Thai
2. **Language Detection**: Automatically detects saved language preference from localStorage
3. **Easy Switching**: Users can switch languages using the EN/TH buttons in the header
4. **Persistent Selection**: Language preference is saved and remembered for future visits
5. **Dynamic Content**: All text content updates instantly when switching languages
6. **Document Links**: Legal documents automatically switch to the correct language version

## 📞 Contact Information

- **Email**: singleservice2022@gmail.com
- **Telegram Bot (Clients)**: https://t.me/esu_client_bot
- **Telegram Bot (Executors)**: https://t.me/esu_executor_bot
- **Location**: 606440, Nizhny Novgorod region, Bor, Russia

## 📄 Legal

**IP Sosedov Dmitry Igorevich**
- INN: 524615242985
- OGRNIP: 321527500125360
- Legal Address: 606440, Nizhny Novgorod region, Bor

## 🔧 Customization

### Adding a New Language

1. Open `js/translations.js`
2. Add a new language object with all required translations:
```javascript
const translations = {
    en: { /* English translations */ },
    th: { /* Thai translations */ },
    your_lang: {
        siteName: "Your Translation",
        aboutMenu: "About",
        // ... add all translation keys
    }
};
```
3. Add a language button in `index.html`:
```html
<button class="lang-btn" data-lang="your_lang">YOUR_LANG</button>
```

### Changing Colors

The website uses Tailwind CSS with custom colors defined in the Tailwind config:
- **Primary**: `#3b82f6` (blue)
- **Teal/Accent**: `#14b8a6` (teal)

You can modify these in the `<script>` tag in `index.html` where Tailwind is configured.

## 📈 Analytics

The website includes Yandex Metrika for analytics (ID: 103165085).

To use your own analytics:
1. Replace the Yandex Metrika code in `index.html`
2. Or add Google Analytics, Plausible, or your preferred analytics service

## 🐳 Docker Support

The project includes a `docker-compose.yml` file for easy deployment with Nginx:

```bash
docker-compose up -d
```

This will serve the website on port 8010.

## 📝 License

© 2025 IP Sosedov Dmitry Igorevich. All rights reserved.

## 🤝 Contributing

This is a private business website. For inquiries, please contact via email.

---

**Note**: This is version 2 (v2) of the Service Platform website with enhanced multilingual support.
