# Component 4: Chat & Messaging System

## Team Member Assignment
**Assigned to: [Team Member 4 Name]**

## What This Component Includes

### Backend Files:
- `backend/src/services/socketHandlers.js`
- `backend/src/models/Message.js`
- `backend/src/routes/messages.js` (if separate from main server)
- Socket.IO integration in `working-server.js`

### Frontend Files:
- `frontend/src/pages/ChatPage.jsx`
- `frontend/src/services/socketService.js`
- `frontend/src/components/chat/` (new directory)
- `frontend/src/stores/chatStore.js` (new file)

## Key Features to Implement:
1. Real-time messaging with Socket.IO
2. Message threading and conversation management
3. Message status (sent, delivered, read)
4. File and image sharing
5. Message search and history
6. Online/offline status indicators
7. Message encryption (optional)

## API Endpoints to Implement:
- `GET /api/messages`
- `GET /api/messages/:userId`
- `POST /api/messages`
- `PUT /api/messages/:messageId/read`
- `DELETE /api/messages/:messageId`

## Dependencies to Install:
```bash
# Backend
npm install socket.io multer

# Frontend
npm install socket.io-client react-emoji-picker
```

## Testing Checklist:
- [ ] Real-time messaging works between users
- [ ] Messages are properly threaded
- [ ] Message status updates correctly
- [ ] File uploads work in chat
- [ ] Message history loads properly
- [ ] Online status is accurate
- [ ] Messages persist in database

## Integration Points:
- Depends on Component 1 (Authentication)
- Uses user data from Component 2 (Profiles)
- Connects users from Component 3 (Matching)
- Chat can lead to Component 5 (Sessions)

## Files to Create/Modify:
1. Create Socket.IO handlers for real-time messaging
2. Implement message persistence in MongoDB
3. Create chat interface components
4. Add file upload functionality
5. Implement message status tracking

## Key Components to Build:
1. **ChatContainer Component**: Main chat interface
2. **MessageList Component**: Display messages
3. **MessageInput Component**: Send new messages
4. **ConversationList Component**: List of conversations
5. **FileUpload Component**: Handle file sharing
6. **OnlineStatus Component**: Show user online status

## Socket.IO Events to Implement:
1. **Connection Events**: User connect/disconnect
2. **Message Events**: Send/receive messages
3. **Status Events**: Typing indicators, read receipts
4. **Room Events**: Join/leave conversation rooms
5. **Notification Events**: New message notifications

## Database Schema:
```javascript
// Message Schema
{
  threadId: String,
  sender: String,
  recipient: String,
  content: String,
  type: String, // 'text', 'image', 'file'
  status: String, // 'sent', 'delivered', 'read'
  createdAt: Date,
  updatedAt: Date
}
```

## Notes:
- Focus on real-time performance
- Implement proper error handling for network issues
- Consider message encryption for privacy
- Add message search functionality
- Ensure mobile-friendly chat interface
