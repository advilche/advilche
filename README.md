# Adrian Vilchez - Personal Portfolio

A modern, responsive personal portfolio website showcasing Adrian Vilchez's skills, projects, and professional experience as a full-stack developer.

## 🚀 Features

- **Responsive Design**: Mobile-first approach with tablet and desktop breakpoints
- **Modern UI/UX**: Clean, professional design with smooth animations and transitions
- **Project Showcase**: Display of 6 featured projects with responsive images
- **Skills Section**: Highlighted technical skills with experience levels
- **Contact Form**: Functional contact form with form validation
- **Social Links**: Integration with GitHub and LinkedIn profiles
- **Accessibility**: Proper ARIA labels and semantic HTML structure

## 🏗️ Architecture

```
advilche/
├── index.html              # Main HTML structure
├── style.css               # CSS styles and responsive design
├── assets/                 # Images, icons, and media files
│   ├── favicon-32x32.png  # Site favicon
│   ├── icon-*.svg         # Social media and UI icons
│   ├── image-profile-*.webp # Responsive profile images
│   ├── pattern-*.svg      # Decorative background patterns
│   └── thumbnail-project-*.webp # Project showcase images
├── other/                  # Additional HTML files
└── README.md              # This file
```

## 🛠️ Tech Stack

### Frontend
- **HTML5** - Semantic markup and accessibility
- **CSS3** - Custom properties, Flexbox, Grid, and responsive design
- **Vanilla JavaScript** - Form validation and interactive elements
- **WebP Images** - Optimized image formats for better performance
- **Google Fonts** - Space Grotesk typography

### Design & UX
- **Mobile-First Design** - Responsive breakpoints at 37.5em and 62.5em
- **CSS Custom Properties** - Consistent theming with CSS variables
- **Smooth Transitions** - 250ms ease-in-out animations
- **Visual Feedback** - Form validation states and hover effects

## 🚀 Quick Start

### Prerequisites
- Modern web browser with CSS Grid and Flexbox support
- Local web server (optional, for development)

### 1. Clone and Setup

```bash
git clone https://github.com/advilche/advilche.git
cd advilche
```

### 2. Run Locally

**Option 1: Direct file opening**
Simply open `index.html` in your web browser

**Option 2: Local server (recommended)**
```bash
# Using Python 3
python -m http.server 8000

# Using Node.js
npx serve .

# Using PHP
php -S localhost:8000
```

Visit `http://localhost:8000` to see the portfolio!

## 📱 Responsive Breakpoints

- **Mobile**: Default (up to 37.5em / 600px)
- **Tablet**: 37.5em and above (600px+)
- **Desktop**: 62.5em and above (1000px+)

## 🎨 Design System

### Color Palette
```css
--bg-body: hsl(0, 0%, 8%)      /* Dark background */
--bg-body2: hsl(0, 0%, 14%)    /* Secondary background */
--accent: hsl(153, 71%, 59%)   /* Green accent */
--text1: hsl(0, 0%, 100%)      /* Primary text */
--text2: hsl(0, 0%, 85%)       /* Secondary text */
--invalid: hsl(7, 100%, 68%)   /* Error states */
```

### Typography
- **Font Family**: Space Grotesk (Google Fonts)
- **Font Sizes**: Responsive scaling from 1rem to 5.5rem
- **Line Heights**: Optimized for readability (1.1 for headings, 1.5 for body)

### Spacing & Layout
- **Container Width**: 69.375rem (1110px max)
- **Transitions**: 250ms ease-in-out
- **Grid System**: CSS Grid for project layouts
- **Flexbox**: Navigation and component alignment

## 📋 Project Sections

### 1. Hero Section
- Professional profile photo (responsive images)
- Introduction and tagline
- Call-to-action button
- Decorative background elements

### 2. Skills Section
- **C/C++**: 3 Years Experience
- **Python**: 3 Years Experience
- **HTML**: 1 Year Experience
- **Next.js**: 1 Year Experience
- **Node.js**: 1 Year Experience

### 3. Projects Showcase
- **Design Portfolio**: HTML/CSS
- **E-Learning Landing Page**: HTML/CSS
- **Todo Web App**: HTML/CSS/JavaScript
- **Entertainment Web App**: HTML/CSS/JavaScript
- **Memory Game**: HTML/CSS/JavaScript
- **Art Gallery Showcase**: HTML/CSS/JavaScript

### 4. Contact Section
- Contact form with validation
- Name, email, and message fields
- Form submission via Web3Forms API
- Professional contact information

## 🔧 Customization

### Updating Profile Information
Edit the following sections in `index.html`:
- Hero section text and profile photo
- Skills and experience levels
- Project descriptions and links
- Contact information and social links

### Styling Changes
Modify CSS custom properties in `style.css`:
```css
:root {
  --accent: hsl(153, 71%, 59%);    /* Change accent color */
  --bg-body: hsl(0, 0%, 8%);       /* Change background */
  --text1: hsl(0, 0%, 100%);       /* Change text color */
}
```

### Adding New Projects
1. Add project images to `assets/` folder
2. Update HTML structure in projects section
3. Ensure responsive images with `<picture>` elements
4. Add appropriate alt text and descriptions

## 🚀 Deployment

### GitHub Pages
1. Push code to GitHub repository
2. Enable GitHub Pages in repository settings
3. Select source branch (usually `main`)
4. Site will be available at `https://username.github.io/repository-name`

### Netlify
1. Connect GitHub repository to Netlify
2. Build command: (none needed for static site)
3. Publish directory: `.` (root)
4. Deploy automatically on push

### Vercel
1. Import GitHub repository to Vercel
2. Framework preset: Other
3. Build command: (none needed)
4. Output directory: `.`
5. Deploy automatically on push

## 📱 Browser Support

- **Modern Browsers**: Chrome, Firefox, Safari, Edge (latest versions)
- **CSS Features**: Grid, Flexbox, Custom Properties, Clamp()
- **JavaScript**: ES6+ features
- **Images**: WebP with fallback support

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 👤 About the Developer

**Adrian Vilchez** is a full-stack developer based in the US with experience in:
- C/C++ and Python development
- Web technologies (HTML, CSS, JavaScript)
- Modern frameworks (Next.js, Node.js)
- Building responsive and accessible web applications

## 📞 Contact

- **GitHub**: [@advilche](https://github.com/advilche)
- **LinkedIn**: [Adrian Vilchez](https://www.linkedin.com/in/adrian-vilchez1)
- **Portfolio**: [adrian-vilchez.com](https://adrian-vilchez.com)

---

*Built with ❤️ using modern web technologies* 