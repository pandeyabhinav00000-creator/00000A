# Namveda Ayurveda — Website

Premium Ayurvedic e-commerce website built with vanilla HTML, CSS, and JavaScript.

## 📁 Project Structure

```
namveda-site/
├── index.html              ← Main SPA entry point
├── vercel.json             ← Vercel deployment config
├── assets/
│   ├── css/
│   │   └── style.css       ← All styles (design system, components, animations)
│   └── js/
│       └── main.js         ← All logic (data, cart, wishlist, routing, carousels)
└── README.md
```

## ✨ Features

- **Preloader** — White background, logo + name + "Loading Experience..." text, animated green line bar (2 passes), smooth fade-out
- **Smooth Animations** — IntersectionObserver-based reveal: `fadeInUp`, `fadeInLeft`, `fadeInRight`, `fadeInDown`, `scale`, `fade` — carousels and preloader excluded
- **SPA Navigation** — All pages in one HTML file: Home, Shop, Product Detail, Cart, Wishlist, Checkout, Policy
- **Carousels** — Category + Testimonials with CSS infinite scroll + touch/mouse drag swipe
- **Cart & Wishlist** — localStorage persistence
- **Responsive** — Mobile-first, works on all screen sizes
- **Mobile Bottom Nav** — Fixed 4-tab nav on mobile only
- **FAQs** — Accordion with smooth expand/collapse

## 🚀 Deploy on Vercel

### Option 1: Drag & Drop (Fastest)
1. Go to [vercel.com](https://vercel.com) → Log in
2. Click **"Add New Project"** → **"Deploy without Git"**
3. Drag the entire `namveda-site/` folder into the upload area
4. Click **Deploy** — done! Live in ~30 seconds

### Option 2: Via GitHub (Recommended for updates)
1. Create a new GitHub repository (e.g. `namveda-ayurveda`)
2. Upload all files from `namveda-site/` to the repository root
3. Go to [vercel.com](https://vercel.com) → **"Add New Project"**
4. Import your GitHub repo
5. Framework: **Other** (auto-detected as static)
6. Root directory: leave as `/`
7. Click **Deploy**

### Option 3: Vercel CLI
```bash
npm install -g vercel
cd namveda-site
vercel
# Follow prompts — select "Other" framework
```

## 🛠 Customisation

### Replace logo
Search for `https://i.imgur.com/AzOWZzB.png` in `index.html` and replace with your image URL or local path.

### Change brand colours
Edit CSS variables in `assets/css/style.css`:
```css
:root {
  --primary:   #004225;   /* Deep Forest Green */
  --secondary: #355E3B;   /* Classic Botanical Green */
  --accent:    #4C6B47;   /* Soft Olive Green */
  --gold:      #b8965a;   /* Golden accent */
}
```

### Add/edit products
Edit the `PRODUCTS` array in `assets/js/main.js`.

### Add/edit FAQs
Edit the `FAQS` array in `assets/js/main.js`.

## 📱 Browser Support
Chrome, Firefox, Safari, Edge (all modern versions) · iOS Safari · Android Chrome

## ⚡ Performance
- Zero external JS libraries (no jQuery, no Bootstrap, no GSAP)
- CSS animations only (GPU-accelerated `transform` and `opacity`)
- IntersectionObserver fires once per element, then disconnects
- Images are lazy-loaded
- Fonts preconnected for faster load
