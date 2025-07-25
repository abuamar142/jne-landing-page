# JNE Landing Page

> Landing page modern dan responsif untuk JNE Express - perusahaan ekspedisi pengiriman barang
> terpercaya di Indonesia.

![JNE Landing Page](https://img.shields.io/badge/Vue.js-4FC08D?style=for-the-badge&logo=vuedotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)

## ✨ Fitur Utama

- **🚀 Modern Design** - Interface yang clean, modern, dan user-friendly
- **📱 Responsive** - Optimal di desktop, tablet, dan mobile
- **⚡ Fast Loading** - Dioptimasi untuk performa tinggi
- **🎨 Interactive UI** - Animasi smooth dan efek hover yang menarik
- **📦 Tracking System** - Fitur pelacakan kiriman real-time
- **🎯 SEO Optimized** - Struktur yang ramah mesin pencari

## 🛠️ Tech Stack

- **Framework:** Vue.js 3 dengan Composition API
- **Language:** TypeScript
- **Styling:** Tailwind CSS v4
- **Build Tool:** Vite
- **Testing:** Vitest + Playwright
- **Linting:** ESLint + Prettier

## 📋 Sections

### 🏠 Beranda

- **Hero Section** - Tagline utama dengan CTA yang jelas
- **Services** - Layanan unggulan (Express, Logistics, Freight)
- **Tracking** - Form pelacakan kiriman dengan simulasi hasil

### ℹ️ Tentang Kami

- **Company Story** - Perjalanan JNE selama 35+ tahun
- **Statistics** - Pencapaian dan jangkauan layanan
- **Values** - Nilai-nilai perusahaan dengan icon menarik

### 🚀 Fitur Unggulan

- **Real-time Tracking** - Pelacakan status pengiriman
- **Service Categories** - Berbagai jenis layanan pengiriman
- **Contact Integration** - Informasi kontak dan media sosial
- **Responsive Navigation** - Menu mobile-friendly

## 🚀 Quick Start

### Prerequisites

- Node.js 18+
- npm atau yarn

### Installation

```bash
# Clone repository
git clone <repository-url>
cd jne-landing-page

# Install dependencies
npm install

# Start development server
npm run dev
```

### Available Scripts

```bash
# Development
npm run dev          # Start dev server (localhost:5173)

# Build & Preview
npm run build        # Build for production
npm run preview      # Preview production build

# Testing
npm run test:unit    # Run unit tests
npm run test:e2e     # Run E2E tests

# Code Quality
npm run lint         # Run ESLint
npm run type-check   # TypeScript type checking
```

## 📁 Project Structure

```
src/
├── components/          # Reusable components
│   ├── home/           # Home page specific components
│   │   ├── HeroSection.vue
│   │   ├── ServicesSection.vue
│   │   └── TrackingSection.vue
│   └── layout/         # Layout components
│       ├── Header.vue
│       └── Footer.vue
├── views/              # Page components
│   ├── HomeView.vue
│   └── AboutView.vue
├── router/             # Vue Router config
├── stores/             # Pinia stores
└── assets/             # Static assets
```

## 🎨 Design System

### Colors

- **Primary Red:** `#dc2626` (JNE Brand Color)
- **Secondary:** `#64748b` (Gray)
- **Success:** `#10b981` (Green)
- **Warning:** `#f59e0b` (Yellow)

### Typography

- **Font:** Inter (System font fallback)
- **Headings:** Bold, various sizes
- **Body:** Regular weight, 1.6 line height

### Components

- **Buttons:** Rounded corners, hover effects, gradient backgrounds
- **Cards:** Shadow, rounded borders, hover animations
- **Forms:** Clean inputs, focus states, validation

## 📱 Responsive Breakpoints

```css
sm: 640px   # Small devices
md: 768px   # Medium devices
lg: 1024px  # Large devices
xl: 1280px  # Extra large devices
```

## ⚡ Performance Features

- **Code Splitting** - Lazy loading untuk optimasi bundle
- **Image Optimization** - Kompresi dan lazy loading gambar
- **CSS Purging** - Hanya CSS yang digunakan yang di-bundle
- **Tree Shaking** - Eliminasi dead code otomatis

## 🔧 Configuration

### Tailwind CSS

Konfigurasi custom di `tailwind.config.js` dengan:

- Custom colors sesuai brand JNE
- Extended spacing dan typography
- Custom animations dan transitions

### Vite

Setup optimal untuk development dan production di `vite.config.ts`

## 🌟 Key Features Implementation

### Hero Section

- Gradient background dengan pattern
- Animated statistics counter
- Interactive CTA buttons
- Floating elements dengan animasi

### Services Section

- Grid layout responsif
- Hover effects pada cards
- Icon integration
- Feature lists dengan checkmarks

### Tracking Section

- Form handling dengan validation
- Loading states dan progress indicators
- Sample tracking results
- Quick action buttons

## 🚀 Deployment

Build project untuk production:

```bash
npm run build
```

File hasil build akan tersedia di folder `dist/` dan siap untuk deployment ke:

- Netlify
- Vercel
- GitHub Pages
- Traditional hosting

## 🤝 Contributing

1. Fork repository
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open Pull Request

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

## 📞 Support

Untuk pertanyaan atau support:

- **Email:** support@jne.co.id
- **Phone:** 14045
- **Website:** https://www.jne.co.id

---

**Dibuat dengan ❤️ untuk JNE Express Indonesia**
