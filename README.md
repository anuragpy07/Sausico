# Sausico

### A Modern, High-Performance JioSaavn Client

[![React Native](https://img.shields.io/badge/React%20Native-0.81-61DAFB?style=flat&logo=react&logoColor=white)](https://reactnative.dev/)
[![Expo](https://img.shields.io/badge/Expo-SDK%2054-000020?style=flat&logo=expo&logoColor=white)](https://expo.dev/)
[![License](https://img.shields.io/badge/License-MIT-green.svg?style=flat)](LICENSE)
[![Platform](https://img.shields.io/badge/Platform-Android-3DDC84?style=flat&logo=android&logoColor=white)](https://www.android.com/)

**Experience music streaming reimagined with cutting-edge technology and thoughtful design.**

🌐 **Website:** Coming soon

---

### 📌 Table of Contents

- [⬇ Download](#-download)
- [✨ Features](#-features)
- [🖼 Screenshots](#-screenshots)
- [⚡ Quick Start](#-quick-start)
- [🛠 Troubleshooting](#-troubleshooting)
- [⚖ Legal Notice](#-legal-notice)

---

## ⬇ Download

**Current Version:** `v1.0.1`

Choose the build that matches your device architecture.

| Build Variant | Device Compatibility | Download |
|---------------|---------------------|----------|
| **arm64-v8a** | Modern Android devices (2015+) | https://github.com/anuragpy07/Sausico/releases/download/v1.0.1/app-arm64-v8a-release.apk |
| **armeabi-v7a** | Older Android devices (pre-2015) | https://github.com/anuragpy07/Sausico/releases/download/v1.0.1/app-armeabi-v7a-release.apk |
| **x86_64** | Emulators and x86-based devices | https://github.com/anuragpy07/Sausico/releases/download/v1.0.1/app-x86_64-release.apk |
| **x86** | Legacy emulators | https://github.com/anuragpy07/Sausico/releases/download/v1.0.1/app-x86-release.apk |

> Download arm64-v8a first. If installation fails, try armeabi-v7a.

---

### Why Sausico?

- 🏗️ Production-ready architecture built for scale
- ⚡ Optimized performance using MMKV storage
- 🎨 Clean UI with smooth animations
- 🔊 Background playback & queue management
- 🧪 Modern stack (React Native + Expo)

---

## ✨ Features

### 🎧 Audio Experience
* Background audio playback with foreground service
* Seamless queue management (play next, add to queue)
* Full media controls (seek, skip, repeat, shuffle)
* Android lock-screen & notification controls
* Gapless playback support
* Audio focus handling

### 🔍 Discovery & Search
* Powerful search across songs, albums, artists, playlists
* Voice search with on-device speech recognition
* Curated home feed with personalized content
* Trending charts and new releases
* Genre-based browsing
* Smart recommendations

### 📚 Library Management
* Favorites and collections
* Listening history tracking
* Offline downloads support
* Custom playlist creation
* Recently played quick access
* Library sync and backup

### 🎨 UI & Design
* Dynamic color theming from album artwork
* Mini-player with gesture controls
* Immersive full-screen player
* Smooth transitions and animations
* Tablet-optimized layouts
* Dark mode support
* Global snackbar feedback system

---

## 📱 Screenshots

### 🎵 Core Experience
| Home Feed | Full Player | Downloads |
|:---:|:---:|:---:|
| ![Home Feed](assets/images/screenshots/home.png) | ![Full Player](assets/images/screenshots/full-player.png) | ![Downloads](assets/images/screenshots/downloads.png) |
| *Trending content and suggestions* | *Immersive playback experience* | *Offline content management* |

### 🔍 Search & Discovery
| Search Interface | Search Results | Voice Search |
|:---:|:---:|:---:|
| ![Search Interface](assets/images/screenshots/search-interface.png) | ![Search Results](assets/images/screenshots/search-results.png) | ![Voice Search](assets/images/screenshots/search-voice.png) |
| *Full text search over categories* | *Categorized results with quick filters* | *On-Device Voice Search* |

### 🎧 Media Details
| Album View | Artist Profile | Playlist View |
|:---:|:---:|:---:|
| ![Album View](assets/images/screenshots/details-album.png) | ![Artist Profile](assets/images/screenshots/details-artist.png) | ![Playlist View](assets/images/screenshots/details-playlist.png) |
| *Complete album information* | *Top tracks & discography* | *Curated & custom playlists* |

### 📚 Library & Collections
| Favorites | Collections | Custom Collection |
|:---:|:---:|:---:|
| ![Favorites](assets/images/screenshots/library-favorites.png) | ![Collections](assets/images/screenshots/library-collections-1.png) | ![Custom Collection](assets/images/screenshots/library-collections-2.png) |
| *Liked songs & albums* | *Organized library sections* | *User-defined music collections* |

### ⭐ Bonus Features
| Track Menu | Audio Quality | History |
|:---:|:---:|:---:|
| ![Track Menu](assets/images/screenshots/track-menu.png) | ![Audio Quality](assets/images/screenshots/audio-quality.png) | ![History](assets/images/screenshots/history.png) |
| *Context menu with rich actions* | *High fidelity playback options* | *List of recently played tracks* |

---

## 🚀 Quick Start

### Prerequisites
Before you begin, ensure you have the following installed:

| Requirement | Version | Download |
|---|---|---|
| Node.js | 18.x or higher | [nodejs.org](https://nodejs.org/) |
| Java JDK | 17 (recommended) | [Oracle JDK](https://www.oracle.com/java/technologies/downloads/) |
| Android SDK | Latest | Via Android Studio |
| Android Device/Emulator | API 21+ | Android Studio |

> ⚠️ **Important Notice** > This project uses native modules and cannot run in **Expo Go**. You must build and run a development client.

### 💻 Installation

```bash
# 1. Clone the repository
git clone [https://github.com/anuragpy07/Sausico.git](https://github.com/anuragpy07/Sausico.git)
cd Sausico

# 2. Install dependencies (Choose one)
npm install
# OR yarn install
# OR bun install

# 3. Build and run development client
# Build and install on connected Android device/emulator
npm run android

# Start the Metro bundler
npx expo start --dev-client

# 4. Launch the app
# Open the installed development client on your device and it will automatically connect to Metro.
```

🐛 Troubleshooting
Common Issues

```bash
# ==========================================
# 1. App crashes on launch
# ==========================================
# Rebuild the development client
npm run android
# Clear Metro cache
npx expo start -c

# ==========================================
# 2. No audio playback
# ==========================================
# Possible causes: Development client not properly installed, Android audio focus not granted, or Service not registered in AndroidManifest.xml.
# Reinstall with clean build
cd android && ./gradlew clean
cd .. && npm run android

# ==========================================
# 3. Build errors with Gradle
# ==========================================
# Clean Gradle cache
cd android
./gradlew clean
rm -rf .gradle
cd ..
# Rebuild
npm run android

# ==========================================
# 4. Metro bundler issues
# ==========================================
# Clear all caches
npx expo start -c
watchman watch-del-all  # If using watchman
rm -rf node_modules && npm install
```
📄 Legal Notice
This is an unofficial application.

• Not affiliated with, endorsed by, or connected to JioSaavn

• Does not host, store, or redistribute any copyrighted content

• All media data and URLs are fetched from publicly accessible APIs

• Usage compliance is the sole responsibility of the end user

• This project is intended for educational and personal use only. Please respect copyright laws and support artists by using official platforms.

---

🤝 Contributing

Feel free to open issues or submit pull requests for improvements.

---

📜 License
MIT © 2026 Anurag Kumar

See **LICENSE** for details.

Built by Anurag Kumar with a focus on correctness and longevity.

## ⭐ Support

If you like this project, consider giving it a ⭐ on GitHub — it really helps!

Also, feel free to **follow me on GitHub** for more projects and updates:
👉 https://github.com/anuragpy07
