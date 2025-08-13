# 📹 Streamify

Streamify is a full-stack real-time communication platform that enables **video calls**, **instant messaging**, and **secure user authentication**.  
It is powered by **Stream's Video & Chat APIs** with a modern **React frontend** and a robust **Node.js + Express + MongoDB backend**.

---

## ✨ Features

- 🎥 **Real-time Video Calls** — powered by `@stream-io/video-react-sdk`
- 💬 **Instant Messaging** — using `stream-chat` and `stream-chat-react`
- 🔒 **Secure Authentication** — with JWT and password hashing (`bcryptjs`)
- 📦 **Persistent Data Storage** — using MongoDB + Mongoose
- 🖥 **Modern UI** — Tailwind CSS + DaisyUI for responsive design
- ⚡ **Fast State Management** — via `zustand`
- 🌐 **REST API Backend** — built with Express
- 🔄 **Cron Jobs** — for scheduled background tasks
- 🔑 **Environment Variables Support** — with `dotenv`

---

## 📂 Folder Structure

streamify/
│
├── backend/ # Backend server (Node.js + Express)
│ ├── src/ # Backend source code
│ ├── package.json
│ └── .env # Backend environment variables (ignored in Git)
│
├── frontend/ # Frontend client (React + Vite)
│ ├── src/ # Frontend source code
│ ├── package.json
│ └── .env # Frontend environment variables (ignored in Git)
│
└── README.md # Project documentation





---

## 🛠 Tech Stack

### **Frontend**
- **React 19** + **Vite**
- `@stream-io/video-react-sdk`
- `stream-chat` & `stream-chat-react`
- `react-router` for navigation
- `zustand` for state management
- `axios` for API requests
- **Tailwind CSS** + **DaisyUI** for styling
- `react-hot-toast` for notifications

### **Backend**
- **Node.js** + **Express**
- **MongoDB** with **Mongoose**
- `jsonwebtoken` for authentication
- `bcryptjs` for password hashing
- `cookie-parser` for handling cookies
- `cors` for cross-origin requests
- `cron` for scheduled tasks
- `dotenv` for environment variables

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository
```bash
git clone <your-repo-url>
cd streamify



backedn setup
cd backend
npm install
npm run start


frontend setup
cd frontend
npm install
npm run dev

backedn.env

PORT=5000
MONGO_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/streamify
JWT_SECRET=your_jwt_secret
STREAM_API_KEY=your_stream_api_key
STREAM_API_SECRET=your_stream_api_secret
API_URL=https://localhost/api/health


frontend.env

VITE_STREAM_API_KEY=your_stream_api_key
VITE_BACKEND_URL=http://localhost:5000




| Command           | Description              |
| ----------------- | ------------------------ |
| `npm run dev`     | Start development server |
| `npm run build`   | Build for production     |
| `npm run preview` | Preview production build |



| Command         | Description                |
| --------------- | -------------------------- |
| `npm run start` | Start backend server       |
| `npm run dev`   | Start backend with Nodemon |




        ┌───────────────────────┐
        │      Frontend         │
        │  (React + Vite)       │
        └─────────┬─────────────┘
                  │  Axios / WebSocket
                  ▼
        ┌───────────────────────┐
        │      Backend           │
        │ (Node.js + Express)    │
        └─────────┬─────────────┘
                  │  REST API / Auth
                  ▼
        ┌───────────────────────┐
        │     MongoDB           │
        │   (Mongoose ODM)      │
        └───────────────────────┘

                  │
                  ▼
        ┌───────────────────────┐
        │   Stream API           │
        │ (Video + Chat SDK)     │
        └───────────────────────┘
