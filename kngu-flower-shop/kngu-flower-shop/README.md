## Magical Flora - E-Commerce Storefront

A modern, responsive, single-page e-commerce website.

This project focuses on translating UI/UX design into clean, semantic HTML, leveraging utility-first CSS for rapid styling, and implementing Vanilla JavaScript to create interactive, state-driven user experiences without the overhead of heavy frontend frameworks.

---

## Quick Start (How to Run)

Because this project is built using native web technologies and the Tailwind CSS Play CDN, there are **no build steps or `npm` installations required**.

1. Download/Clone the repository.
2. Open the project folder in your code editor (e.g., VS Code).
3. Open `index.html` using a local server (like the **Live Server** extension in VS Code) to ensure JavaScript modules and local assets render correctly.
4. The site will launch at `http://127.0.0.1:5500/index.html`.

---

## Technologies Used

* **HTML5:** Semantic structuring and accessibility best practices.
* **Tailwind CSS (via CDN):** Utility-first styling for completely custom, responsive layouts (Flexbox, CSS Grid, absolute positioning) directly within the markup.
* **Vanilla JavaScript (ES6+):** DOM manipulation, state management, and event handling.
* **Unsplash / Shopify CDNs:** High-quality image placeholders and bulletproof vector payment icons.

---

## Core Features & JavaScript Logic

This Website goes beyond static HTML by incorporating several production-like interactive features:

### 1. Interactive Bouquet Builder (State Management)
Located in the "Craft Your Masterpiece" section, this widget mimics a complex e-commerce product customizer.
* **Dynamic Rendering:** Selecting a base (Roses, Tulips, Mixed) triggers a re-render of the available stem options.
* **State Tracking:** An internal `currentSelections` object tracks the exact quantity of each stem.
* **Strict Validation:** A `MAX_FLOWERS` constant enforces a strict 12-stem limit. Users are prevented from exceeding this limit via UI alerts.
* **Dynamic Pricing:** The "Add to Cart" button dynamically calculates the total price based on the individual cost of the selected stems.
* **Checkout Gate:** The Add to Cart button validates that exactly 12 stems have been selected before allowing a successful submission.

### 2. Auto-Rotating Hero Slider
* Utilizes CSS opacity transitions layered with JavaScript timing events (`setInterval`).
* Includes manual override controls (Next/Prev arrows) which automatically reset the interval timer (`clearInterval`) to prevent jarring jumps immediately after a user interaction.

### 3. Horizontal Product Gallery
* The "New Products" section utilizes CSS `snap-mandatory` and `overflow-x-auto` to create a touch-friendly swiping gallery for mobile.
* For desktop users, custom Vanilla JS arrows utilize the native `scrollBy({ behavior: 'smooth' })` API to navigate the gallery cleanly while hiding the default browser scrollbar via custom CSS.

### 4. UI Modals & Drawers
* Includes a **Login/Register Modal** and a **Sliding Cart Drawer**.
* Controlled via JS toggling of Tailwind utility classes (`hidden`, `translate-x-full`).
* Features backdrop-blur overlays with event listeners that allow users to close the modals by clicking outside the container.

---

## Design & Layout Decisions

* **Bento Grid Layout:** The "Featured Items" section utilizes a modern CSS Grid layout, spanning specific items across multiple columns/rows to break away from standard uniform grids.
* **Responsive Design:** Extensively uses Tailwind's mobile-first breakpoints (`md:`, `lg:`) to ensure the layout gracefully degrades from a multi-column desktop view to a stacked mobile view.
* **Typography:** Combines *Playfair Display* (Serifs for elegant headings) and *Inter* (Sans-serif for highly legible body copy and UI elements) to match the boutique aesthetic.

---

## Folder Structure

/kngu-flower-shop
├── index.html       # Main HTML document containing markup and JS logic
├── style.css        # Custom CSS for scrollbar hiding and minor overrides
├── README.md        # Project documentation
└── .gitignore       # Git configuration