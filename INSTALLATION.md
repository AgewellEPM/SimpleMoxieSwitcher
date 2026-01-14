# Installation Guide

## macOS Installation

### Requirements
- macOS 13.0 (Ventura) or later
- 8GB RAM (16GB recommended)
- 10GB free disk space
- Internet connection

### Steps

1. **Download**
   - Visit [openmoxie.org/download](https://openmoxie.org/download)
   - Click "Download for Mac"
   - Save `SimpleMoxieSwitcher-1.0.0.dmg`

2. **Install**
   - Open the downloaded .dmg file
   - Drag SimpleMoxieSwitcher to Applications folder
   - Eject the disk image

3. **First Launch**
   - Open Applications folder
   - Right-click SimpleMoxieSwitcher
   - Click "Open" (required for first launch)
   - Click "Open" in security dialog

4. **Setup Wizard**
   - Follow the automated setup wizard
   - Docker Desktop will be installed
   - Mosquitto MQTT broker will be configured
   - OpenMoxie backend will be set up

5. **Configuration**
   - Enter your OpenAI API key
   - Set up parental controls (optional)
   - Connect your Moxie robot

## Windows Installation

### Requirements
- Windows 10 (build 19041 or later) or Windows 11
- .NET 8.0 Runtime (installer will prompt if missing)
- 8GB RAM (16GB recommended)
- 10GB free disk space
- Internet connection

### Steps

1. **Download**
   - Visit Our Google Drive At OpenMoxie 2.0 (https://drive.google.com/drive/folders/1p0NC8dvroVD-c8QP2NGTh3dVX00wDVhr?usp=drive_link)
   - Click "Download for Windows"
   - Save `SimpleMoxieSwitcher-Setup.exe`

2. **Install**
   - Run `SimpleMoxieSwitcher-Setup.exe`
   - Click "Yes" if User Account Control prompts
   - Follow installation wizard
   - Choose installation directory (default recommended)

3. **Dependencies**
   - Installer will check for .NET 8.0 Runtime
   - If missing, follow prompts to install
   - Docker Desktop installation will be offered

4. **Setup Wizard**
   - Launch SimpleMoxieSwitcher
   - Follow automated setup
   - Docker and Mosquitto will be configured
   - OpenMoxie backend will be installed

5. **Configuration**
   - Enter your OpenAI API key
   - Set up parental controls (optional)
   - Connect your Moxie robot

## iOS Installation

### Requirements
- iPhone or iPad with iOS 16.0 or later
- Desktop app (Mac or Windows) already running
- Same WiFi network as desktop

### Steps

1. **Install TestFlight**
   - Open App Store on your iPhone/iPad
   - Search "TestFlight"
   - Install TestFlight (free from Apple)

2. **Join Beta**
   - Visit [openmoxie.org/download](https://openmoxie.org/download)
   - Tap "Get iOS App"
   - Tap "Start Testing" in TestFlight
   - Tap "Install"

3. **Configure**
   - Open MoxieRemote app
   - Tap Settings (gear icon)
   - Enter your desktop computer's IP address
   - Tap "Save"

4. **Connect**
   - Tap "Connect" button
   - Should show "Connected to Server"
   - Test by sending a message to Moxie

### Finding Your Computer's IP

**Mac:**
```bash
ifconfig | grep "inet " | grep -v 127.0.0.1
```

**Windows:**
```cmd
ipconfig
```
Look for "IPv4 Address" under your WiFi adapter.

## Troubleshooting

### macOS: "App can't be opened because Apple cannot check it"
1. Open System Preferences → Security & Privacy
2. Click "Open Anyway" button
3. Re-launch the app

### Windows: .NET Runtime Missing
1. Installer will prompt automatically
2. Click "Download .NET Runtime"
3. Install and restart SimpleMoxieSwitcher

### Docker Issues
1. Ensure Docker Desktop is running
2. Check Docker icon in system tray
3. Restart Docker Desktop if needed

### Moxie Not Connecting
1. Ensure Moxie is on same WiFi network
2. Check MQTT broker is running: `brew services list | grep mosquitto` (Mac)
3. Verify OpenMoxie container: `docker ps`
4. Restart SimpleMoxieSwitcher

### iOS Can't Connect
1. Verify desktop app is running
2. Check IP address is correct
3. Ensure iPhone and computer on same WiFi
4. Try disabling VPN if enabled

## Getting Help

- 📖 [Full Documentation](https://openmoxie.org/docs)
- 💬 [Community Forum](https://openmoxie.org/community)
- 📧 [Email Support](mailto:support@openmoxie.org)
