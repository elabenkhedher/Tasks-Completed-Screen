# Task Completed Screen ✅

[![Kotlin](https://img.shields.io/badge/Kotlin-2.2.10-7F52FF?logo=kotlin&logoColor=white)](https://kotlinlang.org/)
[![Jetpack Compose](https://img.shields.io/badge/Jetpack%20Compose-BOM%202026.02.01-4285F4?logo=jetpackcompose&logoColor=white)](https://developer.android.com/jetpack/compose)
[![Material 3](https://img.shields.io/badge/Material%203-Enabled-795548?logo=materialdesign&logoColor=white)](https://m3.material.io/)
[![Android Min SDK](https://img.shields.io/badge/Min%20SDK-24-3DDC84?logo=android&logoColor=white)](https://developer.android.com/)
[![Target SDK](https://img.shields.io/badge/Target%20SDK-37-3DDC84?logo=android&logoColor=white)](https://developer.android.com/)

A clean, modern Android application demonstrating layout arrangement and declarative UI building using **Jetpack Compose**. This project is part of the **[Android Basics with Compose](https://developer.android.com/courses/android-basics-compose/course)** curriculum by Google.

---

## 📱 Preview

<div align="center">
  <img src="app/src/main/res/drawable-nodpi/ic_task_completed.png" width="140" alt="Task Completed Checkmark" />
  <br/><br/>
  <h3><b>All tasks completed</b></h3>
  <p><i>Nice work!</i></p>
</div>

---

## 🎯 About The Project

This practice project focuses on mastering fundamental Jetpack Compose concepts, specifically building a centered completion feedback screen with proper vertical/horizontal alignment, typography styling, and asset integration.

### Core Objectives:
- Learn how to structure UI components using `Column`, `Arrangement`, and `Alignment`.
- Implement responsive centering for both horizontal and vertical axes across varying screen sizes.
- Load and render local drawable resources with `Image` and `painterResource`.
- Apply text styling including custom font weights (`FontWeight.Bold`), font sizing (`sp`), and directional padding (`dp`).
- Enable edge-to-edge system display (`enableEdgeToEdge()`) for a modern Android UI feel.

---

## 🛠️ Tech Stack & Architecture

- **Language:** [Kotlin](https://kotlinlang.org/) (v2.2.10)
- **UI Framework:** [Jetpack Compose](https://developer.android.com/jetpack/compose) with Compose Compiler
- **Design System:** [Material Design 3 (M3)](https://m3.material.io/)
- **Build System:** Gradle Kotlin DSL (`build.gradle.kts`) with Gradle Version Catalogs (`libs.versions.toml`)
- **Compatibility:**
  - **Min SDK:** API 24 (Android 7.0 Nougat)
  - **Target / Compile SDK:** API 37

---

## 📂 Project Structure

```text
MyApplication/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/example/myapplication/
│   │   │   │   ├── MainActivity.kt        # Main entry point & Compose UI implementation
│   │   │   │   └── ui/theme/              # Material 3 Theme, Typography, and Colors
│   │   │   │       ├── Color.kt
│   │   │   │       ├── Theme.kt
│   │   │   │       └── Type.kt
│   │   │   ├── res/
│   │   │   │   └── drawable-nodpi/        # Graphical assets (ic_task_completed.png)
│   │   │   └── AndroidManifest.xml
│   └── build.gradle.kts                   # App module build configuration
├── gradle/
│   └── libs.versions.toml                 # Version catalog dependency management
├── build.gradle.kts                       # Root build configuration
└── README.md
```

---

## 💡 Code Overview

The UI is built with a single, reusable Composable function centered in the viewport:

```kotlin
@Composable
fun task(modifier: Modifier = Modifier) {
    Column(
        verticalArrangement = Arrangement.Center,
        horizontalAlignment = Alignment.CenterHorizontally
    ) {
        Image(
            painter = painterResource(id = R.drawable.ic_task_completed),
            contentDescription = null
        )
        Text(
            text = "All tasks completed",
            modifier = Modifier.padding(top = 24.dp, bottom = 8.dp),
            fontWeight = FontWeight.Bold
        )
        Text(
            text = "Nice work!",
            fontSize = 16.sp
        )
    }
}
```

---

## 🚀 Getting Started

### Prerequisites

- **[Android Studio](https://developer.android.com/studio)** (Ladybug | Meerkat or newer recommended)
- **JDK 11** or higher
- Android SDK with API 37 installed

### Installation & Run

1. **Clone the repository:**
   ```bash
   git clone https://github.com/elabenkhedher/Task-Completed-Screen-Android-Google-Course.git
   cd Task-Completed-Screen-Android-Google-Course
   ```

2. **Open in Android Studio:**
   - Launch Android Studio.
   - Select **Open** and select the cloned project root folder.
   - Wait for Gradle sync to complete.

3. **Run the App:**
   - Select an emulator or connected physical device.
   - Click the green **Run** ▶️ button (or press `Shift + F10`).

4. **Command Line Build (Optional):**
   ```bash
   ./gradlew assembleDebug
   ```

---

## 📚 Acknowledgments & References

- [Android Basics with Compose Course](https://developer.android.com/courses/android-basics-compose/course) by Google
- [Compose Layouts Documentation](https://developer.android.com/jetpack/compose/layouts)

---

## 👤 Author

**Ela Ben Khedher**
- GitHub: [@elabenkhedher](https://github.com/elabenkhedher)
