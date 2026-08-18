# Meterly 📱

Meterly is a cross-platform mobile application built with **Nuxt 4**, **Nuxt UI**, and **Capacitor**. It runs natively on both **Android** and **iOS**.

---

## 🛠️ Prerequisites

Before you start, make sure you have the following installed on your computer:

- [Node.js](https://nodejs.org/) (v20 or higher)
- [pnpm](https://pnpm.io/)
- [Android Studio](https://developer.android.com/studio) with **Java 21** (required for Android builds)
- [ADB Tools](https://developer.android.com/tools/adb)

---

## 🚀 Step 1: Clone & Install the Project

### 1. Clone the repository

```bash
git clone https://github.com/your-username/meterly.git
```

### 2. Navigate into the project directory

```bash
cd meterly
```

### 3. Install dependencies

```bash
pnpm install
```

### 4. Run the web development server

```bash
pnpm dev
```

---

## 🤖 Step 2: Run & Install on Android

You can build and install the native app on a physical Android device using a single command.

### 1. Connect your Android phone

Connect your Android phone to your computer using a USB cable.

### 2. Enable USB Debugging

On your Android phone:

1. Go to **Settings → About Phone**.
2. Tap **Build Number** 7 times to enable Developer Options.
3. Go to **Settings → System → Developer Options**.
4. Turn on **USB Debugging**.

### 3. Run the automated installation command

```bash
pnpm android:install
```

### What this command does

The command automatically:

1. Builds the static web application:

   ```bash
   pnpm build
   ```

2. Copies the web files to the native Android project:

   ```bash
   pnpm cap sync android
   ```

3. Compiles the Android debug APK using Gradle:

   ```bash
   ./gradlew assembleDebug
   ```

4. Installs or updates the APK directly on your connected Android phone using `adb`.

Once the process finishes, open your phone. The **Meterly** native app should be available on your home screen.

---

## 🍎 Step 3: Run & Install on iPhone (iOS)

iOS builds require **Xcode on macOS**.

This repository uses **GitHub Actions** to automatically compile the iOS app package on a cloud Mac.

### How to get the iOS app on your iPhone

#### 1. Push your changes to the `main` branch

```bash
git add .
git commit -m "Update app"
git push origin main
```

#### 2. Open GitHub Actions

Open your repository on GitHub and:

1. Click the **Actions** tab.
2. Open the latest workflow run named **Build Native iOS App**.
3. Wait for the build to finish.
4. Scroll down to the **Artifacts** section.
5. Download **Meterly-iOS-App**.

#### 3. Install the app on your iPhone

Use a free sideloading tool such as **Sideloadly** or **AltStore**.

1. Download and open **Sideloadly** or **AltStore** on your PC.
2. Connect your iPhone to your computer using a USB cable.
3. Drag the downloaded **Meterly-iOS-App** bundle into the sideloading tool.
4. Enter your free Apple ID.
5. Click **Start**.
6. On your iPhone, go to:

   **Settings → General → VPN & Device Management**

7. Tap your Apple ID and select **Trust**.

The **Meterly** native app is now installed and ready to open from your iPhone home screen.
