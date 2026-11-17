<div align="right">
  <strong>English</strong> | <a href="README_TR.md">Türkçe</a>
</div>

# Flawless | Personal Progress Tracker

**Flawless** is a personal Android app created to make my goals visible and track my daily progress between **November 23 and January 10**. Rather than keeping tasks, routines, and reflections in different places, I wanted a single space where I could see what I planned, what I completed, and which habits I was building over this period.

This is a **personal learning and productivity project**, not a commercial product. Its main purpose is to support consistency through a defined time window, rather than promise instant results.

## Why I built it

I wanted to turn a personal set of goals into a practical, trackable routine. The November 23–January 10 period gave the project a clear beginning and end, with smaller stages to review progress along the way. Developing Flawless also gave me an opportunity to explore Android application structure, state management, and local data persistence.

## Features

- **Dashboard:** a summary of daily progress and the goal period.
- **Tasks:** create, edit, prioritize, complete, and delete tasks.
- **Habits:** track recurring activities and completed days.
- **Daily tracking:** record water, workouts, English practice, and meal entries.
- **Journal:** write personal reflections and record daily mood.
- **Profile and preferences:** manage app settings and selected personal tracking values.
- **Local persistence:** core tracking data is stored on the device through Android DataStore.

## Tech stack

- Kotlin
- Jetpack Compose / Material 3
- Android Jetpack ViewModel
- DataStore Preferences
- WorkManager
- Gradle (Kotlin DSL)
- Firebase-related Gradle configuration (requires your own configuration file)

## Setup

1. Clone this repository:

   ```bash
   git clone https://github.com/burakunal516/Flawless-App.git
   ```

2. Open the cloned project in **Android Studio**, then sync Gradle.
3. Configure Firebase for your own Android project as described below.
4. Run the app on a compatible Android emulator or device.

### Firebase configuration required

The original `app/google-services.json` file has been **intentionally excluded** from this public repository. This is a privacy choice: it does not mean the project files are missing by accident.

To build the project with the current Google Services plugin configuration:

1. Open [Firebase Console](https://console.firebase.google.com/) and create or select **your own** Firebase project.
2. Register an Android app using the package/application ID `com.burak` (or update the application's ID and register that value).
3. Download the generated `google-services.json` configuration file.
4. Place it locally at `app/google-services.json`.
5. Sync Gradle and build the project.

**Do not commit your local Firebase configuration, service-account credentials, secret keys, or tokens.** The repository's `.gitignore` excludes `google-services.json`. See [`FIREBASE_KURULUM.md`](FIREBASE_KURULUM.md) for the Turkish setup notes. An initial build without the required file may fail because the Google Services Gradle plugin is enabled.

> Note: The source includes a Firebase AI dependency and Google Services plugin configuration. Core tracking records are stored locally using DataStore; this README does not claim that personal entries are synchronized to Firebase.

## Development note

AI-assisted tools were used during development. The application was created around my own tracking needs and the November 23–January 10 goal period.

## Project status

Personal project / ongoing improvements. Functionality and build requirements may change as the app evolves.
