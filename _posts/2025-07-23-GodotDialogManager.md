---
title: "InkDialog: Branching Story System for Godot"
description: Dialog system templates for easier development!
author: Francis Allen Mesa
date: 2025-07-23 10:18:00 +0800
categories: [Project]
tags: [Major-Project, Game-Development]
pin: true
math: true
mermaid: true
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
|--------------------|---------------------------|
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

<!-- **Demo**: [Web Export Playable Here](#) | **GitHub**: [inkgd Plugin Setup](#)   -->

---
## **Why create a new dialogue manager? Why not use existing plugins?**
I want my own DialogManager because I need complete control over its functionality to truly grasp how dialogue systems work at a fundamental level. By rebuilding a plugin from scratch, I'll gain deep understanding of module creation and system architecture that using pre-made solutions can't provide. In addition, using ink helps me to essentially reuse existing dialogs just incase I want to change game engines.

| Feature          | InkDialog | Godot Dialogic | Twine    |
|------------------|-----------|----------------|--------|
| **Ink Support**  | ✅ Yes     | ❌ No           | ✅ Yes    |
| **Live Preview** | ✅ Yes     | ✅ Yes          | ❌ No     |
| **Mobile Ready** | ✅ Yes     | ✅ Yes          | Web-only |

---

## **Roadmap**  
- [ ] **Voice Acting Hooks**: Sync with Ink tags (`<<voice src="...">>`).  
- [ ] **Auto-Type Effect**: Letter-by-letter text animation.  
- [ ] **Timed Choices**: Decisions that expire (e.g., "5 seconds to respond!").  


