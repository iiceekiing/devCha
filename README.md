# devCha - Multi-User Chat Platform

A simple, modern multi-user chat platform built with HTML, Tailwind CSS, and JavaScript. No backend required - all data is stored locally in the browser.

## 🚀 Features

### Core Chat Features
- **Real-time Messaging**: Send and receive messages instantly
- **Multi-User Support**: Register multiple users with unique usernames
- **Session Management**: Persistent login sessions
- **Message History**: All messages saved and loaded on return
- **User Join Notifications**: See when new users join the chat
- **Delete Messages**: Users can delete their own messages only

### Rich Media Support
- **File Upload**: Share images, videos, documents (PDF, DOC, DOCX, TXT)
- **Voice Recording**: Record and send voice notes
- **Media Preview**: Preview files and voice notes before sending
- **Inline Display**: Images show inline, videos have playback controls
- **Download Support**: Download any shared files

### Search & Discovery
- **Real-time Search**: Filter messages by content, username, or filename
- **Member Count**: See total number of registered users
- **Member List**: View all platform members with current user highlighted

### UI/UX
- **Mobile Responsive**: Works perfectly on all screen sizes
- **Modern Design**: Clean, WhatsApp-inspired interface
- **WhatsApp-style Icons**: 🔗 for files, 🗃️ for attachments, 🎙️ for voice
- **Color-coded Messages**: Blue for current user, gray for others
- **System Messages**: Orange badges for join notifications

## 🛠️ Tech Stack

### Frontend
- **HTML5**: Semantic markup structure
- **Tailwind CSS v4**: Utility-first CSS framework
- **Vanilla JavaScript**: No frameworks, pure JS implementation

### Storage
- **Local Storage**: Browser-based persistence
- **Base64 Encoding**: File and audio data storage
- **JSON Format**: Structured data storage

### Development Tools
- **Tailwind CLI**: CSS compilation and optimization
- **Live Server**: Python HTTP server for development

## 📋 Requirements

### Browser Support
- **Modern Browsers**: Chrome, Firefox, Safari, Edge
- **JavaScript Required**: Must be enabled
- **Local Storage**: Browser must support localStorage
- **Media APIs**: Microphone access for voice recording

### File Types Supported
- **Images**: JPG, PNG, GIF, WebP, SVG
- **Videos**: MP4, WebM, OGG
- **Documents**: PDF, DOC, DOCX, TXT

## 🚀 Getting Started

### Prerequisites
- Node.js (for Tailwind CLI)
- Python 3 (for local server)
- Modern web browser

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/iiceekiing/devCha.git
   cd devCha
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start Tailwind CSS compiler**
   ```bash
   npx tailwindcss -i ./src/input.css -o ./src/output.css --watch
   ```

4. **Start local server**
   ```bash
   python3 -m http.server 8080
   ```

5. **Open application**
   Navigate to `http://localhost:8080`

## 🏗️ Project Structure

```
devCha/
├── index.html              # Main application file
├── src/
│   ├── input.css          # Tailwind input file
│   └── output.css         # Compiled CSS output
├── package.json           # Node.js dependencies
├── README.md             # This file
└── .git/               # Git version control
```

## 💾 Data Storage

### Users Collection
```javascript
// localStorage: 'chatUsers'
[
  {
    fullName: "John Doe",
    username: "johndoe",
    password: "password123"
  }
]
```

### Messages Collection
```javascript
// localStorage: 'chatMessages'
[
  {
    id: 1641234567890,
    username: "johndoe",
    fullName: "John Doe",
    message: "Hello everyone!",
    timestamp: "2023-01-04T10:30:00.000Z",
    messageType: "text|file|voice",
    fileAttachment: {
      name: "document.pdf",
      type: "application/pdf",
      size: 1024000,
      data: "base64-encoded-data"
    },
    voiceNote: {
      data: "base64-encoded-audio",
      type: "audio/webm"
    },
    isSystemMessage: false
  }
]
```

### Current Session
```javascript
// localStorage: 'currentUser'
{
  fullName: "John Doe",
  username: "johndoe",
  password: "password123"
}
```

## 🔧 Configuration

### Tailwind CSS
- **Input File**: `src/input.css`
- **Output File**: `src/output.css`
- **Watch Mode**: Enabled for development
- **Custom Colors**: Defined in `@theme` directive

### Server Configuration
- **Port**: 8080 (default)
- **Static Files**: Served from project root
- **CORS**: Enabled for local development

## 🎨 Design System

### Color Palette
- **Primary Blue**: `#2563eb` (buttons, current user messages)
- **Success Green**: `#16a34a` (login button)
- **Danger Red**: `#dc2626` (logout, delete buttons)
- **Warning Orange**: `#f97316` (voice recording, system messages)
- **Neutral Gray**: Various shades for backgrounds and text

### Typography
- **Font Family**: System UI default
- **Responsive Text**: Scales appropriately on all devices
- **Message Timestamps**: 12-hour format with minutes

## 🔒 Security Features

### Authentication
- **Username Validation**: No duplicate usernames allowed
- **Password Storage**: Stored in local storage (client-side only)
- **Session Management**: Automatic login persistence

### Message Security
- **Ownership Verification**: Users can only delete their own messages
- **Input Sanitization**: Basic XSS protection
- **File Type Restrictions**: Limited to safe file types

## 📱 Mobile Optimization

### Responsive Design
- **Flexible Layout**: Adapts to screen size
- **Touch-Friendly**: Large tap targets for mobile
- **Viewport Meta**: Proper mobile rendering
- **Scroll Behavior**: Optimized for touch devices

## 🚀 Deployment

### Static Hosting
The application can be deployed to any static hosting service:

- **Netlify**: Drag and drop deployment
- **Vercel**: Import from GitHub
- **GitHub Pages**: Enable in repository settings
- **Firebase Hosting**: Upload static files

### Build Process
1. Compile CSS with Tailwind CLI
2. Minify HTML (optional)
3. Upload files to hosting service

## 🤝 Contributing

### Development Workflow
1. Fork the repository
2. Create feature branch
3. Make changes
4. Test thoroughly
5. Submit pull request

### Code Style
- **Semantic HTML5**: Use proper elements
- **Tailwind Classes**: Utility-first approach
- **Modern JavaScript**: ES6+ features
- **Consistent Naming**: Clear variable and function names

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 🙏 Acknowledgments

- **Tailwind CSS**: For the excellent CSS framework
- **Browser APIs**: Local storage, MediaRecorder, FileReader
- **WhatsApp Design**: Inspiration for UI/UX patterns

## 📞 Support

For issues, questions, or contributions:
- **GitHub Issues**: Create an issue in the repository
- **Author**: iiceekiing
- **Repository**: https://github.com/iiceekiing/devCha

---

**devCha** - Simple, powerful, client-side chat platform. No backend required! 🚀
