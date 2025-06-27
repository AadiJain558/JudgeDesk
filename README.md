# 🧑‍💻 Judge Desk — Real-time Collaborative Code Editor

<div align="center">

![Judge Desk Banner](https://img.shields.io/badge/Judge%20Desk-Real--time%20Collaboration-blue?style=for-the-badge&logo=code&logoColor=white)

[![React](https://img.shields.io/badge/React-18.0+-61DAFB?style=flat-square&logo=react&logoColor=black)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-16.0+-339933?style=flat-square&logo=nodedotjs&logoColor=white)](https://nodejs.org/)
[![Socket.IO](https://img.shields.io/badge/Socket.IO-4.0+-010101?style=flat-square&logo=socketdotio&logoColor=white)](https://socket.io/)
[![WebRTC](https://img.shields.io/badge/WebRTC-Enabled-FF6B6B?style=flat-square&logo=webrtc&logoColor=white)](https://webrtc.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)

*Bringing developers together in real-time collaboration*

</div>

---

## 🌟 Overview

**Judge Desk** is a comprehensive real-time collaboration platform designed to enhance developer productivity and team communication. Built with modern web technologies, it provides a seamless environment for collaborative coding sessions.

### ✨ Core Features

- 📝 **Real-time Collaborative Code Editing** — Multiple developers can edit code simultaneously with live cursor tracking
- 💬 **Integrated Team Chat** — Contextual messaging within development sessions
- 🎥 **Peer-to-Peer Video Calling** — High-quality video communication using WebRTC
- ✏️ **Interactive Whiteboard** — Visual collaboration with synchronized drawing capabilities
- 🚪 **Room Management** — Create and join development sessions with unique room IDs

All powered by a clean React + Vite frontend and a robust Node.js backend with Socket.IO for real-time communication.

---

## 🚀 Features & Capabilities

### 🔄 Real-time Synchronization
- **Live Code Editing** — See changes as they happen across all connected clients
- **Conflict Resolution** — Smart handling of simultaneous edits

### 🎨 Visual Collaboration
- **Interactive Whiteboard** — Perfect for system design discussions and brainstorming
- **Drawing Tools** — Pen, shapes, text, and color options
- **Canvas Synchronization** — All drawings appear instantly for all participants

### 🗣️ Communication Tools
- **Text Chat** — Quick messaging without leaving the coding environment
- **Video Calling** — Face-to-face communication with automatic disconnect handling

### 🏠 Room Management
- **Custom Room IDs** — Create memorable room names for your team
- **User Management** — See who's online and their current activities

---

## 🛠️ Tech Stack

<div align="center">

| Layer | Technologies |
|-------|-------------|
| **Frontend** | ![React](https://img.shields.io/badge/-React-61DAFB?style=flat&logo=react&logoColor=black) ![Vite](https://img.shields.io/badge/-Vite-646CFF?style=flat&logo=vite&logoColor=white) ![TailwindCSS](https://img.shields.io/badge/-TailwindCSS-38B2AC?style=flat&logo=tailwind-css&logoColor=white) |
| **Backend** | ![Node.js](https://img.shields.io/badge/-Node.js-339933?style=flat&logo=nodedotjs&logoColor=white) ![Express](https://img.shields.io/badge/-Express-000000?style=flat&logo=express&logoColor=white) ![Socket.IO](https://img.shields.io/badge/-Socket.IO-010101?style=flat&logo=socketdotio&logoColor=white) |
| **Real-time** | ![WebSockets](https://img.shields.io/badge/-WebSockets-010101?style=flat&logo=socketdotio&logoColor=white) |
| **Video** | ![WebRTC](https://img.shields.io/badge/-WebRTC-FF6B6B?style=flat&logo=webrtc&logoColor=white) |

</div>

---

## 📁 Project Architecture

```
JudgeDesk/
├── 🔧 backend/                    # Server-side application
│   ├── 🚀 index.js                # Main server entry point
│   ├── 📝 codeCollaboration.js    # Real-time code sync logic
│   ├── 📹 videoCallNew.js         # WebRTC signaling server
│   ├── 🎨 whiteboard.js           # Canvas synchronization
│   └── 📦 package.json            # Backend dependencies
│
├── ⚛️ frontend/                   # Client-side application
│   ├── 📂 src/
│   │   ├── 🧩 components/         # Reusable UI components
│   │   │   ├── 💬 Chat.jsx        # Chat interface
│   │   │   ├── 📝 CodeEditor.jsx  # Collaborative editor
│   │   │   ├── 🏠 RoomSidebar.jsx # Room management UI
│   │   │   └── 🎨 Whiteboard.jsx  # Drawing canvas
│   │   │
│   │   ├── 🎣 hooks/              # Custom React hooks
│   │   │   ├── 🌐 useAppState.js  # Global state management
│   │   │   ├── 🏠 useRoomManagement.js # Room operations
│   │   │   └── 🔌 useSocketConnection.js # Socket lifecycle
│   │   │
│   │   ├── 🔧 services/           # Business logic layer
│   │   │   ├── 🔌 socketService.js # Socket.IO abstraction
│   │   │   └── 💾 storageService.js # Local storage utils
│   │   │
│   │   ├── 📱 App.jsx             # Main application component
│   │   ├── 🏠 Homepage.jsx        # Landing page
│   │   ├── 🚀 main.jsx            # React entry point
│   │   ├── 📹 VideoCallV2.jsx     # Video call interface
│   │   └── 🎨 WhiteboardPage.jsx  # Whiteboard page
│   │
│   ├── 📄 index.html              # HTML template
│   ├── 🎨 tailwind.config.js      # Tailwind configuration
│   ├── ⚡ vite.config.js          # Vite build configuration
│   └── 📦 package.json            # Frontend dependencies
│
└── 📚 README.md                   # Project documentation
```

---

## 🚀 Quick Start Guide

### 📋 Prerequisites

Before you begin, ensure you have the following installed:
- **Node.js** (v16.0 or higher)
- **npm** or **yarn**
- **Git**

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/AadiJain558/JudgeDesk.git
cd JudgeDesk
```

### 2️⃣ Install Dependencies

```bash
# Install backend dependencies
cd backend
npm install

# Install frontend dependencies
cd ../frontend
npm install
```

### 3️⃣ Start the Development Servers

**Option A: Using two terminals (Recommended)**

```bash
# Terminal 1 - Backend Server
cd backend
npm run dev
```

```bash
# Terminal 2 - Frontend Development Server
cd frontend
npm run dev
```

**Option B: Using concurrently (Alternative)**

```bash
# From project root
npm install -g concurrently
concurrently "cd backend && npm run dev" "cd frontend && npm run dev"
```

### 4️⃣ Access the Application

- **Frontend**: [http://localhost:5173](http://localhost:5173)
- **Backend**: [http://localhost:5000](http://localhost:5000)

---

## 🏗️ Module Breakdown

### 🔙 Backend Architecture

#### Core Modules

| Module | Purpose | Key Features |
|--------|---------|-------------|
| `index.js` | 🏠 Server Foundation | Express setup, Socket.IO initialization, CORS configuration |
| `codeCollaboration.js` | 📝 Code Sync Engine | Real-time text synchronization, cursor tracking, conflict resolution |
| `videoCallNew.js` | 📹 Video Infrastructure | WebRTC signaling, peer connection management, call state handling |
| `whiteboard.js` | 🎨 Canvas Sync | Drawing data broadcasting, shape synchronization, collaborative drawing |

#### Server Features
- **Socket.IO Integration** — Real-time bidirectional communication
- **WebRTC Signaling** — Peer-to-peer connection establishment
- **Room Management** — Dynamic room creation and user tracking
- **Error Handling** — Comprehensive error catching and logging

### ⚛️ Frontend Architecture

#### 🧩 Components Layer

| Component | Responsibility | Key Features |
|-----------|---------------|-------------|
| `Chat.jsx` | 💬 Messaging Interface | Real-time chat, message history, emoji support |
| `CodeEditor.jsx` | 📝 Code Collaboration | Syntax highlighting, live editing, cursor tracking |
| `RoomSidebar.jsx` | 🏠 Room Management | User list, room info, settings panel |
| `Whiteboard.jsx` | 🎨 Visual Collaboration | Drawing tools, shape creation, collaborative canvas |

#### 🎣 Hooks Layer

| Hook | Purpose | Responsibilities |
|------|---------|-----------------|
| `useAppState.js` | 🌐 State Management | Global state, user preferences, app configuration |
| `useRoomManagement.js` | 🏠 Room Operations | Join/leave logic, room validation, user management |
| `useSocketConnection.js` | 🔌 Connection Management | Socket lifecycle, reconnection logic, event handling |

#### 🔧 Services Layer

| Service | Function | Capabilities |
|---------|----------|-------------|
| `socketService.js` | 🔌 Communication Layer | Socket.IO abstraction, event management, error handling |
| `storageService.js` | 💾 Data Persistence | Local storage, session management, preferences |

---

## 🎯 Usage Examples

### Creating a New Room

```javascript
// Join or create a room
const roomId = "my-dev-session";
socket.emit('join-room', roomId);
```

### Real-time Code Collaboration

```javascript
// Send code changes
socket.emit('code-change', {
  roomId: currentRoom,
  code: editorContent,
  cursorPosition: cursor.position
});
```

### Whiteboard Drawing

```javascript
// Send drawing data
socket.emit('draw', {
  roomId: currentRoom,
  drawingData: {
    x: mouseX,
    y: mouseY,
    tool: 'pen',
    color: '#ff0000'
  }
});
```

---

## 🔧 Configuration


### Frontend Configuration

Modify `vite.config.js` for custom build settings:

```javascript
export default defineConfig({
  plugins: [react()],
  server: {
    port: 5173,
    host: '0.0.0.0'
  }
});
```

---

## 🚀 Deployment

### Backend Deployment

1. **Prepare for production**:
   ```bash
   cd backend
   npm install --production
   ```

   ```

2. **Start the server**:
   ```bash
   npm start
   ```

### Frontend Deployment

1. **Build the application**:
   ```bash
   cd frontend
   npm run build
   ```

2. **Serve static files** using your preferred method (Nginx, Apache, Vercel, Netlify)

---

## 🤝 Contributing

We welcome contributions from the community! Here's how you can help:

### 🐛 Bug Reports
- Use the GitHub Issues tab
- Include detailed reproduction steps
- Provide environment information

### 💡 Feature Requests
- Open an issue with the "enhancement" label
- Describe the feature and its benefits
- Include mockups or examples if applicable

### 🔧 Development Workflow

1. **Fork the repository**
2. **Create a feature branch**: `git checkout -b feature/amazing-feature`
3. **Make your changes**
4. **Add tests** if applicable
5. **Commit your changes**: `git commit -m 'Add amazing feature'`
6. **Push to the branch**: `git push origin feature/amazing-feature`
7. **Open a Pull Request**

### 📝 Code Style
- Follow existing code conventions
- Use meaningful variable names
- Add comments for complex logic
- Ensure responsive design for UI components

---

## 🧪 Testing

### Running Tests

```bash
# Backend tests
cd backend
npm test

# Frontend tests
cd frontend
npm test
```

### Test Coverage

```bash
# Generate coverage report
npm run test:coverage
```

---

## 🔍 Troubleshooting

### Common Issues

| Issue | Solution |
|-------|----------|
| **Connection Failed** | Check if backend server is running on port 5000 |
| **Video Call Not Working** | Ensure HTTPS is enabled for WebRTC to function |
| **Room Not Found** | Verify room ID is correct and server is accessible |
| **Drawing Not Syncing** | Check network connection and socket status |

### Debug Mode

Enable debug logging:

```bash
# Backend
DEBUG=socket.io:* npm run dev

# Frontend
VITE_DEBUG=true npm run dev
```

---



## 🔒 Security Considerations

- **Input Validation** — All user inputs are sanitized
- **Rate Limiting** — Protection against spam and DoS attacks
- **CORS Configuration** — Proper cross-origin resource sharing setup
- **WebRTC Security** — Secure peer-to-peer connections

---


## 📞 Support

### Getting Help

- 📧 **Email**: [aadijain558@gmail.com](aadijain558@gmail.com)
- 🐛 **Issues**: [GitHub Issues](https://github.com/AadiJain558/JudgeDesk/issues)

### Community

- 🌟 **Star us on GitHub** if you find Judge Desk useful!

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2025 Judge Desk

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
```

---

## 🙏 Acknowledgments

### Built With Love By
- **Aadi Jain and Vansh Gupta** — The passionate developers behind Judge Desk

### Special Thanks
- **Socket.IO Team** — For real-time communication capabilities
- **WebRTC Community** — For peer-to-peer video technology
- **React Team** — For the amazing frontend framework
- **Tailwind CSS** — For beautiful and responsive styling

---

<div align="center">

### 🌟 Made with ❤️ by developers, for developers

**Happy Coding!** 🚀

</div>
