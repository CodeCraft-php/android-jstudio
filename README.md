# android-jstudio
A Claude skill for creating and structuring Android projects with JStudio — the Android IDE that runs directly on your Android device.
---
name: jstudio
description: >
  Guide for creating, configuring, and structuring Android projects with JStudio — an Android IDE
  that runs directly on an Android device. Use this skill whenever the user mentions JStudio,
  creating an Android project on mobile, Android project structure, or asks for help with
  MainActivity, AndroidManifest, build.gradle.kts, or Android templates in JStudio. Also triggers
  for any question about Kotlin DSL, res/, layout/, or values/ folders in a JStudio project context.
---

# JStudio — Android Development on Android

JStudio lets you create and edit Android projects directly from an Android device,
with a project structure identical to Android Studio.

---

## Creating a New Project

**Main menu → + New → Android → Project**

### Available Templates

| Template | Recommended Use |
|---|---|
| **Empty Activity** | ✅ Best choice for beginners |
| No Activity | Project with no UI |
| Basic Views Activity | UI with AppBar and FAB |
| Bottom Navigation Views Activity | Bottom tab navigation |
| Empty Views Activity | Simple empty view |
| Navigation Drawer Views Activity | Side drawer menu |
| Responsive Views Activity | Multi-screen adaptive layout |

---

## Project Configuration

| Field | Description |
|---|---|
| **Name** | Application name |
| **Package** | Unique identifier (e.g. `com.yourname.yourapp`) |
| **Location** | Project creation folder |
| **Language** | Kotlin (recommended) or Java |
| **Minimum SDK** | Minimum supported Android version |
| **Build Configuration Language** | Kotlin DSL `.kts` (recommended) or Groovy DSL |

### ✅ Modern Best Practices
- Language: **Kotlin**
- Build config: **Kotlin DSL** (`build.gradle.kts`)

---

## Generated Project Structure

```
ProjectName/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/package/name/
│   │   │   │   └── MainActivity.kt          ← app entry point
│   │   │   ├── res/
│   │   │   │   ├── drawable/
│   │   │   │   ├── layout/
│   │   │   │   │   └── activity_main.xml    ← UI layout
│   │   │   │   ├── mipmap/                  ← app icons
│   │   │   │   ├── values/                  ← strings, colors, themes
│   │   │   │   └── values-night/            ← dark theme
│   │   │   └── AndroidManifest.xml          ← global config
│   │   ├── androidTest/
│   │   └── test/
│   ├── build.gradle.kts                     ← module dependencies
│   └── proguard-rules.pro
├── build.gradle.kts                         ← root Gradle config
├── gradle.properties
├── settings.gradle.kts
└── gradlew / gradlew.bat
```

---

## Key Files

### `MainActivity.kt`
```
app/src/main/java/package/name/MainActivity.kt
```
The app's entry point. **First file to edit** when adding logic.

### `activity_main.xml`
```
app/src/main/res/layout/activity_main.xml
```
The UI layout for the main activity. Defines visual components:
`TextView`, `Button`, `ImageView`, `RecyclerView`, etc.

### `AndroidManifest.xml`
```
app/src/main/AndroidManifest.xml
```
Global app configuration:
- Activity declarations
- Permissions (Internet, Camera, etc.)
- App metadata

### `res/values/`
- `strings.xml` — all app text
- `colors.xml` — color palette
- `themes.xml` — themes and styles

### `build.gradle.kts` (app module)
Used to add **dependencies** (external libraries).

---

## Next Steps After Project Creation

1. **Edit the UI** → `res/layout/activity_main.xml`
2. **Add logic** → `MainActivity.kt`
3. **Add libraries** → `app/build.gradle.kts`
4. **Build and test** → generate an APK from JStudio

---

## Upcoming Guides
- Adding a new Activity
- Installing Android libraries
- Using AI to generate Android code
- Building and exporting an APK from JStudio
