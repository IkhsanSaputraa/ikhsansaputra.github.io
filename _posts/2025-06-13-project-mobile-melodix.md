---
title : Melodix - Aplikasi Pemutar Musik Android 🎵
description: Melodix adalah aplikasi pemutar musik Android modern yang mengintegrasikan API Deezer untuk streaming musik. Aplikasi ini dikembangkan menggunakan Java dan menyediakan pengalaman mendengarkan musik yang komprehensif dengan fitur autentikasi, pencarian musik, favorit, dan download offline.
author: Kevin Ardhana
date: 2025-06-13
categories: [Mobile, Java, Android ]
Tag: [Java, Android Studio]
image:
    path: /assets/img/logomelodix.png
    lqip: data:image/webp;base64,UklGRpoAAABXRUJQVlA4WAoAAAAQAAAADwAABwAAQUxQSDIAAAARL0AmbZurmr57yyIiqE8oiG0bejIYEQTgqiDA9vqnsUSI6H+oAERp2HZ65qP/VIAWAFZQOCBCAAAA8AEAnQEqEAAIAAVAfCWkAALp8sF8rgRgAP7o9FDvMCkMde9PK7euH5M1m6VWoDXf2FkP3BqV0ZYbO6NA/VFIAAAA
    alt: Logo Melodix.
---

# Melodix - Aplikasi Pemutar Musik Android 🎵

## 1. Ringkasan Project

Melodix adalah aplikasi pemutar musik Android modern yang mengintegrasikan API Deezer untuk streaming musik. Aplikasi ini dikembangkan menggunakan Java dan menyediakan pengalaman mendengarkan musik yang komprehensif dengan fitur autentikasi, pencarian musik, favorit, dan download offline.

## 2. Tujuan Aplikasi

- Menyediakan platform streaming musik yang mudah digunakan
- Mengintegrasikan layanan musik populer (Deezer API)
- Memberikan pengalaman pengguna yang seamless dengan autentikasi Firebase
- Memungkinkan pengguna menyimpan musik favorit dan mengunduh untuk offline
- Menyediakan interface yang responsif dengan dukungan tema terang dan gelap

## 3. Teknologi yang Digunakan

### Backend & API:
- **Java** - Bahasa pemrograman utama (100%)
- **Firebase Authentication** - Sistem autentikasi pengguna
- **Firebase Firestore** - Database cloud untuk menyimpan data pengguna
- **Deezer API** - API streaming musik
- **SQLite** - Database lokal untuk musik yang diunduh

### Libraries & Framework:
- **Retrofit** - HTTP client untuk API calls
- **Gson** - JSON serialization/deserialization
- **Glide** - Image loading dan caching
- **OkHttp** - HTTP client
- **Material Design Components** - UI components
- **RecyclerView** - List management
- **MediaPlayer** - Audio playback

### Development Tools:
- **Android Studio** - IDE
- **Gradle** - Build system

## 4. Struktur Proyek

```
app/src/main/java/com/example/melodix/
├── activity/           # Activities
│   ├── MainActivity.java
│   ├── SplashActivity.java
│   ├── LoginActivity.java
│   ├── SignUpActivity.java
│   ├── ForgotPasswordActivity.java
│   ├── SetNewPasswordActivity.java
│   └── ProfileActivity.java
├── fragment/           # Fragments
│   ├── HomeFragment.java
│   ├── FavoriteFragment.java
│   └── DownloadFragment.java
├── adapter/            # RecyclerView Adapters
│   ├── NewMusicAdapter.java
│   ├── FavoriteAdapter.java
│   ├── SearchResultAdapter.java
│   └── RecentlyPlayedAdapter.java
├── model/              # Data Models
│   ├── Track.java
│   ├── Artist.java
│   ├── Album.java
│   └── SearchResponse.java
├── api/                # API Integration
│   ├── DeezerApiClient.java
│   ├── DeezerApiService.java
│   └── DeezerRepository.java
├── listener/           # Utilities & Managers
│   ├── MusicPlayer.java
│   ├── MusicDownloader.java
│   ├── ThemeManager.java
│   └── UserPreferencesManager.java
└── database/           # Local Database
    ├── DownloadedMusicDbHelper.java
    └── DownloadedMusicContract.java
```

## 5. Fitur-Fitur Aplikasi

### 🔐 Autentikasi & Profil
- Login/Register dengan Firebase Authentication
- Reset password via email
- Manajemen profil pengguna
- Logout dengan konfirmasi

### 🎵 Pemutar Musik
- Streaming musik melalui Deezer API
- Kontrol playback (play, pause, skip, previous)
- Progress bar dengan seek functionality
- Background audio playback
- Auto-play next track

### 🔍 Pencarian & Penemuan
- Pencarian real-time musik, artis, dan album
- Filter hasil pencarian berdasarkan kategori
- Discover musik baru dan trending
- Recently played tracks

### ❤️ Favorit & Koleksi
- Tambah/hapus musik ke/dari favorit
- Sinkronisasi favorit dengan cloud (Firebase)
- Kelola daftar musik favorit
- Quick access ke musik yang sering diputar

### 📱 Download & Offline
- Download musik untuk offline listening
- Manajemen file download
- Local storage dengan SQLite database
- Progress tracking saat download

### 🎨 Antarmuka & Tema
- Material Design interface
- Dark mode dan light mode
- Responsive design untuk berbagai ukuran layar
- Smooth animations dan transitions

### 🔧 Fitur Tambahan
- Splash screen dengan auto-login
- Error handling yang komprehensif
- Network state monitoring
- User preferences management

## 6. Tampilan Aplikasi

### Splash Screen
<img src="/Screenshots/splash_screen.jpeg" width="300" alt="Splash Screen">

### Login & Registration
<img src="/Screenshots/login.jpeg" width="300" alt="Login Screen"/>

### Home Screen
<img src="/Screenshots/homescreen.jpeg" width="300" alt="Home Screen"/>

### Music Player
<img src="/Screenshots/musicPlayer.jpeg" width="300" alt="Music Player"/>

### Favorites
<img src="/Screenshots/favorite.jpeg" width="300" alt="Favorite Screen"/>

### Profile & Settings
<img src="/Screenshots/profile.jpeg" width="300" alt="Profile Screen"/>

## 7. Instalasi & Menjalankan Proyek

### Prasyarat
- Android Studio Arctic Fox atau lebih baru
- JDK 11 atau lebih baru
- Android SDK API Level 21+ (Android 5.0+)
- Akun Firebase dan Deezer Developer

### Langkah Instalasi

1. **Clone Repository**
   ```bash
   git clone https://github.com/Kevinardhana096/Melodix.git
   cd Melodix1
   ```

2. **Setup Firebase**
   - Buat project baru di [Firebase Console](https://console.firebase.google.com/)
   - Aktifkan Authentication dan Firestore
   - Download file `google-services.json`
   - Letakkan file tersebut di folder `app/`

3. **Setup Deezer API**
   - Daftar di [Deezer Developers](https://developers.deezer.com/)
   - Dapatkan Application ID
   - Update `AndroidManifest.xml`:
     ```xml
     <meta-data
         android:name="deezer.applicationId"
         android:value="YOUR_DEEZER_APPLICATION_ID" />
     ```

4. **Konfigurasi Facebook SDK** (Opsional)
   - Buat app di [Facebook Developers](https://developers.facebook.com/)
   - Tambahkan App ID ke `strings.xml`:
     ```xml
     <string name="facebook_app_id">YOUR_FACEBOOK_APP_ID</string>
     <string name="facebook_client_token">YOUR_FACEBOOK_CLIENT_TOKEN</string>
     ```

5. **Build Project**
   - Buka project di Android Studio
   - Sync Gradle files
   - Build dan jalankan aplikasi

### Menjalankan Aplikasi

1. **Development Mode**
   ```bash
   ./gradlew assembleDebug
   adb install app/build/outputs/apk/debug/app-debug.apk
   ```

2. **Release Mode**
   ```bash
   ./gradlew assembleRelease
   ```

## 8. Arsitektur Aplikasi

### Design Pattern
- **MVP (Model-View-Presenter)** - Pemisahan logic dan UI
- **Repository Pattern** - Abstraksi data layer
- **Singleton Pattern** - Untuk shared instances (API client, preferences)

### Data Flow
```
UI Layer (Activities/Fragments) 
    ↓
Adapter Layer (RecyclerView Adapters)
    ↓
Repository Layer (Data Management)
    ↓
API/Database Layer (Deezer API, Firebase, SQLite)
```

### Threading Model
- **Main Thread** - UI operations
- **Background Thread** - API calls dan database operations
- **AsyncTask/ExecutorService** - Heavy operations

## 9. API Documentation

### Deezer API Endpoints
```java
// Search music
GET /search?q={query}&type=track

// Get track details
GET /track/{id}

// Get artist info
GET /artist/{id}

// Get album tracks
GET /album/{id}/tracks
```

### Firebase Collections
```
users/
├── {userId}/
│   ├── profile: {name, email, avatar}
│   ├── favorites: [trackId1, trackId2, ...]
│   └── playlists: [{id, name, tracks}, ...]
```

## 10. Testing & Quality Assurance

### Unit Testing
- Model validation tests
- API response parsing tests
- Database operation tests

### Integration Testing
- Authentication flow testing
- Music playback testing
- Download functionality testing

### UI Testing
- User interface responsiveness
- Navigation flow testing
- Error state handling

### Performance Testing
- Memory usage optimization
- Battery consumption analysis
- Network efficiency testing

## 11. Security & Privacy

### Data Protection
- User authentication via Firebase
- Secure API key management
- Local data encryption
- Network traffic encryption (HTTPS)

### Privacy Features
- User data anonymization
- Optional data collection
- Clear privacy policy
- GDPR compliance considerations

### Security Measures
- Input validation
- SQL injection prevention
- API rate limiting
- Secure file storage

## 12. Performance Optimization

### Memory Management
- Image caching dengan Glide
- Lazy loading untuk RecyclerView
- Proper lifecycle management
- Memory leak prevention

### Network Optimization
- Request caching
- Offline mode implementation
- Progressive loading
- Retry mechanisms

### Battery Optimization
- Background service optimization
- Wake lock management
- Efficient audio codec usage
- Power-aware networking

## 13. Deployment & Distribution

### Build Configuration
```gradle
android {
    compileSdkVersion 34
    defaultConfig {
        minSdkVersion 21
        targetSdkVersion 34
        versionCode 1
        versionName "1.0.0"
    }
    buildTypes {
        release {
            minifyEnabled true
            proguardFiles getDefaultProguardFile('proguard-android.txt')
        }
    }
}
```

### Release Checklist
- [ ] Code review dan testing
- [ ] Performance profiling
- [ ] Security audit
- [ ] API key configuration
- [ ] Signing configuration
- [ ] Store listing preparation

## 14. Future Enhancements

### Planned Features
- **Social Features**
  - Share musik ke social media
  - Follow friends dan lihat aktivitas mereka
  - Collaborative playlists

- **Advanced Audio**
  - Equalizer dengan preset
  - Audio effects (reverb, bass boost)
  - Crossfade antar track
  - Sleep timer

- **Smart Features**
  - Machine learning untuk rekomendasi
  - Voice control integration
  - Smart playlists berdasarkan mood
  - Location-based music suggestions

- **Platform Expansion**
  - Android Auto support
  - Wear OS companion app
  - Chromecast integration
  - Smart TV app

### Technical Improvements
- Migration ke Kotlin
- Implementation of MVVM dengan LiveData
- Room database migration
- Jetpack Compose UI
- Modular architecture

## 15. Known Issues & Limitations

### Current Limitations
- Terbatas pada Deezer API preview (30 detik)
- Download feature tergantung pada Deezer terms
- Tidak mendukung podcast atau audiobook
- Offline mode terbatas pada musik yang sudah didownload

### Bug Reports
- Memory leak pada prolonged usage (investigating)
- Occasional crash pada network interruption (fixed in v1.0.1)
- UI glitches pada beberapa device dengan notch (workaround available)

### Performance Issues
- Slow loading pada koneksi internet lambat
- High battery consumption pada background playback
- Large APK size due to dependencies

## 16. Troubleshooting Guide

### Common Issues

**App Crash saat Login**
```
Solution: 
1. Check Firebase configuration
2. Verify google-services.json file
3. Clear app data dan restart
```

**Musik tidak bisa diputar**
```
Solution:
1. Check internet connection
2. Verify Deezer API status
3. Check audio permission
4. Restart app
```

**Download gagal**
```
Solution:
1. Check storage permission
2. Verify available storage space
3. Check network stability
4. Clear download cache
```

### Debug Commands
```bash
# Clear app data
adb shell pm clear com.example.melodix

# Check logs
adb logcat | grep "Melodix"

# Monitor memory usage
adb shell dumpsys meminfo com.example.melodix

# Check network usage
adb shell cat /proc/net/xt_qtaguid/stats | grep $(adb shell ps | grep melodix | awk '{print $2}')
```

## 17. Contributing Guidelines

### Development Setup
1. Fork repository
2. Create feature branch
3. Follow coding standards
4. Write tests for new features
5. Update documentation
6. Submit pull request

### Code Style
- Follow Java naming conventions
- Use meaningful variable names
- Add comments untuk complex logic
- Maintain consistent indentation
- Use proper access modifiers

### Commit Messages
```
feat: add new search filter functionality
fix: resolve memory leak in music player
docs: update API documentation
style: format code according to guidelines
refactor: improve database query performance
test: add unit tests for authentication
```

## 18. Support & Community

### Getting Help
- **GitHub Issues** - Bug reports dan feature requests
- **Documentation** - Comprehensive guides dan tutorials
- **Stack Overflow** - Tag dengan `melodix-android`
- **Email Support** - kevinardhana096@gmail.com

### Community Guidelines
- Be respectful dan constructive
- Search existing issues sebelum create new one
- Provide detailed information untuk bug reports
- Follow template untuk feature requests

## 19. Acknowledgments

### Third-Party Libraries
- **Deezer SDK** - Music streaming capabilities
- **Firebase** - Authentication dan cloud services
- **Retrofit** - Network operations
- **Glide** - Image loading dan caching
- **Material Components** - UI design system

### Inspiration
- Spotify - UI/UX design inspiration
- Google Play Music - Feature inspiration
- Apple Music - Design patterns

### Contributors
- Kevin Ardhana (@kevinardhana096) - Main Developer
- Open source community - Bug reports dan suggestions

## 20. License & Legal

### MIT License
```
MIT License

Copyright (c) 2025 Kevin Ardhana

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

### Third-Party Licenses
- Deezer API - [Deezer Terms of Use](https://www.deezer.com/legal/cgu)
- Firebase - [Google Terms of Service](https://policies.google.com/terms)
- Material Design Icons - [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)

### Disclaimer
This application is for educational purposes. Music content is provided by Deezer and subject to their terms of service. Users are responsible for complying with applicable copyright laws.

---

## Kontak

**Developer:** Kevin Ardhana  
**GitHub:** [@kevinardhana096](https://github.com/kevinardhana096)  
**Repository:** [Melodix](https://github.com/kevinardhana096/Melodix)  
**Email:** kevinardhana096@gmail.com  

---

*Melodix - Your Music, Your Way* 🎵

**"Music is the universal language of mankind"** - Henry Wadsworth Longfellow