---
title: "Frost & Flourish: Artisan Baking Delivered"
description: A websited designed to sell products! Made by me and my friends! (Practice Project)
author: Francis Allen Mesa
date: 2025-07-23 10:18:00 +0800
categories: [Project]
tags: [Minor-Project, Web-Development]
math: true
mermaid: true
---
## What We Built  

A complete bakery management system with:  
- **User roles** (Admin vs Customer)  
- **Session-based cart system** (state management the old-school way)  
- **Product CRUD operations** (Create, Read, Update, Delete)  
- **Product catalog** with categories (Breads, Pastries, Cakes)  

### The Pain Points  
⚠ **Session management headaches** - Debugging `Session["Cart"]` serialization issues  
⚠ **Manual dependency management** - No built-in DI meant service classes everywhere  
⚠ **Web.config nightmares** - Endless XML tags for simple settings  

## Key Lessons Learned  

1. **State management is painful** - Sessions work but feel archaic compared to modern approaches  
2. **Separation of concerns matters** - Even without DI, we enforced clean layers  
3. **Razor is timeless** - The view engine still holds up well today  

## Would I Build This Again in Framework?  

Only if maintaining legacy systems. Modern .NET Core offers:  
- **Cleaner dependency injection**  
- **Environment-based configuration**  
- **Cross-platform support**  
- **Better performance**  

This project taught me both the value of understanding legacy systems and the importance of moving forward. While I appreciate what I learned, my new projects all use modern .NET!  
