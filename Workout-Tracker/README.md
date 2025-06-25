
````markdown
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
````

Install dependencies:

```bash
npm install
```

Create a `.env` file:

```env
JWT_KEY=your_jwt_secret_key
```

Run MongoDB (locally or with Atlas), then start the server:

```bash
node index.js
```

Server starts on **[http://localhost:3000](http://localhost:3000)** (or your specified port).

---

## 📂 Folder Structure

```
.
├── models/
│   ├── createUser.js       # User model + methods
│   ├── workOuts.js         # Workout model + operations
│   └── seedExercises.js    # Exercise list fetcher
├── views/                  # Static HTML frontend views
├── .env                    # JWT secret key
├── index.js                # Main server file
```

---

## 🔐 Authentication Flow

* `/signup` – Accepts name, username, password → stores hashed credentials
* `/login` – Verifies credentials → issues JWT → sets secure cookie
* Routes like `/dashboard` or `/api` are protected using JWT validation middleware
* Token expiration: 24 hours

---

## 📊 API Endpoints (Key)

| Endpoint                    | Method | Description                                |
| --------------------------- | ------ | ------------------------------------------ |
| `/signup`                   | POST   | Register a new user                        |
| `/login`                    | POST   | Login and receive token                    |
| `/api/users`                | GET    | Get current user info via token            |
| `/dashboard/create-workout` | POST   | Create a new workout                       |
| `/api/workouts`             | GET    | Get all workouts for user                  |
| `/api/schedules`            | GET    | Fetch scheduled workouts                   |
| `/api/report/frequency`     | GET    | Get monthly/yearly workout frequency       |
| `/api/report/volume`        | GET    | Get workout volume (reps × sets × weights) |
| `/api/report/classes`       | GET    | Breakdown of workouts into categories      |

---

## 📅 Reports Overview

* **Frequency**: Number of workouts grouped by `Month-Year`.
* **Volume**: For each workout, calculates:

  * Weighted Volume = sets × reps × weights
  * Repetition Volume = sets × reps
* **Categories**: Classifies exercises into:

  * Push / Pull / Legs / Core / Cardio / Full Body / Plyometrics

## 🤝 Contributing

Pull requests are welcome! Please open an issue first to discuss any changes you'd like to make.
