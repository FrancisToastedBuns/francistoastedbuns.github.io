---
title: "Code Quest: A Turn-Based Android Game Teaching Java Fundamentals"
description: Learn Java through interactive turn-based gameplay
author: Francis Allen Mesa
date: 2025-07-23 10:18:00 +0800
categories: [Project]
tags: [Major-Project, Game-Development]
pin: true
math: true
mermaid: true
image:
  path: public/codequest/codequest.png
  lqip: data:image/webp;base64,UklGRpoAAABXRUJQVlA4WAoAAAAQAAAADwAABwAAQUxQSDIAAAARL0AmbZurmr57yyIiqE8oiG0bejIYEQTgqiDA9vqnsUSI6H+oAERp2HZ65qP/VIAWAFZQOCBCAAAA8AEAnQEqEAAIAAVAfCWkAALp8sF8rgRgAP7o9FDvMCkMde9PK7euH5M1m6VWoDXf2FkP3BqV0ZYbO6NA/VFIAAAA
  alt: Responsive rendering of Chirpy theme on multiple devices.
---

![Code Quest Gameplay](public/codequest/codequest.gif){: .shadow .rounded-10 w='800' h='450' }  
*Code Quest: Learn Java through interactive turn-based gameplay.*  

## **About the Project**  
**Code Quest** is an **educational Android game** designed to teach **Java programming fundamentals** through:  
- 🎮 **Turn-based gameplay** with coding challenges.  
- 📝 **Quizzes, drag-and-drop mini-games**, and quests.  
- 💡 **Real Java syntax** parsing using the **Roslyn compiler** (C#).  
- 📖 **Rich dialogue** to guide learners.  

### **Key Features**  
1. **Interactive Java Lessons**  
   - Players write code to solve in-game puzzles.  
   - Immediate feedback via a **mimicked Java compiler** (parsed from text files).  
2. **Diverse Challenges**  
   - Multiple-choice quizzes.  
   - Code-block sequencing (drag-and-drop).  
   - Debugging tasks.  
3. **Engaging Narrative**  
   - Story-driven quests to motivate learning.  

---

## **Tech Stack** 

| Component         | Technology Used         |
| ----------------- | ----------------------- |
| **Game Engine**   | Unity (C#)              |
| **Java Compiler** | Roslyn + custom parsing |
| **UI/UX**         | Unity UI Toolkit        |
| **Data Storage**  | JSON/text files         |

```csharp  
// Example: Parsing Java code from text files  
public void ParseJavaCode(string filePath) {  
  string code = File.ReadAllText(filePath);  
  
}  
```  
*How Code Quest mimics a Java environment.*  

---

## **How It Works**  
1. **Players encounter a coding problem** (e.g., fix a loop).  
2. **Solve it via**:  
   - Typing code directly.  
   - Removing the syntax that is causing the problem.
3. **The game "compiles" their answer** using Roslyn and gives feedback.  

> **Why Java?**  
> Java’s strict syntax makes it ideal for teaching core programming concepts like OOP and logic structures, in addition, it was the most popular language used to teach grade 11 and 12 students.  
{: .prompt-info }  

---

## **Challenges & Solutions**  

| Challenge                  | Solution Implemented              |
| -------------------------- | --------------------------------- |
| Mimicking Java compilation | Used Roslyn + custom parsers      |
| Engaging non-coders        | Added RPG-like quests & story     |
| Cross-platform performance | Optimized Unity build for Android |
