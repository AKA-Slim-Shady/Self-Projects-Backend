# 🏋️ Fitness Workout Tracker

A full-stack fitness workout tracker built using **Node.js**, **Express**, **MongoDB**, and **JWT authentication**. This application helps users manage their workouts, schedule sessions, and analyze performance data like frequency and volume. It's a feature-rich, privacy-focused platform for fitness enthusiasts and beginners alike.

[📌 Project Idea Reference (Roadmap.sh)](https://roadmap.sh/projects/fitness-workout-tracker)

---

## 🚀 Features

- 🔐 User Authentication with **JWT** and password hashing using **bcrypt**
- 📝 Workout creation, update, and deletion
- 📅 Workout scheduling with date/time support
- 📊 Reports for:
  - Workout frequency (monthly/yearly)
  - Volume tracking (reps & weights)
  - Exercise class breakdown (Push, Pull, Legs, Core, etc.)
- 📦 Exercise database (pre-seeded)
- 📈 User-specific workout history
- 🍪 Uses cookies for secure token storage
- 📄 Clean HTML views for login, signup, dashboard, etc.

---

## 🧱 Tech Stack

- **Backend**: Node.js, Express.js
- **Database**: MongoDB (Mongoose ORM)
- **Authentication**: JSON Web Tokens (JWT), bcrypt
- **Frontend**: HTML (served as static views)
- **Other**: dotenv, cookie-parser

---

## 🔧 Installation

Clone the repo:

```bash
git clone https://github.com/yourusername/fitness-workout-tracker.git
cd fitness-workout-tracker
