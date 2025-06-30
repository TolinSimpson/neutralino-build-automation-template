# Build Automation Scripts

This folder contains all the build automation scripts and documentation for cross-platform deployment of Homestead Tools.

## 📁 Contents

### Build Scripts
- **`build-mac-enhanced.sh`** - Complete macOS app bundle and DMG creation
- **`build-linux-enhanced.sh`** - Linux packaging (AppImage, DEB, RPM)
- **`setup-macos-signing.sh`** - Apple Developer signing setup (optional)

### Processing Scripts
- **`preproc-linux.sh`** / **`postproc-linux.sh`** - Linux build customization
- **`preproc-mac.sh`** / **`postproc-mac.sh`** - macOS build customization

### Documentation
- **`GITHUB_ACTIONS_SETUP.md`** - Complete GitHub Actions setup and troubleshooting guide

## 🚀 Quick Usage

### For GitHub Actions (Automated)
All scripts are automatically called by the workflows in `.github/workflows/`. No manual intervention needed.

### For Local Development

#### macOS Build
```bash
chmod +x build-mac-enhanced.sh
./build-mac-enhanced.sh --dmg
```

#### Linux Build
```bash
chmod +x build-linux-enhanced.sh
./build-linux-enhanced.sh --appimage --deb --rpm
```

#### Windows Build
Use Inno Setup to compile `HomesteadTools.iss` in the project root.

## 📖 Documentation

See **`GITHUB_ACTIONS_SETUP.md`** for:
- Complete setup instructions
- Troubleshooting guide
- Release process
- Platform-specific configurations

## 🔧 Requirements

### macOS
- macOS 10.13+ (for building)
- Xcode Command Line Tools
- Node.js 18+
- Homebrew packages: `jq`, `create-dmg`

### Linux
- Ubuntu 18.04+ or equivalent
- Node.js 18+
- Build tools: `build-essential`, `fuse`, `rpm`, `alien`

### Windows
- Windows 10+ with PowerShell
- Node.js 18+
- Inno Setup 6+

---

**Note**: All dependencies are automatically installed by GitHub Actions workflows. Local installation is only needed for manual testing. 