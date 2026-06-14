# 🍸 The Crafted Pour

**The Crafted Pour** is a premium, modern, and highly interactive single-page web application showcasing an artisanal cocktail and mocktail menu. Built with **React 19**, **Vite 8**, **Tailwind CSS v4**, and driven by **GSAP (GreenSock)** animations, it offers an immersive experience that blends fluid, scroll-driven storytelling with beautiful web aesthetics.

---

## ✨ Features

- **Interactive Hero Section**: A stunning greeting with an integrated, scroll-bound cinematic video playback that progresses as you scroll, alongside parallax floating decorative leaves.
- **Curated Menu Showcase**: Smooth interactive tabs and recipe sliders allowing visitors to explore signatures like the *Classic Mojito*, *Raspberry Mojito*, *Violet Breeze*, and *Curacao Mojito* with detailed tasting notes and recipes.
- **Dynamic Cocktails & Mocktails Grid**: Displays lists of the "Most Loved Mocktails" and "Most Popular Cocktails" with prices and origin details, decorated with scroll-controlled parallax elements.
- **Obsessive Brand Story ("About Us")**: A styled image grid with staggered entrances focusing on quality, mixology precision, and craftsmanship.
- **"The Art" Scroll-Trigger Section**: A premium visual section utilizing GSAP ScrollTrigger to scale image masks dynamically as you scroll, revealing hidden layouts under the heading *Sip-Worthy Perfection*.
- **Responsive Layout**: Crafted to deliver an equally beautiful, optimized experience across mobile, tablet, and desktop screens using viewport-aware styling and media hooks.

---

## 🛠️ Tech Stack

- **Frontend**: [React 19](https://react.dev/) & [Vite 8](https://vite.dev/) (Ultra-fast HMR and build performance)
- **Styling**: [Tailwind CSS v4](https://tailwindcss.com/) (Modern utility-first CSS engine)
- **Animations**: 
  - [GSAP (GreenSock Animation Platform)](https://gsap.com/)
  - [`@gsap/react`](https://www.npmjs.com/package/@gsap/react) (GSAP hooks for React lifecycle integration)
  - `GSAP ScrollTrigger` & `SplitText` (Custom scroll animations and letter-by-letter/word-by-word text effects)
- **Device Responsiveness**: `react-responsive` (Declarative media queries inside React components)

---

## 📂 Project Structure

```text
├── constants/
│   └── index.js            # Menu lists, mocktails, socials, and contact information
├── public/
│   ├── images/             # Floating assets, check icons, logo, and section backgrounds
│   └── videos/             # Background scroll-tied video (e.g., output.mp4)
├── src/
│   ├── components/
│   │   ├── About.jsx       # Brand grid and customer counter
│   │   ├── Art.jsx         # ScrollTrigger mask-image reveal effect
│   │   ├── Cocktails.jsx   # Curated price list with parallax leaves
│   │   ├── Contact.jsx     # Footer, opening hours, and socials
│   │   ├── Hero.jsx        # Video scrub control and initial typography split
│   │   ├── Menu.jsx        # Carousel recipe slider with tabs
│   │   └── Navbar.jsx      # Sticky blur header with scroll trigger
│   ├── App.jsx             # Main page layout assembler
│   ├── index.css           # Global custom typography, variables, and noise effects
│   └── main.jsx            # Application entrypoint
├── package.json            # Scripts & dependencies
└── vite.config.js          # Vite configurations
```

---

## 🚀 Getting Started

Follow these steps to run the project locally on your machine:

### Prerequisite

Ensure you have [Node.js](https://nodejs.org/) (v18.x or higher recommended) and npm/yarn installed.

### 1. Clone the repository
```bash
git clone https://github.com/your-username/the-crafted-pour.git
cd the-crafted-pour
```

### 2. Install dependencies
```bash
npm install
```

### 3. Run the development server
```bash
npm run dev
```
Open your browser and navigate to `http://localhost:5173` (or the port specified in your console).

### 4. Build for production
To compile the project with optimized assets for production hosting:
```bash
npm run build
```

---

## 🎨 Design and Animation Details

### Scroll-Tied Video Scrubbing
In the `Hero` section, React's `useRef` tracks the background video and syncs its `currentTime` to the ScrollTrigger timeline, scrubbed directly against the window's vertical scroll percentage.

### Custom Typography Splitting
Using `SplitText`, titles and subtitles are split dynamically into letters or lines at runtime, enabling organic staggered entry animations.

### Scroll-Reveal Masks
The `Art` component relies on CSS custom masks combined with GSAP's pin mechanism. On scroll, the mask scales up smoothly, creating a modern, cinematic "portal" transition revealing the underlying content block.
