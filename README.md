#  Todo App using React Context API

This project is a **simple Todo application** built using **React + Context API**.  
The main goal of this project is to understand **global state management in React** without using prop drilling.

This project was built as a **learning project** after watching a full Context API lecture and implementing it step by step.

---

##  Live Demo

🔗 https://Lazik-Latief.github.io/todo-context-api/

---

##  Project Overview

This Todo App allows users to:

- ➕ Add a new todo
- ✏️ Edit an existing todo
- ✅ Mark a todo as completed
- ❌ Delete a todo
- 🔄 Share todo data across components using Context API

The focus of this project is **logic and data flow**, not UI complexity.

---

##  Why Context API?

In React, passing data from one component to another using **props** becomes difficult when the app grows.  
This problem is called **prop drilling**.

 **Context API solves this problem** by providing a **global store** that any component can access directly.

In this project:
- Todos and related functions are stored in **Context**
- Components access data using a custom hook (`useTodo`)
- No props are passed unnecessarily

---

##  Project Structure
```
src/
│
├── contexts/
│ └── TodoContext.jsx → Global state & shared logic
│
├── components/
│ ├── TodoForm.jsx → Add new todo
│ └── TodoItem.jsx → Display, edit, delete todo
│
├── App.jsx → Wraps app with Context Provider
└── main.jsx → Entry point

```

---

## 🔑 Core Concepts Used

- React Components
- `useState` hook
- Context API
- `createContext`
- `useContext`
- Custom Hooks
- Controlled Inputs
- Event Handling
- Conditional Rendering

---

##  Context API Explanation 

### 1️⃣ Creating Context
`TodoContext` is created using `createContext()`  
It defines the structure of shared data:
- todos array
- functions like add, update, delete

---

### 2️⃣ Provider
`TodoProvider` wraps the application and **provides data** to all child components.

This is where:
- State (`todos`) lives
- Logic functions are defined

---

### 3️⃣ Custom Hook (`useTodo`)
Instead of using `useContext(TodoContext)` everywhere,  
a custom hook `useTodo()` is created for cleaner and reusable code.

---

##  Data Flow (How Everything Works)
User Action
↓
Component calls Context function
↓
Context updates state (todos)
↓
React re-renders UI automatically


### Example:
- User adds a todo in `TodoForm`
- `addTodo()` is called from Context
- Todos state updates
- `TodoItem` re-renders with updated data

---

##  Component Responsibilities

### 🔹 TodoForm.jsx
- Handles input field
- Manages local input state
- Calls `addTodo()` from Context

---

###  TodoItem.jsx
- Displays individual todo
- Allows editing todo text
- Toggles completed state
- Deletes todo using Context functions

---

##  Local Storage (Concept Learned)

Although not mandatory, this project helped understand how:
- Data can be stored in `localStorage`
- Todos can persist after page refresh
- State can be synced with browser storage

---

##  What I Learned From This Project

- How Context API works internally
- How to manage global state in React
- How components communicate without props
- How data flows between Context and components
- How to structure a React project properly
- How React automatically updates UI when state changes
- How to deploy a Vite + React app on GitHub Pages

---

##  Tech Stack

- React
- Vite
- JavaScript (ES6)
- Context API
- Tailwind CSS
- Git & GitHub
- GitHub Pages

---

##  Deployment

This project is deployed using **GitHub Pages** with:
- `vite.config.js` base configuration
- `gh-pages` package
- Production build (`dist` folder)

---

##  Final Notes

This project helped me build a **strong foundation in React state management**, especially using the **Context API**.  
I learned how to create a global state using `createContext` and share data across multiple components using a **Context Provider**, without relying on prop drilling.

Although this is a beginner-friendly project, it introduces **real-world React concepts** such as global state management, clean component structure, and predictable data flow, which are commonly used in production-level applications.
---

###  Author
**Lazik Latief**  
Frontend Developer (Learning React)




