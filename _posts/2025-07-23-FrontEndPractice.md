---
title: "Frontend Playground: Interactive Project Gallery"
description: A portfolio to showcase all the projects I practiced on!
author: cotes
date: 2025-07-23 10:18:00 +0800
categories: [Blogging, ProjectPortfolio]
tags: [typography]
math: true
mermaid: true
---

<!-- ![Portfolio Preview](/assets/img/portfolio-demo.gif){: .shadow .rounded-10 w='100%' }  
*A dynamic showcase of web experiments, frameworks, and UI designs.* -->

---

## **Featured Projects**
### 1. **Neon Calculator (React + CSS Animations)**  
   - **Tech**: React Hooks, Framer Motion  
   - **Demo**: [Live Link](#)  
   - **Code**: [GitHub](#)
   {% raw %}
   ```javascript
   // Animated button component
   <motion.button whileHover={{ scale: 1.1 }} whileTap={{ scale: 0.9 }}>
   {buttonLabel}
   </motion.button>
   ```
   {% endraw %}

### 2. **Weather Dashboard (Vue + API Integration)**  
   - **Tech**: Vue 3, OpenWeatherMap API  
   - **Features**: Geolocation, 5-day forecast graphs  
   ![Weather App](/assets/img/weather-demo.jpg){: .w-75 .border}

### 3. **Pixel Art Editor (Vanilla JS Canvas)**  
   - **Tech**: HTML5 Canvas, Web Storage  
   - **Interactive**: Try it [here](#)  

---

## **Tech Stack Showcase**
<div class="tech-grid" markdown="1">
| Category       | Tools Used                         |
| -------------- | ---------------------------------- |
| **Frameworks** | React, Vue, Svelte                 |
| **Styling**    | Tailwind, SCSS, CSS Grid/Animation |
| **APIs**       | REST, GraphQL, Firebase            |
| **Testing**    | Jest, Cypress                      |
</div>

---

## **Interactive Elements**
- **Project Filter**:  
  ```html
  <!-- Filter by tech -->
  <button @click="filterProjects('react')" 
          class="filter-btn" data-active="true">
    React
  </button>
  ```
- **Live Code Previews**: Embedded CodePens/JSFiddles  
- **Dark Mode Toggle**: Persists via `localStorage`

---

## **Design Philosophy**
> "Mobile-first, accessible components with <br> 
> **90+ Lighthouse scores** across PWA metrics."
{: .prompt-tip }

---

## **Get the Code**
```bash
# Clone portfolio source
git clone https://github.com/yourusername/frontend-portfolio.git
```
**Template Available**: [Use this design](#) (MIT Licensed)

---

### **Why This Stands Out**
- **Micro-interactions**: Hover animations on every card  
- **SEO Optimized**: Auto-generated project schema markup  
- **CMS Ready**: Netlify CMS integration for easy updates  


