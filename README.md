# 🌐 OR-Master: Operations Research Interactive Learning Platform

> A comprehensive, gamified, self-contained educational web application and solver suite for **Operations Research (Modules 1 & 2)**.

---

## 🚀 Features

- **Gamified Taskbar & Progress Tracker**: Syllabus completion % and XP points stored automatically in `localStorage`.
- **Module 1 (Linear Programming)**: Complete coverage of Model Formulation, 2D Graphical Method & 4 Edge Cases, Standard Simplex, Big-M (Penalty Cost), and Two-Phase Method.
- **Module 2 (Networks & Sequencing)**: Complete coverage of Transportation Problem (NWCR, LCM, VAM, MODI $u-v$), Assignment Problem (Hungarian Algorithm, Max, Prohibited, TSP), and Job Sequencing (Johnson's 2/3 machines & 2-Job Graphical Method).
- **Interactive Stepper Solvers**:
  - Step-by-step Simplex Multi-Tableau Stepper with highlighted pivot rows, columns, and elements.
  - VAM & MODI Transportation Visualizer.
  - Hungarian Matrix Reducer.
  - Gantt Chart Sequencing Visualizer.
- **25+ Zero-Pen Mental Puzzles**: Concept-building flashcards designed for zero-paper mental reasoning.
- **Exam Diagnostic Quizzes**: Self-assessment multiple-choice quizzes with instant grading and explanations.
- **Exam Master Cheat-Sheet**: 1-page quick formula and trap reference.

---

## 📦 How to Run Locally

Simply double-click `index.html` or open it in any modern web browser (Chrome, Edge, Firefox, Safari). Zero installation required!

---

## ☁️ How to Deploy to Vercel in 1 Minute

### Method 1: Using Vercel CLI
```bash
npx vercel
```

### Method 2: Via GitHub & Vercel Dashboard
1. Create a new GitHub repository: `or-master-platform`.
2. Push the files in this directory to your repository:
   ```bash
   git init
   git add .
   git commit -m "Initial commit of OR-Master platform"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/or-master-platform.git
   git push -u origin main
   ```
3. Go to [vercel.com](https://vercel.com) &rarr; Click **"Add New Project"** &rarr; Select your repository &rarr; Click **"Deploy"**.
4. Your site will be live instantly with global CDN acceleration and HTTPS!
