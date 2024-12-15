# TaskGenie: AI-Powered Task Management and Roadmap Generator

TaskGenie is an intelligent task management web application that helps you plan and complete your tasks efficiently. Whether you're learning something new, working on a project, or just need a clear roadmap to reach your goals, TaskGenie is here to help.

[Check out the live version here: TaskGenie](https://taskgenielandingpage.onrender.com)

## Screenshot
<img width="1227" alt="Screenshot 2024-12-15 at 4 44 26 PM" src="https://github.com/user-attachments/assets/217a6c81-deaf-4177-bf18-efcd5ff00b20" />
<img width="1470" alt="Screenshot 2024-12-15 at 4 34 26 PM" src="https://github.com/user-attachments/assets/aad03802-9f13-44be-b7d9-b5e2a0d1ec60" />
<img width="1470" alt="Screenshot 2024-12-15 at 4 34 53 PM" src="https://github.com/user-attachments/assets/ccee2616-9cf7-4509-bfa5-36de59428758" />
<img width="1470" alt="Screenshot 2024-12-15 at 4 36 23 PM" src="https://github.com/user-attachments/assets/f946d06c-da1f-4822-a13f-dcd898bf2d5e" />
<img width="1470" alt="Screenshot 2024-12-15 at 4 36 47 PM" src="https://github.com/user-attachments/assets/650188d6-a450-4aff-a3e5-d60c44421d6b" />
<img width="1470" alt="Screenshot 2024-12-15 at 4 37 16 PM" src="https://github.com/user-attachments/assets/3503ed58-14b4-44e2-8569-9523c6db1b4a" />


## Features

* **AI-Generated Roadmaps**: Input your goals (e.g., "Learn Python" or "Finish a project"), and TaskGenie will automatically create a step-by-step roadmap.
* **Task Breakdown**: The app divides your large tasks into smaller, manageable modules and generates a timetable for your activities.
* **Google Calendar Integration (Coming Soon)**: Soon, you'll be able to sync your generated timetable directly with Google Calendar to get reminders for your tasks and have everything in one place!

## Work In Progress

### Google Calendar Integration
Currently, the Google Calendar sync feature is under construction. This feature will allow users to directly integrate their generated timetable with Google Calendar, receive task reminders, and keep everything up to date automatically.

## Getting Started

### Prerequisites

Before you run this project locally, make sure you have:
* **Node.js** installed on your computer (version 14 or later is recommended).
* **API Keys**:
   * **Gemini API**: Required to generate personalized roadmaps.
   * **Google Calendar API**: Required for the future calendar integration.

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/TaskGenie.git
cd TaskGenie
```

2. Install the necessary dependencies:
```bash
npm install
```

3. Set up environment variables by creating a `.env` file in the root directory and adding your API keys:
```makefile
GEMINI_API_KEY=your_gemini_api_key
GOOGLE_CLIENT_ID=your_google_client_id
GOOGLE_CLIENT_SECRET=your_google_client_secret
```

4. Start the development server:
```bash
npm start
```

Your application will be available at `http://localhost:3000`.

## How It Works

1. **Input Your Goal/Task**: You enter a task or goal you want to accomplish, such as "Learn Web Development."
2. **Generate Roadmap**: TaskGenie uses the Gemini API to create a structured, step-by-step roadmap.
3. **Task Breakdown**: The roadmap is broken down into manageable tasks/modules, along with estimated time frames.
4. **Google Calendar Sync (Coming Soon)**: The timetable can be synced with Google Calendar for automatic reminders and task tracking (this feature is still under development).

## Contributing

We encourage open-source contributions! If you want to improve TaskGenie, feel free to fork the repo and submit a pull request.

### How to Contribute:
1. Fork the repository.
2. Create a new branch: `git checkout -b new-feature`
3. Make your changes.
4. Commit your changes: `git commit -m 'Add new feature'`
5. Push to your forked repository: `git push origin new-feature`
6. Open a pull request.

## Reporting Issues

If you find bugs or have any suggestions, please open an issue.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

## Contact

For questions or collaboration opportunities, feel free to contact us:
* **Email**: adarsh261201@gmail.com
* **Twitter**: @adarsh_kathriya

## Acknowledgments

* **Gemini API**: For helping us generate personalized roadmaps.
* **Google Calendar API**: For upcoming integration.
* **Render** : For provnding us free hosting service.
