# Chit-Chit-Chat
> **Real-Time Chat Application**

A full-stack real-time chat application built with React, Node.js, and Socket.io. Features multiple chat rooms, private messaging, typing indicators, and real-time notifications.

## Live Demo

- **Frontend (Live site)**: https://chit-chit-chat.netlify.app
- **Backend API**: Hosted on Render

## Features

### Core Functionality
- **Simple Username Authentication** - Join with any username
- **Multiple Chat Rooms** - General, Random, and Tech rooms
- **Real-time Messaging** - Instant message delivery
- **Online User List** - See who's currently online
- **Typing Indicators** - See when others are typing
- **Message Timestamps** - All messages include timestamps

### Advanced Features
- **Private Messaging** - Send direct messages to other users
- **Message Reactions** - React to messages with emojis
- **Real-time Notifications** - Browser and sound notifications
- **Responsive Design** - Works on desktop and mobile
- **Auto-reconnection** - Handles connection drops gracefully

### User Experience
- **Read Receipts** - Message delivery confirmation
- **Sound Notifications** - Audio alerts for new messages
- **Mobile Optimized** - Touch-friendly interface
- **Modern UI** - Clean and intuitive design
- **Performance Optimized** - Efficient real-time communication

## Tech Stack

### Frontend
- **React** - UI framework
- **Vite** - Build tool and dev server
- **Socket.io Client** - Real-time communication
- **CSS3** - Styling with modern features

### Backend
- **Node.js** - Runtime environment
- **Express.js** - Web framework
- **Socket.io** - WebSocket library for real-time features
- **CORS** - Cross-origin resource sharing

### Deployment
- **Netlify** - Frontend hosting
- **Render** - Backend hosting

## Project Structure

```text
real-time-communication-with-socket-io/
├── client/                 # React frontend
│   ├── src/
│   │   ├── components/     # React components
│   │   ├── socket/         # Socket.io client setup
│   │   ├── App.jsx         # Main App component
│   │   └── main.jsx        # React entry point
│   ├── public/             # Static assets
│   └── package.json        # Frontend dependencies
├── server/                 # Node.js backend
│   ├── server.js           # Main server file
│   ├── public/             # Static files
│   └── package.json        # Backend dependencies
└── README.md              # Project documentation
```

## Quick Start
### Prerequisites
- Node.js (v16 or higher)
- npm or yarn

### Local Development
1. Clone the repository
```bash
git clone https://github.com/PLP-MERN-Stack-Development/real-time-communication-with-socket-io-Polceze.git
cd real-time-communication-with-socket-io
```

2. Setup Backend

```bash
cd server
npm install
cp .env.example .env
# Edit .env with your configuration
npm run dev
```

Backend will run on http://localhost:5000

3. Setup Frontend (in a new terminal)

```bash
cd client
npm install
npm run dev
```
Frontend will run on http://localhost:5173

4. Open your browser and navigate to http://localhost:5173

### Environment Variables

**Backend (.env)**
```text
PORT=5000
CLIENT_URL=http://localhost:5173
NODE_ENV=development
```

**Frontend (.env)**
```text
VITE_SOCKET_URL=http://localhost:5000
```

## How to Use

### Join the Chat
- Open the application
- Enter your username
- Click "Join Chat"

### Send Messages
- Type in the message input at the bottom
- Press Enter or click Send
- Messages appear in real-time for all users in the room

### Switch Rooms
- Use the room selector in the sidebar
- Choose from General, Random, or Tech rooms
- Each room has separate message history

### Private Messages
- Click the message icon next to any user
- Type your private message
- Only that user will see the message

### React to Messages
- Hover over any message to see the reaction button
- Click to choose an emoji reaction
- Reactions are visible to all users

## API Endpoints

### Socket.io Events

**Client to Server:**
- `user_join` - Join chat with username
- `send_message` - Send message to room
- `private_message` - Send private message
- `typing` - Typing indicator
- `join_room` - Switch chat rooms
- `message_reaction` - Add reaction to message

**Server to Client:**
- `receive_message` - New message received
- `user_list` - Updated online users
- `typing_users` - Users currently typing
- `user_joined` - User joined notification
- `user_left` - User left notification
- `room_list` - Available rooms

### REST API
- `GET /api/messages/:room` - Get room message history
- `GET /api/users` - Get online users
- `GET /api/rooms` - Get available rooms

## Deployment

### Backend on Render
1. Push code to GitHub
2. Connect repository to Render
3. Set environment variables:
   - `NODE_ENV=production`
   - `CLIENT_URL=https://chit-chit-chat.netlify.app`
4. Deploy automatically on git push

### Frontend on Netlify
1. Build the project: `npm run build`
2. Connect repository to Netlify
3. Set build command: `npm run build`
4. Set publish directory: `dist`
5. Set environment variable:
   - `VITE_SOCKET_URL=https://real-time-communication-with-socket-io-8i10.onrender.com`

## Troubleshooting

### Common Issues

1. **CORS Errors**
   - Ensure backend CORS configuration includes your frontend URL
   - Check for trailing slash mismatches in URLs

2. **Socket Connection Failed**
   - Verify Socket.io server is running
   - Check network connectivity and firewall settings

3. **Messages Not Sending**
   - Check browser console for errors
   - Verify Socket.io connection status

4. **Users Not Appearing Online**
   - Refresh the page to re-establish connection
   - Check if user joined a room successfully

### Debug Mode
Enable debug mode by checking browser console for Socket.io logs and connection status.

## Security Features

- CORS configuration for controlled access
- Input validation and sanitization
- XSS prevention through React's built-in protections
- Rate limiting consideration for production

## Performance

- Message pagination for large histories
- Efficient reconnection handling
- Optimized Socket.io configuration
- Minimal data transfer with message batching

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/amazing-feature`
3. Commit changes: `git commit -m 'Add amazing feature'`
4. Push to branch: `git push origin feature/amazing-feature`
5. Open a Pull Request

## Future Enhancements

- User authentication with JWT
- Message persistence with database
- File and image sharing
- Voice messages
- Video calls
- Message search
- User profiles and avatars
- Chat room creation
- Message editing and deletion
- Admin features and moderation

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Socket.io](https://socket.io/) for real-time communication library
- [React](https://reactjs.org/) for the frontend framework
- [Vite](https://vitejs.dev/) for fast development build tools
- [Render](https://render.com/) for backend hosting
- [Netlify](https://netlify.com/) for frontend hosting

## Support

If you have any questions or run into issues:

1. Check the troubleshooting section above
2. Review the browser console for error messages
3. Ensure all services are running and accessible
4. Verify environment variables are set correctly

---

**Happy Chatting!** 