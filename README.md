# TutorLog 📚

A modern Android application for tutors to manage students, track progress, and organize tutoring sessions built with Jetpack Compose and Clean Architecture.

## 📱 Features

- **Google Sign-In Authentication** - Secure login using Google OAuth
- **Student Management** - Add, view, and organize students
- **Group Management** - Organize students into groups
- **Home Dashboard** - Overview of tutoring activities
- **Modern UI** - Built with Jetpack Compose and Material Design 3
- **Edge-to-Edge Display** - Immersive full-screen experience

## 🏗️ Architecture

This project follows Clean Architecture principles with MVI (Model-View-Intent) pattern:

- **Presentation Layer**: Jetpack Compose UI with ViewModels
- **Domain Layer**: Use cases and business logic
- **Data Layer**: Repositories and data sources

### Tech Stack

- **UI Framework**: Jetpack Compose
- **Navigation**: Compose Destinations
- **Dependency Injection**: Dagger Hilt
- **State Management**: Orbit MVI
- **Networking**: Retrofit + OkHttp
- **Authentication**: Firebase Auth + Google Sign-In
- **Image Loading**: Coil
- **Async**: Kotlin Coroutines + Flow
- **Build System**: Gradle (Kotlin DSL)

## 📋 Prerequisites

- Android Studio Ladybug or newer
- JDK 11 or higher
- Android SDK (API 24+)
- Google Services configuration file (`google-services.json`)

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/tutorLog.git
cd tutorLog
```

### 2. Setup Firebase

1. Go to [Firebase Console](https://console.firebase.google.com/)
2. Create a new project or use an existing one
3. Add an Android app with package name: `com.example.tutorlog`
4. Download `google-services.json` and place it in the `app/` directory
5. Enable Google Sign-In in Firebase Authentication

### 3. Build and Run

```bash
./gradlew clean build
./gradlew installDebug
```

Or simply open the project in Android Studio and click Run.

## 📦 Project Structure

```
app/
├── src/main/java/com/example/tutorlog/
│   ├── MainActivity.kt                 # Entry point
│   ├── TutorLogApplication.kt         # Application class
│   ├── feature/                       # Feature modules
│   │   ├── login/                    # Login feature
│   │   │   ├── LoginScreen.kt
│   │   │   ├── LoginViewModel.kt
│   │   │   └── LoginScreenState.kt
│   │   ├── home/                     # Home dashboard
│   │   │   ├── HomeScreen.kt
│   │   │   ├── HomeViewModel.kt
│   │   │   └── composables/
│   │   └── students/                 # Student management
│   │       ├── StudentScreen.kt
│   │       ├── StudentViewModel.kt
│   │       └── composables/
│   ├── domain/                       # Business logic
│   │   ├── usecase/                 # Use cases
│   │   ├── PreferencesManager.kt    # Local storage
│   │   └── types/                   # Domain models
│   ├── repository/                   # Data repositories
│   ├── service/                      # API services
│   ├── design/                       # Design system
│   │   └── theme/                   # Theme configuration
│   └── utils/                        # Utility classes
└── res/                              # Resources
```

## 🎨 Key Components

### Authentication Flow

1. **Login Screen**: Google Sign-In integration
2. **User Creation**: Store user data locally and in Firebase
3. **Session Management**: Persist user session with SharedPreferences

### Home Dashboard

- User profile display
- Quick access to students
- Navigation to different sections
- Bottom navigation bar

### Student Management

- View all students
- Organize students into groups
- Add new students
- Toggle between individual and group views

## 🔧 Configuration

### Minimum SDK Requirements

- **minSdk**: 24 (Android 7.0)
- **targetSdk**: 35 (Android 15)
- **compileSdk**: 35

### Version Catalog (libs.versions.toml)

Dependencies are managed using Gradle Version Catalog. Key dependencies:

```toml
[versions]
kotlin = "2.0.21"
compose-bom = "2024.12.01"
hilt = "2.51.1"
retrofit = "2.9.0"
orbit = "10.0.0"
```

## 🎨 Design System

The app uses a custom design system with:

- **Color Palette**: Dark theme optimized
- **Typography**: Custom text styles
- **Components**: Reusable composable components
- **LocalColors**: Compose local provider for consistent theming

## 📱 Screens

### 1. Login Screen
- Google Sign-In button
- Loading state with progress indicator
- Edge-to-edge design with transparent system bars

### 2. Home Screen
- User profile section
- Recent activity overview
- Quick navigation to students
- Bottom navigation bar

### 3. Student Screen
- Toggle between students and groups view
- Floating action button to add new entries
- List/Grid view of students
- Bottom navigation

## 🔐 Security

- Firebase Authentication for secure login
- Secure token management
- No hardcoded credentials
- ProGuard rules for release builds

## 🚧 Known Issues & Limitations

- Backend API integration is in progress
- Some features are under development
- Limited offline support

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👨‍💻 Author

**Samarth Raj**

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📞 Support

For support, email mailforsamarth@gmail.com or open an issue in the repository.

## 🙏 Acknowledgments

- [Jetpack Compose](https://developer.android.com/jetpack/compose)
- [Compose Destinations](https://github.com/raamcosta/compose-destinations)
- [Orbit MVI](https://github.com/orbit-mvi/orbit-mvi)
- [Firebase](https://firebase.google.com/)
- [Dagger Hilt](https://dagger.dev/hilt/)

---

Made with ❤️ using Jetpack Compose

