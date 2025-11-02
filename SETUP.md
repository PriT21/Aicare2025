# AICARE 2025 React Website - Setup Guide

## Overview
This is a React conversion of the AICARE 2025 conference website, previously built with HTML/Tailwind CSS/Vanilla JS.

## Project Structure
```
src/
├── components/
│   ├── Navbar.jsx          # Responsive navigation with dropdowns
│   └── Footer.jsx          # Footer component
├── pages/
│   ├── Home.jsx            # Main landing page with countdown timer
│   ├── About*.jsx          # About pages (UEM, COERE, COEA)
│   ├── *Conference*.jsx    # Conference pages (Tracks, Guidelines, etc.)
│   ├── Registration.jsx    # Registration page
│   ├── Venue.jsx           # Venue page
│   ├── ContactUs.jsx       # Contact page
│   ├── Speakers.jsx        # Speakers page
│   ├── PlaceholderPage.jsx # Reusable placeholder component
│   └── committee/
│       ├── OrganizingCommittee.jsx
│       ├── NationalAdvisoryCommittee.jsx
│       ├── InternationalAdvisoryCommittee.jsx
│       ├── TechnicalProgramCommittee.jsx
│       └── StudentCommittee.jsx
├── App.jsx                 # Main app with routing
├── main.jsx                # Entry point
└── index.css               # Global styles
```

## Key Features Implemented

### ✅ Completed
- **React Router** - Multi-page SPA with client-side routing
- **Responsive Navbar** - Desktop/Mobile menu toggle with dropdowns
- **Hero Section** - Background image, logos, responsive layout
- **Countdown Timer** - Live countdown to conference date
- **About Section** - Conference information
- **Key Dates Timeline** - Responsive timeline with dates
- **World Participation** - Country-based visit counter
- **SEO Optimization** - React Helmet for meta tags and SEO
- **Responsive Design** - Mobile, tablet, desktop optimized with Tailwind CSS
- **Tailwind CSS** - All styling using Tailwind utilities
- **Assets** - All images copied to public/assets folder

### 🚀 What You Can Do Next

1. **Update Placeholder Pages** - Replace content in pages with real information:
   - Track of Conference page
   - Submission Guidelines page
   - Committee member details
   - Speaker information
   - Contact form
   - Venue map/details

2. **Add Interactive Features**:
   - Contact form with email validation
   - Paper submission form
   - Committee member profiles with images
   - Speaker testimonials/bios
   - FAQ section
   - Search functionality

3. **Enhance SEO**:
   - Add structured data (Schema.org)
   - Optimize images
   - Add canonical tags
   - Submit sitemap to search engines

## Installation & Setup

### 1. Install Dependencies
```bash
cd C:\Users\pritd\Projects\college-website-react
npm install --legacy-peer-deps
```

### 2. Development Server
```bash
npm run dev
```
Visit `http://localhost:5173` to see the site

### 3. Build for Production
```bash
npm run build
```
Output files will be in the `dist/` folder

### 4. Preview Production Build
```bash
npm run preview
```

### 5. Lint Code
```bash
npm run lint
```

## Technologies Used
- **React 19** - UI library
- **React Router DOM** - Client-side routing
- **React Helmet Async** - SEO/Meta tags
- **Vite** - Build tool (fast development)
- **Tailwind CSS** - Utility-first CSS
- **PostCSS** - CSS processing
- **AutoPrefixer** - Browser compatibility

## Responsive Design Breakpoints
- Mobile: < 640px (sm)
- Tablet: 640px - 1024px (md, lg)
- Desktop: > 1024px (lg, xl)

## File Locations
- **Images/Assets**: `public/assets/`
- **Source Code**: `src/`
- **Build Output**: `dist/`
- **Config Files**: 
  - `vite.config.js` - Vite config
  - `tailwind.config.js` - Tailwind config
  - `postcss.config.js` - PostCSS config

## Important Notes

### Asset Paths
All asset paths should use `/assets/filename` (from public folder):
```jsx
<img src="/assets/IEM_Logo.png" alt="IEM Logo" />
```

### Routing
Navigate using React Router's `Link` component:
```jsx
import { Link } from 'react-router-dom';
<Link to="/venue">Go to Venue</Link>
```

### SEO Meta Tags
Use React Helmet for page-specific SEO:
```jsx
import { Helmet } from 'react-helmet-async';

<Helmet>
  <title>Page Title - AICARE 2025</title>
  <meta name="description" content="Page description" />
  <meta property="og:title" content="OG Title" />
</Helmet>
```

## Next Steps to Complete

1. **Fill content in placeholder pages** - Use content from old HTML files
2. **Add contact form** - Connect with email service
3. **Update committee member info** - Add names, titles, photos
4. **Add speaker bios** - With photos and details
5. **Set up Analytics** - Google Analytics, etc.
6. **Test on all devices** - Mobile, tablet, desktop
7. **Deploy** - To your hosting provider (Vercel, Netlify, etc.)

## Deployment Options

### Vercel (Recommended for React)
```bash
npm install -g vercel
vercel
```

### Netlify
```bash
npm install -g netlify-cli
netlify deploy
```

### Traditional Hosting
Build and upload `dist/` folder to your host

## Questions?
- Check React documentation: https://react.dev
- Tailwind CSS docs: https://tailwindcss.com
- React Router: https://reactrouter.com
