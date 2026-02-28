# 🚀 Frontend Mentor - Social proof section solution

This is a solution to the [Social proof section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/social-proof-section-6e0qTv_bA).  
The goal of this challenge was to build a responsive testimonial section following a mobile-first approach and matching the provided design as closely as possible.

---

## 🎬 Demo

![](./docs/demo.gif)

---

## ✨ Overview

This project focuses on layout precision, responsive design, and clean CSS architecture using semantic HTML and modern CSS features.

---

## 🎯 The challenge

Users should be able to:

- View the optimal layout for the section depending on their device's screen size

---

## 📸 Screenshots

### 📱 Mobile

![](./docs/mobile-default.avif)

### 📱 Tablet

![](./docs/tablet-default.avif)

### 💻 Desktop

![](./docs/desktop-default.avif)

### 💻 Desktop - Interaction states

![](./docs/desktop-interaction.avif)

---

## 🔗 Links

- 🌎 [Live site](https://vimpdev.github.io/fem-05-social-proof-section/)
<!-- - 👩‍💻 [Frontend Mentor solution](https://your-solution-url.com) -->

---

## 🛠️ Built with

- Semantic HTML5
- CSS custom properties
- CSS Grid (with `grid-template-areas`)
- Flexbox
- Mobile-first workflow
- Variable font (`@font-face` with weight range `100 - 900`)
- Logical properties (`inline-size`, `block-size`)
- Modern media query syntax (`@media (width >= ...)`)

---

## 🧠 Architecture & Technical Decisions

### 1️⃣ Variable font implementation

The project uses a locally hosted variable font:
```js
@font-face {
  font-family: 'League Spartan';
  src: url('./../assets/fonts/LeagueSpartan.woff2') format('woff2');
  font-weight: 100 900;
  font-display: swap;
}
```
This allows flexible weight usage without importing multiple font files.

### 2️⃣ Layout strategy
- Mobile-first base layout
- CSS Grid with named areas:
  ```js
  grid-template-areas:
    "intro"
    "ratings"
    "testimonials";
  ```
- Desktop rearranges layout into two columns
- Subtle staggered positioning implemented with:
  ```js
  .rating:nth-of-type(2) {
    transform: translateX(3.9rem);
  }
  ```
  and
  ```js
  .testimonial:nth-of-type(3) {
    transform: translateY(2.55rem);
  }
  ```
This replicates the design’s visual offset effect.

### 3️⃣ Background images (shorthand practice)

Two decorative background images are applied using background shorthand in mobile and replaced in desktop via media queries.
```js
background:
  url(...) no-repeat top left,
  url(...) no-repeat bottom right var(--white);
```

### 4️⃣ Utility class
The project includes a reusable accessibility utility:
```js 
.visually-hidden
```
Used to keep content accessible to screen readers while hiding it visually.

### 5️⃣ Semantic quotes with pseudo-elements

Instead of hardcoding quotation marks in HTML, they are generated using:
```js
.testimonial__quote::before { content: '\201c'; }
.testimonial__quote::after { content: '\201d'; }
```
This keeps markup clean and semantic.

### 6️⃣ Accessibility improvements (beyond the challenge)

The attribution links include:
- :focus-visible
- Hover underline animation
- Visible keyboard focus state

These were intentionally added even though they were not required in the design.

---

## 📈 What I learned

- Better control of layout using `grid-template-areas`
- Practical use of variable fonts
- Creating subtle visual hierarchy with transform instead of margin hacks
- Implementing accessible focus states properly

---

## 🤖 AI Collaboration

AI tools were used to:

- Reviewing architectural decisions
- Discussing semantic structure improvements
- Refining commit message conventions
- Improving README structure and documentation clarity

The goal was not code generation, but architectural discussion and refinement.

## 👤 Author

- Frontend Mentor - [@vimpdev](https://www.frontendmentor.io/profile/vimpdev)