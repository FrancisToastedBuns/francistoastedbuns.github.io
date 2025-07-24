---
title: "InkDialog: Branching Story System for Godot"
description: Dialog system templates for easier development!
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

![Dialog Demo](/assets/img/inkdialog-demo.gif){: .shadow .rounded-10 }  
*Seamlessly integrate Ink.js narratives into Godot with full branching, variables, and save/load support.*  

---

## **Key Features**  
- **🖋️ Ink.js Integration**: Parse `.ink` files directly into Godot’s dialog system.  
- **🌳 Branching Narratives**: Supports complex choices, knots, and stitches.  
- **🎭 Character Emotions**: Dynamic portraits with mood-based expressions.  
- **📜 Scrollable History**: Review past dialog (with choice backtracking).  
- **💾 Save/Load States**: Preserves story variables and progress.  

```gdscript
# Example: Loading an Ink story in Godot
var ink_story = load("res://addons/inkgd/runtime/story.gd").new()
ink_story.load_story(json_story)
var text = ink_story.continue()
```

---

## **Tech Stack**  
| Component          | Technology Used           |
| ------------------ | ------------------------- |
| **Game Engine**    | Godot 4.2                 |
| **Narrative**      | Ink.js (via inkgd plugin) |
| **UI**             | Godot’s Control nodes     |
| **Export Targets** | Web, PC, Mobile           |

---

## **How It Works**  
1. **Write Stories in Ink**:  
   ```ink
   === meeting_guard ===
   "Halt! Who goes there?"
   * [Lie] "I’m the king!" -> guard_laughs
   * [Truth] "Just a traveler." -> allow_passage
   ```
2. **Import to Godot**: The plugin converts `.ink` to JSON.  
3. **Render Choices**: Dynamically generate buttons from Ink branches.  

> **Why Ink?**  
> Industry-standard for narrative games (*"80 Days"*, *"Heaven’s Vault"*), with built-in branching logic.  
{: .prompt-info }

---

## **Code Snippets**  
### 1. **Choice Handling**  
```gdscript
func _on_Choice_pressed(index):
    ink_story.choose_choice_index(index)
    update_dialog()
```

### 2. **Variable Tracking**  
```gdscript
if ink_story.variables.get("knows_secret"):
    show_extra_dialog()
```

---

## **Use Cases**  
- Visual novels  
- RPG dialog systems  
- Interactive fiction tools  

**Demo**: [Web Export Playable Here](#) | **GitHub**: [inkgd Plugin Setup](#)  

---

## **Comparison to Alternatives**  
| Feature          | InkDialog | Godot Dialogic | Twine    |
| ---------------- | --------- | -------------- | -------- |
| **Ink Support**  | ✅ Yes     | ❌ No           | ✅ Yes    |
| **Live Preview** | ✅ Yes     | ✅ Yes          | ❌ No     |
| **Mobile Ready** | ✅ Yes     | ✅ Yes          | Web-only |

---

## **Roadmap**  
- [ ] **Voice Acting Hooks**: Sync with Ink tags (`<<voice src="...">>`).  
- [ ] **Auto-Type Effect**: Letter-by-letter text animation.  
- [ ] **Timed Choices**: Decisions that expire (e.g., "5 seconds to respond!").  

---

### **Screenshots**  
| Editor Integration                                | Branching Flow                                 |
| ------------------------------------------------- | ---------------------------------------------- |
| ![Editor](/assets/img/ink-editor.png){: .border } | ![Flow](/assets/img/ink-graph.png){: .border } |

---

**Pro Tip**: Use Ink’s **tags** (`#`) to trigger Godot signals for gameplay events:  
```ink
"I’ll help you." # QUEST_ACCEPTED
```

