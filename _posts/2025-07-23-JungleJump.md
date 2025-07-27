---
title: "Jungle Jump: A Wild 2D Platformer Adventure"
description: It is a Godot styled mario game!
author: Francis Allen Mesa
date: 2025-07-23 10:18:00 +0800
categories: [Project]
tags: [Major-Project, Game-Development]
pin: true
math: true
mermaid: true
image:
  path: public/junglejump/junglejump.png
  lqip: data:image/webp;base64,UklGRpoAAABXRUJQVlA4WAoAAAAQAAAADwAABwAAQUxQSDIAAAARL0AmbZurmr57yyIiqE8oiG0bejIYEQTgqiDA9vqnsUSI6H+oAERp2HZ65qP/VIAWAFZQOCBCAAAA8AEAnQEqEAAIAAVAfCWkAALp8sF8rgRgAP7o9FDvMCkMde9PK7euH5M1m6VWoDXf2FkP3BqV0ZYbO6NA/VFIAAAA
  alt: Responsive rendering of Chirpy theme on multiple devices.
---


---

![Jungle Jump Gameplay](/public/junglejump/junglejump.gif){: .shadow .rounded-10 w='800' h='450' }  
*Dodge vines, leap over pits, and outrun enemies in this fast-paced jungle romp!*  

---


## **Game Features**  
- 🎮 **Classic Platforming** – Run, jump, and stomp enemies in true Mario style.  
- 🌴 **Lush Pixel Art** – Vibrant jungle environments with animated foliage.  
- 🐍 **Dangerous Wildlife** – Sneaky snakes, angry gorillas, and quicksand pits.  
- 🏆 **Collectibles** – Golden fruits for points, hidden power-ups (double jump, speed boost).  
- 🎵 **Catchy Chiptune OST** – Retro-inspired soundtrack.  

```gdscript
# Example: Player jump mechanic in Godot
extends CharacterBody2D

var jump_force = -600
var gravity = 1200

func _physics_process(delta):
    velocity.y += gravity * delta
    if Input.is_action_just_pressed("jump") and is_on_floor():
        velocity.y = jump_force
    move_and_slide()
```

---

| Component | Technology Used |
|-----------|-----------------|
| **Engine** | Godot 4.2 |
| **Art** | Aseprite (Pixel Art) |
| **Sound** | BFXR (SFX), Bosca Ceoil (Music) |
| **Export Targets** | Windows/Linux, Web(WIP), Android (WIP)|

| Feature | Super Mario | Jungle Jump |
|---------|-------------|-------------|
| **Setting** | Mushroom Kingdom | Untamed Jungle |
| **Art Style** | Cartoony | Pixel Art + Parallax Scrolling |

{::nomarkdown}
<blockquote class="prompt-info">
  <strong>Why Godot?</strong><br>
  Lightweight, open-source, and perfect for indie 2D platformers with built-in physics.
</blockquote>
{:/nomarkdown}

---

## **Development Highlights**  
### **Challenges Solved**  
1. **Smooth Wall Jumps** – Tweaked Godot’s `move_and_slide()` for better friction control.  
2. **Enemy AI** – Used `RayCast2D` for patrol paths and player detection.  
3. **Parallax Backgrounds** – Layered scrolling for depth (see code snippet below).  

```gdscript
# Parallax Layer Script
extends ParallaxLayer
@export var scroll_speed = -50

func _process(delta):
    motion_offset.x += scroll_speed * delta
```

---

## **Roadmap**  
- [ ] **Multiplayer Mode** – Race a friend locally.  
- [ ] **Integrated Dialogue** – Let players talk to interesting NPCs.  
- [ ] **New Biomes** – Volcanic caves, treetop villages.  

