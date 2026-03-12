# 🍅 Pom - Advanced Pomodoro Timer

A next-generation Pomodoro timer with CLI and Web UI, featuring AI insights, multi-profiles, cloud sync, and plugin system. Built with Go and pure HTML/JS.

![Go](https://img.shields.io/badge/Language-Go-00ADD8?style=for-the-badge&logo=go&logoColor=white)
![Cobra CLI](https://img.shields.io/badge/CLI-Cobra-7E57C2?style=for-the-badge&logo=terminal&logoColor=white)
![Pom Web UI](https://img.shields.io/badge/Web%20UI-Galactic%20Flux-18FFFF?style=for-the-badge)
![Version](https://img.shields.io/github/v/release/Flack74/pom?style=for-the-badge)
![License](https://img.shields.io/github/license/Flack74/pom?style=for-the-badge)

## ✨ Features

### 🚀 **High-Impact Features**
- 🌐 **Web UI Bridge** - Modern HTML/JS interface with Galactic Flux theme
- 👥 **Multi-Profile Support** - Work, study, quick, and custom profiles
- 📅 **Calendar Heatmap** - Visual session tracking with activity levels
- 📤 **Export/Import** - JSON/CSV data backup and analysis
- 🔄 **Cloud Sync** - GitHub/Dropbox synchronization (optional)
- 🧩 **Plugin System** - Custom scripts for Notion, Slack, notifications
- 🔐 **Privacy Mode** - Zero-data logging with local-only option

### 🎯 **Core Features**
- 🎯 Beautiful progress bar with real-time countdown
- 🎨 Multiple color themes (default, minimal, vibrant, galactic)
- 📊 Comprehensive session tracking and statistics
- 🎯 Daily goals with streak tracking
- 📝 Task planning and time tracking
- 🔔 Cross-platform notifications and sounds
- ⏯️ Pause/resume/quit functionality
- 💪 Motivational messages and feedback

## 🌐 Web UI - Galactic Flux Theme

Launch the modern web interface with stunning space-themed design:

```bash
# Foreground mode (blocks terminal)
pom web                    # Start on port 8080
pom web -p 3000           # Custom port

# True background daemon (recommended)
nohup pom web &           # Background on port 8080
nohup pom web -p 3000 &   # Background on custom port

# Alternative: daemon flag (still attached to terminal)
pom web -d                # Shows daemon instructions

# Access web UI
# Open browser: http://localhost:8080 (or your port)
# Stop daemon: pkill pom
```

**✅ Fully Working Features:**
- 🎨 **Galactic Flux** theme with animated glow effects
- 📱 **Responsive design** - works on all devices
- ⚡ **Embedded in binary** - no external files needed
- 🎯 **Working timer** with real-time progress visualization
- 📊 **Dashboard** with live stats via API
- 🎮 **CLI Controls** - all CLI commands via web interface
- 🌍 **Cross-platform** - Windows, Mac, Linux
- 🚀 **Daemon mode** - run in background
- 🔧 **Zero dependencies** - single binary solution

**Color Palette:**
- Background: Deep space navy (#0B0F1A)
- Primary: Neon cyan (#18FFFF)
- Secondary: Vibrant pink (#FF4081)
- Success: Emerald green (#00E676)
- Warning: Solar yellow (#FFD600)

## 🚀 Quick Start

### CLI Usage
```bash
# Basic session
pom start

# Use profiles
pom profile use work       # 45min work, 10min break
pom start -p study        # 30min work, 5min break

# AI insights
pom insights suggest      # Get personalized recommendations
pom insights calendar     # View session heatmap

# Export data
pom export json backup.json
```

### Web Interface
```bash
# True background daemon (terminal free) ✅ RECOMMENDED
nohup pom web &
nohup pom web -p 3000 &    # Custom port

# Foreground mode (terminal blocked)
pom web

# Daemon instructions
pom web -d                 # Shows daemon setup help

# Access features:
# 1. Open browser: http://localhost:8080
# 2. Use Timer tab for Pomodoro sessions
# 3. Use CLI Controls tab for all CLI commands
# 4. Use Dashboard tab for statistics

# Stop daemon: pkill pom
```

**Troubleshooting Web UI:**
```bash
# If web UI doesn't load:
# 1. Check server is running
curl http://localhost:8080/

# 2. Test API endpoints
curl http://localhost:8080/api/profiles

# 3. Check daemon process
ps aux | grep pom

# 4. Start true daemon
nohup pom web -p 3001 &

# 5. Stop all instances
pkill pom
```

## 👥 Multi-Profile System

Pre-built profiles for different work contexts:

| Profile | Work Time | Break Time | Sessions | Use Case |
|---------|-----------|------------|----------|----------|
| `default` | 25min | 5min | 4 | Standard Pomodoro |
| `work` | 45min | 10min | 3 | Deep work sessions |
| `study` | 30min | 5min | 4 | Learning & research |
| `quick` | 15min | 3min | 6 | Quick tasks |

```bash
pom profile list                    # List all profiles
pom profile use work               # Switch profile
pom profile create "coding" 45 10 3  # Create custom
```

## 🧠 AI-Powered Insights

Get personalized suggestions based on your performance:

```bash
pom insights suggest              # AI recommendations
pom insights today               # Today's statistics
pom insights calendar            # Visual heatmap
```

**AI analyzes:**
- Completion rates and patterns
- Optimal session lengths
- Best focus times
- Productivity trends

## 🧩 Plugin System

Automate workflows with custom scripts:

```bash
pom plugins list                 # Available plugins
pom plugins enable notion-logger # Log to Notion
pom plugins add "my-script" "echo 'Done!'" session_end
```

**Built-in plugins:**
- **Notion Logger** - Log sessions to Notion database
- **Slack Notify** - Send completion notifications
- **Break Reminder** - Desktop notifications with sound
- **Focus Mode** - Block distracting websites

## 📤 Data Management

Export and sync your productivity data:

```bash
# Export
pom export json backup.json      # Complete backup
pom export csv sessions.csv      # Spreadsheet format

# Cloud sync
pom sync setup github           # Configure GitHub sync
pom sync push                   # Upload data
pom sync pull                   # Download data

# Privacy
pom privacy enable              # Zero logging mode
pom privacy clear               # Delete all data
```

### CLI Interface
![image](https://github.com/user-attachments/assets/164def14-0d86-4e2f-aa16-399b8a6c20e2)
*Beautiful progress bar with real-time countdown*

![image](https://github.com/user-attachments/assets/ca10ac43-86dd-49ee-bd33-01ce8acd266b)
*Multiple color themes (default, minimal, vibrant)*

![image](https://github.com/user-attachments/assets/48a15a2e-a4ae-458f-8ea1-917604299c85)
*Comprehensive session tracking and analytics*

### Web UI - Galactic Flux Theme
![image](https://github.com/user-attachments/assets/d7ed283a-f6fc-45d6-8ad2-4ad1eb72709f)
*Modern React interface with space-themed design*

![image](https://github.com/user-attachments/assets/6e5f6d99-070a-4aad-84e9-00db25e12f0f)
*Productivity analytics*

![image](https://github.com/user-attachments/assets/f74452b9-29d3-44b8-9619-0198a01fa6c7)
*Web cli controls with session visualization*

## 🔧 Installation

### ✅ Available Now

#### Arch Linux (AUR)
```bash
yay -S pom
# or
paru -S pom
```

#### GitHub Releases
```bash
# Download latest release
curl -L https://github.com/Flack74/pom/releases/latest/download/pom-linux-amd64.tar.gz | tar xz
sudo mv pom /usr/local/bin/
```

#### From Source
```bash
git clone https://github.com/Flack74/pom.git
cd pom
go build -o pom .
sudo cp pom /usr/local/bin/
```

### 🚧 Coming Soon

#### Debian/Ubuntu
```bash
# Coming soon
sudo apt install pom
```

#### Fedora/RHEL
```bash
# Coming soon
sudo dnf install pom
```

#### macOS
```bash
# Coming soon
brew install pom
```

#### Windows
```powershell
# Coming soon
choco install pom
```

#### Snap
```bash
# Coming soon
sudo snap install pom
```

#### Flatpak
```bash
# Coming soon
flatpak install flathub com.github.Flack74.pom
```

## 🛠️ Development

### Prerequisites
- Go 1.21+

### Build
```bash
# Build with embedded web UI
go build -o pom .

# Or use Makefile for version info
make build
```

### Project Structure
```
pom/
├── cmd/           # CLI commands
├── config/        # Configuration & data management
├── logs/          # Session logging
├── web/           # Web UI server & HTML/JS frontend
├── packaging/     # Package configurations
└── .github/       # CI/CD workflows
```

## 🔐 Privacy & Security

- **Privacy Mode**: Zero data logging
- **Local Storage**: All data stored locally
- **Optional Cloud Sync**: Opt-in only
- **No Telemetry**: No usage tracking
- **Open Source**: Full transparency

## 📊 Statistics & Analytics

Track your productivity with detailed insights:
- Daily/weekly/monthly progress
- Session completion rates
- Focus time trends
- Goal achievement tracking
- Streak monitoring
- Task-specific analytics

## 🎨 Themes

Choose your visual experience:
- **Default**: Professional and clean
- **Minimal**: Distraction-free
- **Vibrant**: Colorful and energetic
- **Galactic**: Space-themed (Web UI)

## 🤝 Contributing

1. Fork the repository
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open Pull Request

## 📄 License

MIT License - see [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- The Pomodoro Technique® by Francesco Cirillo
- Go community for excellent libraries

---

**🚀 Ready to boost your productivity? Start with `pom start` or `pom web`!**

**Built with ❤️ by Flack**
