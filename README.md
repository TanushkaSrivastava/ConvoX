# MeetX ❤️ — Video Conferencing Application

MeetX is a web-based video conferencing application designed to connect people through real-time video and audio communication. It provides a simple interface for joining meetings, communicating with other participants, sharing screens, and exchanging chat messages.

## ✨ Features

- **User Authentication:** Register and log in using a username and password.
- **Video Conferencing:** Connect with other participants using WebRTC.
- **Audio and Video Controls:** Enable or disable your microphone and camera during a meeting.
- **Meeting Rooms:** Join a meeting using a meeting code or room URL.
- **Screen Sharing:** Share your screen with other participants.
- **Real-Time Chat:** Send and receive messages during meetings.
- **Meeting History:** View previously joined meetings.
- **Protected Routes:** Restrict access to authenticated users.
- **Responsive Interface:** A user-friendly interface for navigating the application.

## 🛠️ Tech Stack

### Frontend
- React.js
- JavaScript
- Material UI (MUI)
- React Router DOM
- Axios
- Socket.IO Client
- CSS Modules

### Backend and Communication
- Node.js
- Express.js
- Socket.IO
- WebRTC
- MongoDB

*The backend technologies listed above reflect the project's intended architecture and the available frontend integrations; verify the backend implementation before claiming every component is fully configured.*

## 📂 Project Structure

```text
MeetX/
├── public/
│   ├── index.html
│   ├── favicon.ico
│   ├── logo192.png
│   ├── logo512.png
│   ├── mobile.png
│   ├── logo3.png
│   └── background.png
│
├── src/
│   ├── App.js
│   ├── App.css
│   ├── index.js
│   ├── index.css
│   ├── environment.js
│   │
│   ├── contexts/
│   │   └── AuthContext.jsx
│   │
│   ├── pages/
│   │   ├── landing.jsx
│   │   ├── authentication.jsx
│   │   ├── home.jsx
│   │   ├── history.jsx
│   │   └── VideoMeet.jsx
│   │
│   ├── styles/
│   │   └── videoComponent.module.css
│   │
│   └── utils/
│       └── withAuth.jsx
│
├── package.json
├── package-lock.json
└── README.md
```

*Note: Adjust the directory structure to match your actual repository. The listed image assets and package files must exist in the corresponding locations.*

## ⚙️ Prerequisites

Before running MeetX, make sure you have installed:

- [Node.js](https://nodejs.org/) — preferably an active LTS version.
- npm, included with Node.js.
- Git, if you want to clone the repository.
- A modern browser with camera and microphone support.

A running backend server is also required for authentication, meeting signaling, and meeting history.

## 🚀 Installation and Setup

### 1. Clone the repository

```bash
git clone <YOUR_REPOSITORY_URL>
cd <YOUR_PROJECT_FOLDER>
```

Replace the placeholders with your actual repository URL and project directory.

### 2. Install dependencies

```bash
npm install
```

### 3. Configure the backend URL

Open `src/environment.js`.

The supplied frontend configuration uses a hosted backend URL:

```javascript
let IS_PROD = true;

const server = IS_PROD
  ? "https://meetx-backend-sy25.onrender.com"
  : "http://localhost:8000";

export default server;
```

To use a local backend, change `IS_PROD` to `false` and make sure
