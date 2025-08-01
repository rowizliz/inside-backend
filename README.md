# 🎥 Inside Video Call Backend

Socket.io signaling server cho ứng dụng video call Inside.

## 🚀 Features

- **WebRTC Signaling**: Xử lý offer/answer/ICE candidates
- **User Management**: Quản lý users online
- **Room Management**: Quản lý video call rooms
- **Connection Monitoring**: Heartbeat và health checks
- **CORS Support**: Hỗ trợ cross-origin requests

## 🛠️ Tech Stack

- **Node.js** + **Express.js**
- **Socket.io** for real-time communication
- **CORS** for cross-origin support

## 📦 Installation

```bash
npm install
```

## 🏃‍♂️ Running

### Development
```bash
npm run dev
```

### Production
```bash
npm start
```

## 🌐 Endpoints

- `GET /` - Server status
- `GET /health` - Health check with stats
- `Socket.io` - Real-time signaling

## 🔧 Environment

- **Port**: Process.env.PORT || 3001
- **CORS Origins**: localhost:3000, *.vercel.app

## 📡 Socket Events

### Client → Server
- `user-joined` - User joins with info
- `initiate-call` - Start video call
- `accept-call` - Accept incoming call
- `reject-call` - Reject incoming call
- `webrtc-offer` - WebRTC offer
- `webrtc-answer` - WebRTC answer
- `webrtc-ice-candidate` - ICE candidate
- `end-call` - End video call
- `heartbeat` - Connection heartbeat

### Server → Client
- `users-updated` - Updated user list
- `incoming-call` - Incoming call notification
- `call-accepted` - Call accepted
- `call-rejected` - Call rejected
- `webrtc-offer` - WebRTC offer
- `webrtc-answer` - WebRTC answer
- `webrtc-ice-candidate` - ICE candidate
- `call-ended` - Call ended
- `heartbeat-response` - Heartbeat response
- `user-disconnected` - User disconnected

## 🚀 Deployment

Deploy to Railway, Heroku, or any Node.js hosting platform.

## 📄 License

MIT License
