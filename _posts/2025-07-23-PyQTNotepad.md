---
title: "PyQt Notepad: A Windows-Style Text Editor"
description: A lightweight, customizable text editor built with Python and PyQt.
author: cotes
date: 2025-07-23 10:18:00 +0800
categories: [Blogging, ProjectPortfolio]
tags: [typography]
math: true
mermaid: true
image:
  path: public/2.jpg
  lqip: data:image/webp;base64,UklGRpoAAABXRUJQVlA4WAoAAAAQAAAADwAABwAAQUxQSDIAAAARL0AmbZurmr57yyIiqE8oiG0bejIYEQTgqiDA9vqnsUSI6H+oAERp2HZ65qP/VIAWAFZQOCBCAAAA8AEAnQEqEAAIAAVAfCWkAALp8sF8rgRgAP7o9FDvMCkMde9PK7euH5M1m6VWoDXf2FkP3BqV0ZYbO6NA/VFIAAAA
  alt: Responsive rendering of Chirpy theme on multiple devices.
---

![PyQt Notepad Screenshot](/assets/img/notepad-demo.png){: .shadow .rounded-10 w='800' h='450' }  
*A lightweight, customizable text editor built with Python and PyQt.*  

## **Features**  
✔ **Familiar Interface** – Mirrors classic Windows Notepad with added enhancements.  
✔ **Rich Text Editing** – Supports plain text (.txt) and basic formatting (bold, italics, underline).  
✔ **Customizable UI** – Dark/light mode, font size, and theme options.  
✔ **Essential Tools** – Find/replace, undo/redo, print, and file encoding (UTF-8, ASCII).  
✔ **Cross-Platform** – Runs on Windows, Linux, and macOS.  

```python
# Example: Core PyQt setup
from PyQt6.QtWidgets import QApplication, QMainWindow, QTextEdit

class Notepad(QMainWindow):
    def __init__(self):
        super().__init__()
        self.text_edit = QTextEdit()
        self.setCentralWidget(self.text_edit)
        self.setWindowTitle("PyQt Notepad")
```

---

## **Tech Stack**  
| Component         | Technology Used          |
| ----------------- | ------------------------ |
| **GUI Framework** | PyQt6 (Qt for Python)    |
| **Language**      | Python 3.10+             |
| **Tools**         | Qt Designer, PyInstaller |

---

## **How It Compares to Windows Notepad**  
| Feature         | Windows Notepad | PyQt Notepad |
| --------------- | --------------- | ------------ |
| Dark Mode       | ❌ No            | ✅ Yes        |
| Text Formatting | ❌ No            | ✅ Basic      |
| Cross-Platform  | ❌ Windows-only  | ✅ Yes        |
| Open Source     | ❌ No            | ✅ Yes        |

> **Why PyQt?**  
> PyQt offers native-looking UIs and granular control over widgets, perfect for replicating (and improving) classic apps.  
{: .prompt-tip }  

---

## **Installation**  
1. Clone the repo:  
   ```bash
   git clone https://github.com/yourusername/pyqt-notepad.git
   ```
2. Install dependencies:  
   ```bash
   pip install PyQt6
   ```
3. Run the app:  
   ```bash
   python notepad.py
   ```

---

## **Future Roadmap**  
- [ ] Add syntax highlighting for code.  
- [ ] Integrate cloud save (Google Drive/Dropbox).  
- [ ] Plugin system for extensions (e.g., Markdown support).  

**Download**: [Get the .exe/.dmg here](#) | **GitHub**: [Source Code](#)  

---

### **Screenshot Gallery**  
| Light Mode                                          | Dark Mode                                         |
| --------------------------------------------------- | ------------------------------------------------- |
| ![Light](/assets/img/notepad-light.png){: .border } | ![Dark](/assets/img/notepad-dark.png){: .border } |

---

This keeps the **Chirpy theme’s** clean layout while highlighting your project’s technical strengths. Customize the screenshots/links, and it’s ready to deploy!  

Need tweaks? For example:  
- A "heroic" Tagalog name for the app (e.g., *"SulatPad"* from *"sulat"* = to write)?  
- More emphasis on specific features?
