---
title: "Mystic Quest: A Java GUI Text Adventure"
description: A nostalgic choose-your-own-adventure game with rich GUI storytelling.
author: cotes
date: 2025-07-23 10:18:00 +0800
categories: [Blogging, ProjectPortfolio]
tags: [typography]
pin: true
math: true
mermaid: true
image:
  path: /assets/lib/public/mockimage.jpg
  lqip: data:image/webp;base64,UklGRpoAAABXRUJQVlA4WAoAAAAQAAAADwAABwAAQUxQSDIAAAARL0AmbZurmr57yyIiqE8oiG0bejIYEQTgqiDA9vqnsUSI6H+oAERp2HZ65qP/VIAWAFZQOCBCAAAA8AEAnQEqEAAIAAVAfCWkAALp8sF8rgRgAP7o9FDvMCkMde9PK7euH5M1m6VWoDXf2FkP3BqV0ZYbO6NA/VFIAAAA
  alt: Responsive rendering of Chirpy theme on multiple devices.
---

![Gameplay Screenshot](/assets/img/mystic-quest-demo.png){: .shadow .rounded-10 w='700' }  
*A nostalgic choose-your-own-adventure game with rich GUI storytelling.*  

---

## **Features**  
- 📖 **Immersive Narrative**: Branching storylines with 50+ decision points.  
- 🖼️ **Sleek Java GUI**: Swing-based interface (themes: Dark/Light).  
- 🎭 **Character System**: Stats (Strength, Wisdom) that affect outcomes.  
- 🔍 **Interactive Elements**: Clickable inventory, auto-save/load.  
- 🎵 **Atmospheric Sound**: Background music and SFX.  

```java
// Example: GUI Window with Swing
JFrame frame = new JFrame("Mystic Quest");
frame.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
frame.add(new GamePanel()); // Custom panel for story/inventory
frame.pack();
frame.setVisible(true);
```

---

## **Tech Stack**  
| Component         | Technology Used       |
| ----------------- | --------------------- |
| **Language**      | Java 17+              |
| **GUI Framework** | Java Swing            |
| **Audio**         | `javax.sound.sampled` |
| **Build Tool**    | Maven/Gradle          |

---

## **How It Works**  
1. **Player reads story segments** in a scrollable text pane.  
2. **Choices appear as buttons** (e.g., "Open the chest" / "Run away").  
3. **Game state updates** dynamically (health, inventory, story flags).  

> **Why Java Swing?**  
> Lightweight, native look, and perfect for turn-based narrative games.  
{: .prompt-tip }  

---

## **Code Snippets**  
### 1. **Choice Handling**  
```java
// Button action listener
choiceButton.addActionListener(e -> {
    player.addItem("Rusty Key");
    storyPanel.appendText("\nYou found a key!");
});
```

### 2. **Inventory System**  
```java
// Inventory GUI (JList)
DefaultListModel<String> model = new DefaultListModel<>();
model.addElement("Sword");
model.addElement("Healing Potion");
JList<String> inventoryList = new JList<>(model);
```

---

## **Download & Play**  
- **JAR File**: [Download here](#)  
- **Source Code**: [GitHub](#)  
- **Requires**: Java 17+ installed.  

```bash
# Run from terminal
java -jar MysticQuest.jar
```

---

## **Screenshots**  
| Story Scene                                              | Inventory                                                  |
| -------------------------------------------------------- | ---------------------------------------------------------- |
| ![Story](/assets/img/mystic-quest-story.png){: .border } | ![Inventory](/assets/img/mystic-quest-inv.png){: .border } |

---

## **Future Plans**  
- [ ] Add ASCII art for key scenes.  
- [ ] Export stories to JSON for modding.  
- [ ] Steam Greenlight (with bundled JRE).  

---

### **Tagalog Twist?**  
- **Localized Title**: *"Paglalakbay ng Bayani"* (Hero’s Journey)  
- **Filipino Themes**: Incorporate *aswang* myths or *barangay* settings.  

---

**Pro Tip**: Use `JSplitPane` for a classic text-adventure layout (story on top, choices/inventory below). Let me know if you’d like help with specific Swing components!
