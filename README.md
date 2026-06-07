# 🏫 Premier Schools Exhibition (PSE) Landing Page

Welcome to the official repository for the **Premier Schools Exhibition** web platform, live at [junior-school.netlify.app](https://junior-school.netlify.app/). 

This project is a high-performance, responsive, and visually striking single-page application (SPA) landing page designed to help parents discover top schools, pre-schedule appointments with admission heads, and compare curriculum details. It is built entirely from scratch with a focus on polished UI micro-interactions, smooth animations, and solid semantic accessibility.

---

## 🔗 Live Demo
Check out the live deployment of the site here:  
👉 **[https://junior-school.netlify.app/](https://junior-school.netlify.app/)**

---

## 🛠️ The Tech Stack (What We Used & Why)

We deliberately chose a lightweight, native web stack to ensure lightning-fast load times, flawless SEO indices, and zero build compilation overhead. 

*   **HTML5 (Semantic Structure):** Written with strict semantic markup (`<header>`, `<main>`, `<section>`, `<footer>`, `<dialog>`, etc.) to ensure clear page hierarchy and accessibility.
*   **Vanilla CSS3 (BEM Architecture & Variable Tokens):** 
    *   No bloated CSS frameworks (like Tailwind or Bootstrap). Instead, we wrote clean, modular CSS using the **BEM (Block, Element, Modifier)** naming convention.
    *   Powered by a dedicated **Design Token System** (`index.css` variables) defining the color scheme, gradient formulas, font weights, and transition curves.
    *   Uses modern layout modules: **CSS Flexbox** for navigation and columns, and **CSS Grid** for cards and interactive galleries.
*   **Vanilla JavaScript (ES6+):** Utilized for lightweight DOM manipulation, interactive custom events, and smooth scroll behaviors without loading heavy libraries (like jQuery).
*   **Swiper JS (3D Coverflow Slider):** A highly customized touch-carousel plugin configured with a custom 3D Coverflow effect to animate key features cards dynamically on desktop and mobile screens.

---

## 🎨 Design Features & Interactive Micro-Animations

The user interface was designed to look premium, dynamic, and modern. Here's a breakdown of the key visual features built into the code:

### 1. The Smart Dynamic Header
*   **White State (Top of Page):** Features a clean white background with a large brand logo and a dual-block "Register Now" CTA button (incorporating a neat sliding gradient fill on hover).
*   **Scrolled State:** As you scroll down past $80\text{px}$, the header automatically compresses in height and shifts into a premium dark gradient overlay (`#000E38` to `#3F186A`) to maximize viewport real estate while maintaining high readability.
*   **Show/Hide Scroll Logic:** To give users an immersive viewing experience, the header intelligently slides off-screen upwards when scrolling down, and reappears instantly when scrolling back up.

### 2. Infinite Marquee visual grids
*   **Hero Visual Column:** On desktop viewports, there's an oval-card gallery displaying real-life student and school photography. This column runs on an infinite, seamless vertical scroll animation via CSS Translate. It automatically pauses when the cursor hovers over any card so parents can view the image clearly.
*   **Double-Row Logo Slider:** In the "Participating Schools" section, logo arrays scroll automatically in opposite directions (Row 1 slides left, Row 2 slides right) to create a lively, balanced visual rhythm.

### 3. Glassmorphism Enquire Form
*   An elegant overlay form built using `backdrop-filter: blur(16px)` and translucent borders (`rgba(255, 255, 255, 0.12)`) allowing the vibrant background gradients to shine through while keeping input fields highly readable.

### 4. Swiper JS 3D Coverflow Gallery
*   Used for the "What Makes This Exhibition a Must-Visit" section. It's configured to automatically compute depths, rotation modifiers (`rotate: 10`), and slide shadows (`slideShadows: true`) to deliver a gorgeous 3D deck-swiping effect.
*   **Fail-safe fallback:** The script contains a custom fallback handler that automatically downloads and boots up Swiper from an alternate CDN if the primary CDN fails to resolve.

---

## 📂 Project Structure

Here is how the project files are structured:

```bash
SRV-Media-Assement/
│
├── index.html           # Main page structure, inline JS, and scripts
├── index.css            # Core design tokens, layout definitions, and Hero styles
│
├── css/                 # Segmented CSS stylesheets
│   ├── choose-school.css # Grid styles for school categories
│   ├── footer.css       # Layout styles for office columns and social icons
│   ├── logos.css        # Animations & tracking for school logo marquee
│   ├── must-visit.css   # Coverflow Swiper container & controls styling
│   └── pre-schedule.css # Split-screen CTA section styling
│
└── assets/              # Static media files (logos, icons, and illustrations)
    ├── choose-school/   # Category cards assets
    ├── icons/           # Feature card vectors
    └── Mask group.png   # Primary brand logo
```

---

## ♿ Accessibility (A11y) & SEO Best Practices
We designed this page to be friendly to search engine bots, screen readers, and keyboard navigation alike:
*   **Keyboard Friendly:** Added a customized `.skip-link` allowing users to jump directly to the main content. Standard interactive focus borders (`:focus-visible`) have been customized to render a high-contrast outline (`--color-focus-ring`).
*   **Semantic Structure:** Strict heading levels (`h1`, `h2`, `h3`) prevent screen reader navigation confusion. 
*   **SEO Setup:** Includes a optimized `<title>` tag, clean `<meta name="description">` metadata, responsive viewport tags, and clean image attributes.

---

## 🚀 Running Locally
You don't need any complex build steps to run or edit this project! 

1.  Clone this repository to your local drive.
2.  Open `index.html` directly in any web browser, or launch it with a local server extension (like VS Code's **Live Server**) to support active hot-reloading.
3.  Enjoy exploring! Feel free to modify the design variables at the top of `index.css` to tweak colors and typography instantly across the entire page.
