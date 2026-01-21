# 🔍 Cursor Chat Search

> A powerful web application for browsing, searching, and managing chat histories from the Cursor editor's AI chat feature. View, search, and export your AI conversations in various formats.

**This fork adds enhanced global search capabilities** - search across all your projects and conversations instantly with a command palette interface.

## ✨ Features

### 🆕 Global Search (New!)
- **⌘K / Ctrl+K** - Open search from anywhere with keyboard shortcut
- **Command Palette UI** - Modern, sleek search interface inspired by VS Code
- **Real-time Search** - Instant results as you type with smart debouncing
- **Filter by Type** - Search All, Ask Logs only, or Agent Logs only
- **Keyboard Navigation** - Arrow keys to navigate, Enter to open, Esc to close
- **Contextual Snippets** - See matching text with surrounding context
- **Cross-Project Search** - Find conversations across all your workspaces

### Core Features
- 🔍 Browse and search all workspaces with Cursor chat history
- 🌐 Support for both workspace-specific and global storage (newer Cursor versions)
- 🤖 View both AI chat logs and Composer logs
- 📁 Organize chats by workspace
- 🔎 Full-text search with filters for chat/composer logs
- 📱 Responsive design with dark/light mode support
- ⬇️ Export chats as:
  - Markdown files
  - HTML documents (with syntax highlighting)
  - PDF documents
- 🎨 Syntax highlighted code blocks
- 📌 Bookmarkable chat URLs
- ⚙️ Automatic workspace path detection

## 🚀 Quick Start

### Prerequisites

- Node.js 18+ and npm
- A Cursor editor installation with chat history

### Installation

1. Clone the repository:
```bash
git clone https://github.com/fulviofreitas/cursor-chat-browser.git
cd cursor-chat-browser
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

4. Open [http://localhost:3000](http://localhost:3000) in your browser

## 🔍 Using Global Search

The global search feature allows you to find any conversation across all your projects:

1. **Open Search**: Click the search button in the navbar or press `⌘K` (Mac) / `Ctrl+K` (Windows/Linux)
2. **Type Your Query**: Start typing to search across all conversations
3. **Filter Results**: Use the filter tabs to show only Ask Logs or Agent Logs
4. **Navigate Results**: Use `↑`/`↓` arrow keys or mouse to select
5. **Open Conversation**: Press `Enter` or click to open the selected result
6. **Close**: Press `Esc` or click outside to close

### Search Features

| Feature | Description |
|---------|-------------|
| Real-time | Results appear as you type (300ms debounce) |
| Cross-project | Searches all workspaces simultaneously |
| Title search | Matches conversation titles |
| Content search | Searches within message content |
| Snippets | Shows context around matching text |
| Sorted | Results sorted by most recent first |

## ⚙️ Configuration

The application automatically detects your Cursor workspace storage location based on your operating system:

| Platform | Path |
|----------|------|
| Windows | `%APPDATA%\Cursor\User\workspaceStorage` |
| WSL2 | `/mnt/c/Users/<USERNAME>/AppData/Roaming/Cursor/User/workspaceStorage` |
| macOS | `~/Library/Application Support/Cursor/User/workspaceStorage` |
| Linux | `~/.config/Cursor/User/workspaceStorage` |
| Linux (SSH) | `~/.cursor-server/data/User/workspaceStorage` |

If automatic detection fails, you can manually set the path in the Configuration page (⚙️).

## 📖 Usage

### Browsing Logs
- View all workspaces on the home page
- Browse AI chat logs by workspace
- Access Composer logs from the navigation menu
- Navigate between different chat tabs within a workspace
- View combined logs with type indicators
- See chat and composer counts per workspace

### Searching
- Use `⌘K` / `Ctrl+K` for global search across all projects
- Use the search bar in the navigation to search across all logs
- Filter results by chat logs, composer logs, or both
- Search results show:
  - Type badge (Chat/Composer)
  - Matching text snippets
  - Workspace location
  - Title
  - Timestamp

### Exporting
Each log can be exported as:
- **Markdown**: Plain text with code blocks
- **HTML**: Styled document with syntax highlighting
- **PDF**: Formatted document suitable for sharing

## 🛠️ Development

Built with:
- Next.js 14 (App Router)
- TypeScript
- Tailwind CSS
- shadcn/ui components
- Radix UI (Dialog)
- SQLite for reading Cursor's chat database

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 Changelog

See [CHANGELOG.md](CHANGELOG.md) for a list of changes.

### Recent Changes (This Fork)

- ✨ Added global search with command palette UI (`⌘K` / `Ctrl+K`)
- 🔧 Updated search API to support new Cursor data format (cursorDiskKV)
- 📦 Added @radix-ui/react-dialog dependency
- 🎨 Added dialog UI component
- 🔒 Added .cursor/ to .gitignore

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Original project by [thomas-pedersen](https://github.com/thomas-pedersen/cursor-chat-browser)
- Enhanced with global search by [fulviofreitas](https://github.com/fulviofreitas)
