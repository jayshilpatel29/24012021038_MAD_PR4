# ⏰ Android Alarm Application — MAD Practical 4

<div align="center">

### 📱 Mobile Application Development

**An Android Alarm Application built using Kotlin, AlarmManager, BroadcastReceiver & Service**

<br>

![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logo=kotlin&logoColor=white)
![Android](https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)
![Android Studio](https://img.shields.io/badge/Android%20Studio-3DDC84?style=for-the-badge&logo=androidstudio&logoColor=white)
![MAD](https://img.shields.io/badge/MAD-Practical%204-FF6B6B?style=for-the-badge)

</div>

---

## 🌙 About the Project

**Android Alarm Application** is **MAD Practical 4** developed as part of the **Mobile Application Development** course.

The application allows users to select a specific time and schedule an alarm. When the scheduled time is reached, an Android **BroadcastReceiver** receives the alarm event and starts an **AlarmService**, which plays the alarm sound.

The practical demonstrates how Android applications can perform scheduled background operations using system services and broadcast events.

---

## 🎯 Aim

> **Create an Android Alarm Application by using Service & BroadcastReceiver.**

---

## ✨ Features

- ⏰ Set an alarm for a specific time
- 🕐 Display current time using `TextClock`
- 📅 Select alarm time using `TimePickerDialog`
- 🔔 Schedule alarms using `AlarmManager`
- 📡 Receive alarm events using `BroadcastReceiver`
- ⚙️ Start alarm playback using `Service`
- 🎵 Play alarm sound using `MediaPlayer`
- 🛑 Stop the alarm service when required
- 📱 Material Design based UI
- 🔐 Exact alarm permission support

---

## 🧠 Concepts Covered

This practical focuses on the following Android concepts:

| Concept | Purpose |
|---|---|
| 📡 `BroadcastReceiver` | Receives the alarm broadcast |
| ⚙️ `Service` | Runs the alarm operation |
| ⏰ `AlarmManager` | Schedules the alarm |
| 🕐 `TextClock` | Displays current time |
| ⏱️ `TimePickerDialog` | Allows the user to select alarm time |
| 📅 `Calendar` | Handles date and time |
| 📆 `SimpleDateFormat` | Formats date/time |
| 📦 `PendingIntent` | Defines the action triggered by the alarm |
| 🎵 `MediaPlayer` | Plays the alarm sound |
| 🔧 `getSystemService()` | Accesses Android system services |
| 📢 `sendBroadcast()` | Sends broadcast events |
| ▶️ `startService()` | Starts the alarm service |
| ⏹️ `stopService()` | Stops the alarm service |
| 📥 `Intent.getStringExtra()` | Retrieves intent data |
| 📤 `Intent.putStringExtra()` | Passes data through an intent |
| 🎨 `MaterialCardView` | Creates Material-style UI cards |

---

## 🔄 How the Application Works

```text
                    ┌─────────────────────┐
                    │   User Opens App    │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │ Select Alarm Time    │
                    │ TimePickerDialog     │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │     Calendar        │
                    │ Calculate Time      │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    AlarmManager     │
                    │ Schedule Alarm      │
                    └──────────┬──────────┘
                               │
                         ⏳ Waiting...
                               │
                               ▼
                    ┌─────────────────────┐
                    │ BroadcastReceiver   │
                    │ Receives Alarm      │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    AlarmService     │
                    │     Starts          │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    MediaPlayer      │
                    │   Plays Alarm.mp3   │
                    └─────────────────────┘
```

---

## 🏗️ Application Architecture

```text
MainActivity
     │
     │ Set Alarm
     ▼
AlarmManager
     │
     │ PendingIntent
     ▼
AlarmBroadcastReceiver
     │
     │ Intent
     ▼
AlarmService
     │
     ▼
MediaPlayer
     │
     ▼
🔔 Alarm Sound
```

---

## 🛠️ Technology Stack

### Languages & Framework

- **Kotlin**
- **Android SDK**
- **Android Framework**

### Development Tools

- **Android Studio**
- **Gradle**
- **Android Emulator / Physical Android Device**

### Android Components

- `Activity`
- `BroadcastReceiver`
- `Service`
- `AlarmManager`
- `PendingIntent`
- `MediaPlayer`
- `Calendar`
- `TimePickerDialog`
- `TextClock`
- `MaterialCardView`

---

## 🔐 Required Permission

The application requires permission to schedule exact alarms.

Add the following permission to `AndroidManifest.xml`:

```xml
<uses-permission android:name="android.permission.SCHEDULE_EXACT_ALARM" />
```

This permission allows the application to schedule alarms at an exact time where supported by the Android version/device.

---

## 📂 Project Structure

```text
24012021038_MAD_PR4/
│
├── 📁 app/
│   │
│   └── 📁 src/
│       │
│       └── 📁 main/
│           │
│           ├── 📁 java/
│           │   └── 📁 com.jayshil...
│           │       ├── MainActivity.kt
│           │       ├── AlarmBroadcastReceiver.kt
│           │       └── AlarmService.kt
│           │
│           ├── 📁 res/
│           │   ├── 📁 drawable/
│           │   ├── 📁 layout/
│           │   ├── 📁 mipmap/
│           │   └── 📁 values/
│           │
│           └── AndroidManifest.xml
│
├── 📁 gradle/
├── 📄 build.gradle.kts
├── 📄 settings.gradle.kts
├── 📄 gradle.properties
├── 📄 gradlew
├── 📄 gradlew.bat
└── 📄 README.md
```

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/jayshilpatel29/24012021038_MAD_PR4.git
```

### 2. Open in Android Studio

Open the cloned project in **Android Studio**.

```text
Android Studio
      ↓
File
      ↓
Open
      ↓
24012021038_MAD_PR4
```

### 3. Sync Gradle

Wait for Android Studio to complete the Gradle synchronization.

### 4. Run the Application

Connect an Android device or start an emulator.

Then click:

```text
▶ Run
```

### 5. Set an Alarm

1. Open the application.
2. Select the desired alarm time.
3. Confirm the selected time.
4. The application schedules the alarm.
5. Wait until the scheduled time.
6. `AlarmBroadcastReceiver` receives the broadcast.
7. `AlarmService` starts.
8. `MediaPlayer` plays the alarm sound. 🔔

---

## 🎵 Alarm Sound

The application uses an MP3 audio file for the alarm sound.

```text
res/
└── raw/
    └── alarm.mp3
```

The sound is played using Android's `MediaPlayer`.

---



---

## 🎓 Learning Outcomes

After completing this practical, the following concepts can be understood:

- Understanding Android `BroadcastReceiver`
- Understanding Android `Service`
- Scheduling tasks using `AlarmManager`
- Working with `PendingIntent`
- Handling date and time using `Calendar`
- Creating a time selection interface using `TimePickerDialog`
- Playing audio using `MediaPlayer`
- Passing data through `Intent`
- Starting and stopping Android services
- Working with Android permissions
- Creating Material Design interfaces

---

## 🧪 Practical Workflow

```text
User
 │
 ▼
MainActivity
 │
 │ Select Time
 ▼
TimePickerDialog
 │
 ▼
Calendar
 │
 ▼
AlarmManager
 │
 ▼
PendingIntent
 │
 │ Alarm Time Reached
 ▼
BroadcastReceiver
 │
 ▼
AlarmService
 │
 ▼
MediaPlayer
 │
 ▼
🔊 Alarm.mp3
```

---

## 📚 Academic Information

| 📌 Information | Details |
|---|---|
| Subject | Mobile Application Development |
| Practical | Practical 4 |
| Aim | Create an Android Alarm Application using Service & BroadcastReceiver |
| Platform | Android |
| Language | Kotlin |
| IDE | Android Studio |
| Student | Jayshil Patel |
| Enrollment No. | 24012021038 |

---

## 🌐 Course Resources

This practical is based on the **MAD 2025** course material provided by Ganpat University.

- 📘 [MAD 2025 Course](https://sites.google.com/ganpatuniversity.ac.in/mad/home)
- 📱 [Views Android](https://sites.google.com/ganpatuniversity.ac.in/mad/views-android)
- 🧪 [Practical List](https://sites.google.com/ganpatuniversity.ac.in/mad/practical-list)
- 📝 [Kotlin](https://sites.google.com/ganpatuniversity.ac.in/mad/kotlin)

---

## 👨‍💻 Developer

<div align="center">

### Jayshil Patel

**IT Engineering Student**

🎓 Mobile Application Development  
💻 Android & Kotlin Developer

**Enrollment No. 24012021038**

<br>

[![GitHub](https://img.shields.io/badge/GitHub-Jayshil%20Patel-181717?style=for-the-badge&logo=github)](https://github.com/jayshilpatel29)

</div>

---

## ⭐ Support

If you found this project useful for learning Android development, consider giving the repository a ⭐.

<div align="center">

### ⏰ Schedule. Wait. Get Notified. 🔔

**Built with ❤️ using Kotlin & Android Studio**

**© 2026 Jayshil Patel**

</div>
