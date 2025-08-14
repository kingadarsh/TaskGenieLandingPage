# TaskGenie: AI‑Powered Task Management & Roadmap Generator

**TaskGenie** is an intelligent task‑management web app that helps you plan, track, and complete goals efficiently. Whether you’re learning something new, shipping a project, or just want a clear, bite‑sized path to a result, TaskGenie generates a personalized roadmap and keeps you moving.

**Live demo:** [https://taskgenielandingpage.onrender.com](https://taskgenielandingpage.onrender.com)

---

## Table of Contents

* [Features](#features)
* [Architecture (Microservices)](#architecture-microservices)
* [Repositories](#repositories)
* [Screenshots](#screenshots)
* [Work in Progress](#work-in-progress)
* [Getting Started](#getting-started)

  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
  * [Environment Variables](#environment-variables)
  * [Run Locally](#run-locally)
* [How It Works](#how-it-works)
* [Contributing](#contributing)
* [Reporting Issues](#reporting-issues)
* [License](#license)
* [Contact](#contact)
* [Acknowledgments](#acknowledgments)

---

## Features

* **AI‑Generated Roadmaps**: Enter a goal (e.g., *“Learn Python”* or *“Build a portfolio site”*) and TaskGenie will craft a step‑by‑step, outcomes‑driven plan.
* **Task Breakdown & Timetable**: Large goals are decomposed into focused modules with suggested durations and an auto‑generated timetable.
* **Calendar Sync (Coming Soon)**: One‑click sync to Google Calendar to receive reminders, view schedules, and keep tasks in one place.

---

## Architecture (Microservices)

TaskGenie follows a **microservices** approach for clear separation of concerns, independent deployability, and simpler scaling.

```
┌──────────────────┐       REST / JSON        ┌──────────────────┐
│   Landing Page   │  ─────────────────────▶  │     Frontend     │
│ (Marketing Site) │                          │ (Web Application) │
└──────────────────┘                          └──────────────────┘
                                                    │
                                                    │ GraphQL/REST (internal)
                                                    ▼
                                           ┌──────────────────┐
                                           │     Backend      │
                                           │  (API Service)   │
                                           └──────────────────┘
                                                    │
                                                    ▼
                                         ┌────────────────────┐
                                         │ External Services  │
                                         │ • Gemini API       │
                                         │ • Google Calendar  │
                                         └────────────────────┘
```

* **Landing Page**: Lightweight site that describes TaskGenie, hosts the live demo link, and captures interest.
* **Frontend (Web App)**: User interface for creating goals, viewing roadmaps, and managing tasks.
* **Backend (API Service)**: Orchestrates roadmap generation via the Gemini API, exposes endpoints to the frontend, and (soon) handles Google Calendar sync.

> Each service lives in its own repository, enabling independent development, CI/CD, and deployment.

---

## Repositories

* **Backend** (API Service): [https://github.com/kingadarsh/TodoBackendFullStack](https://github.com/kingadarsh/TodoBackendFullStack)
* **Frontend** (Web App): [https://github.com/kingadarsh/TodoFrontEndFullStack](https://github.com/kingadarsh/TodoFrontEndFullStack)
* **Landing Page** (Marketing Site): [https://github.com/kingadarsh/TaskGenieLandingPage](https://github.com/kingadarsh/TaskGenieLandingPage)

> **Live Demo:** [https://taskgenielandingpage.onrender.com](https://taskgenielandingpage.onrender.com)

---

## Screenshots

<img width="1227" alt="Screenshot 2024-12-15 at 4 44 26 PM" src="https://github.com/user-attachments/assets/217a6c81-deaf-4177-bf18-efcd5ff00b20" />
<img width="1470" alt="Screenshot 2024-12-15 at 4 34 26 PM" src="https://github.com/user-attachments/assets/aad03802-9f13-44be-b7d9-b5e2a0d1ec60" />
<img width="1470" alt="Screenshot 2024-12-15 at 4 34 53 PM" src="https://github.com/user-attachments/assets/ccee2616-9cf7-4509-bfa5-36de59428758" />
<img width="1470" alt="Screenshot 2024-12-15 at 4 36 23 PM" src="https://github.com/user-attachments/assets/f946d06c-da1f-4822-a13f-dcd898bf2d5e" />
<img width="1470" alt="Screenshot 2024-12-15 at 4 36 47 PM" src="https://github.com/user-attachments/assets/650188d6-a450-4aff-a3e5-d60c44421d6b" />
<img width="1470" alt="Screenshot 2024-12-15 at 4 37 16 PM" src="https://github.com/user-attachments/assets/3503ed58-14b4-44e2-8569-9523c6db1b4a" />

---

## Work in Progress

### Google Calendar Integration

Under active development: connect TaskGenie timetables directly to **Google Calendar** to receive reminders and stay on schedule automatically.

---

## Getting Started

### Prerequisites

* **Node.js** ≥ 14
* **API Keys**

  * **Gemini API** – for generating personalized roadmaps
  * **Google Calendar API** – for upcoming calendar sync

### Installation

Clone the service you intend to run. For example, to run the main app (frontend) locally:

```bash
git clone https://github.com/yourusername/TaskGenie.git
cd TaskGenie
npm install
```

> For microservices development, clone the related service(s) from the repos listed above.

### Environment Variables

Create a `.env` file at the project root and add the following:

```bash
GEMINI_API_KEY=your_gemini_api_key
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
```

### Run Locally

Start the development server:

```bash
npm start
```

Your application should now be available at `http://localhost:3000`.

---

## How It Works

1. **Input Your Goal/Task** – e.g., *“Learn Web Development.”*
2. **Generate Roadmap** – The backend calls the Gemini API to create a structured, step‑by‑step plan.
3. **Task Breakdown** – The plan is split into modules with suggested durations and a timetable.
4. **Calendar Sync (Coming Soon)** – Sync your timetable to Google Calendar for reminders and tracking.

---

## Contributing

We love open‑source contributions! To get started:

1. **Fork** the repository you want to improve.
2. Create a feature branch: `git checkout -b feature/awesome-improvement`
3. Make your changes.
4. Commit: `git commit -m "feat: add awesome improvement"`
5. Push: `git push origin feature/awesome-improvement`
6. Open a **Pull Request**.

For larger changes, please open an issue first to discuss what you’d like to change.

---

## Reporting Issues

Found a bug or have a suggestion? Please open an **Issue** in the relevant repository.

---

## License

This project is licensed under the **MIT License**.

---

## Contact

* **Email**: [adarsh261201@gmail.com](mailto:adarsh261201@gmail.com)
* **Twitter**: [@adarsh\_kathriya](https://x.com/adarsh_kathriya)

---

## Acknowledgments

* **Gemini API** – for personalized roadmap generation.
* **Google Calendar API** – for upcoming calendar integration.
* **Render** – for providing free hosting for the live demo.
