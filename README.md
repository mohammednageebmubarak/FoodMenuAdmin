# FoodMenuAdmin

An Android application for managing a restaurant food menu and customer orders. The app is written in Java and uses Firebase for authentication, Realtime Database, and image storage.

## Features

- Admin sign-in
- Create and manage food categories and menu items
- Add food details such as name, description, price, and discount
- Upload food images to Firebase Storage
- View incoming orders and update their status
- Customer sign-up and sign-in

## Technology

- Java and Android SDK
- Android Support Libraries
- Firebase Authentication
- Firebase Realtime Database
- Firebase Storage
- Gradle 4.1 and Android Gradle Plugin 3.0.1

## Requirements

This project uses an older Android build toolchain. To build it as currently configured, use Android Studio with:

- JDK 8
- Android SDK Platform 26
- Android Build Tools 26.0.2

The app's minimum SDK is 21.

## Firebase setup

1. Create or select a Firebase project.
2. Register an Android app using the application ID `com.example.foodmenuadmin`.
3. Add the Firebase configuration file as `app/google-services.json`.
4. Enable the Firebase services used by the app: Authentication, Realtime Database, and Storage.
5. Configure Firebase Database and Storage security rules for your app before using it with real users.

The project currently uses Firebase Authentication for the admin sign-in flow. Customer account data is read from and written to the Realtime Database. Review and secure the Firebase rules carefully; client-side checks alone do not enforce admin access.

## Build

Open the project in Android Studio and allow Gradle to sync. You can also build a debug APK from the project root:

```bash
./gradlew assembleDebug
```

On Windows:

```bat
gradlew.bat assembleDebug
```

The generated APK is usually located at `app/build/outputs/apk/debug/app-debug.apk`.

## Project structure

- `app/src/main/java` — Java application code
- `app/src/main/res` — Android layouts and resources
- `app/src/main/assets` — bundled assets and the SQLite database
- `app/build.gradle` — app SDK settings and dependencies

## Notes

This repository uses the legacy Android Support Libraries and older Gradle/Firebase dependencies. Updating the build system or migrating to AndroidX may require code and dependency changes.
