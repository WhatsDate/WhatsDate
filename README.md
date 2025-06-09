## WhatsDate AI dating reply:

Use [WhatsApp client library](https://wwebjs.dev/) and [OpenAI client library](https://github.com/openai/openai-node) to auto-reply to your instant messages.

## WhatsApp API client Documentation
https://docs.wwebjs.dev/

## Features

### Core AI & WhatsApp Integration
- **AI-Powered Responses**: Automatically generate responses to WhatsApp messages using OpenAI
- **Emoji Reaction Expansion**: React to messages with emojis to generate contextual responses
- **Adaptive Response Timing**: Mimics human conversation patterns by timing responses based on user behavior
- **Smart Message Grouping**: Automatically groups consecutive messages from the same contact and generates unified responses
- **Efficient Message Processing**: Groups consecutive messages within a 12-second window for better context

### User Interface & Experience
- **Modern Web Interface**: Responsive UI served from `/public` to manage contacts, view conversations, and configure AI
- **Real-time Updates**: Server-Sent Events (SSE) for instant UI updates without polling
- **Web-Based QR Code**: Easy setup with browser-based QR code scanning for authentication
- **Auto-response Control**: Enable/disable auto-response per contact or globally via the UI
- **Conversation History Viewer**: View and manage conversation history with formatted timestamps

### Data Management & Persistence
- **Persistent Data**: All conversation history, auto-response settings, and pending responses persist between restarts in `whatsapp-auth/timing-data.json`
- **Standardized Timestamps**: Consistent timestamp handling across the application using `src/utils/TimestampManager.ts`
- **Configuration Management**: Centralized app configuration via `src/config/app-config.json`

### Security & Development
- **Multi-layered Security**: Comprehensive IPC security validation, CSP implementation, and environment-based configurations
- **Development vs Production**: Automatic environment detection with appropriate security policies
- **DevTools Control**: Conditional DevTools access based on environment and configuration
- **Rate Limiting**: Built-in rate limiting for IPC calls to prevent abuse
- **Input Sanitization**: XSS protection and input validation throughout the application

### Packaging & Distribution
- **Electron Desktop App**: Distributed as a native desktop application using Electron and Electron Forge
- **Cross-platform Support**: Windows-focused with configurable build targets
- **Single Instance**: Prevents multiple application instances from running simultaneously

## System Requirements

- Windows operating system
- Node.js installed (for development)
- Web browser (Chrome recommended for interacting with the local web UI)
- Active WhatsApp account

- 
