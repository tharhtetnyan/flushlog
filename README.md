<div align="center">

# 🚽 FlushLog

A free Android toilet health tracker — log your pee, poo, and hydration daily to understand your body better and share clean health reports with your doctor.

![Free](https://img.shields.io/badge/Free-Download-green) ![Android](https://img.shields.io/badge/Platform-Android-blue) ![Offline](https://img.shields.io/badge/Fully-Offline-orange) ![No Account](https://img.shields.io/badge/No%20Account-Needed-lightgrey) ![Min SDK](https://img.shields.io/badge/Min%20SDK-26-informational)

### [⬇️ Download APK (v1.0)](https://github.com/tharhtetnyan31/flushlog/releases/download/v1.0/flushlog.apk)

</div>

---

## 📲 How to Install

1. Download the APK using the button above
2. On your Android phone, open the downloaded file
3. Allow "Install from unknown sources" if prompted, then tap Install

---

## 📸 Screenshots

![FlushLog Screenshots](flushlog_preview.jpg)

---

## ✨ Features

| Feature | Description |
|---|---|
| 🏠 Home Dashboard | Daily summary of pee count, poo count, and water intake with smart insights |
| 💧 Pee Logger | Log pee with color scale, urgency level, volume, and pain indicator |
| 💩 Poo Logger | Log poo with Bristol Stool Scale type, color, duration, and straining |
| 📊 Analytics | Bar charts for pee and poo trends over 7 days, 30 days, or 3 months |
| 🔥 Streak Tracker | Tracks consecutive days of logging to build a healthy habit |
| 🎨 Color Distribution | Visual breakdown of pee color and Bristol stool type history |
| 📄 Doctor Report | Generate and share a clean PDF health summary directly with your doctor |
| 📅 Log Book | Calendar view of all logs with filter by pee, poo, or all entries |
| 📚 Learn | Clinical education on hydration, UTI signs, Bristol chart, and when to see a doctor |
| 🌙 Dark Mode | Fully supported — toggle in Settings, persists across app restarts |
| 🔔 Smart Reminders | Gentle notifications if no log is recorded after a set number of hours |
| ⚙️ Settings | Reminder controls, dark mode toggle, water goal, and export options |

---

## 🛠️ Tech Stack

- **Language:** Kotlin
- **UI:** Jetpack Compose + Material 3
- **Architecture:** MVVM with Repository pattern
- **Database:** Room (local, offline-first)
- **Background Tasks:** WorkManager
- **Navigation:** Jetpack Navigation Compose
- **Preferences:** DataStore
- **PDF Export:** Android native `PdfDocument` (no third-party library)
- **Charts:** MPAndroidChart

---

## 🩺 Health Insights Logic

FlushLog automatically analyses your logs and shows smart tips:

| Condition | Insight Shown |
|---|---|
| Pee count > 10 today | Possible UTI or overactive bladder warning |
| Pee count < 4 by 6pm | Prompt to drink more water |
| Pee color dark amber or darker | Dehydration alert |
| Bristol type 1 or 2 | Low fiber / hydration suggestion |
| Bristol type 6 or 7 | Loose stool — monitor and stay hydrated |
| All normal | Positive daily health confirmation |

---

## 📋 Permissions Used

| Permission | Reason |
|---|---|
| POST_NOTIFICATIONS | Reminder alerts to log toilet visits |
| RECEIVE_BOOT_COMPLETED | Restore reminders after device reboot |
| WRITE_EXTERNAL_STORAGE | Save PDF report to Downloads (API 28 and below only) |

---

## 📄 Doctor Report

FlushLog can generate a clean, professional PDF health report containing:

- Patient summary — totals, averages, streak, most common pee color and Bristol type
- Full pee log table — date, time, color, urgency, volume, pain
- Full poo log table — date, time, Bristol type, color, duration, straining
- Health insights — hydration status, bowel regularity, frequency analysis

The share sheet opens immediately after generation so you can send it directly via Email, WhatsApp, or Telegram to your doctor.

---

## 🔒 Privacy

FlushLog is 100% offline. All your health data — pee logs, poo logs, and settings — is stored locally on your device only. Nothing is sent anywhere. No accounts, no servers, no tracking.

---

## 🏗️ Project Structure

```
flushlog/
├── app/src/main/java/com/example/
│   ├── data/
│   │   ├── Entities.kt          # PeeLog, PooLog Room entities
│   │   ├── Daos.kt              # PeeLogDao, PooLogDao
│   │   ├── PeePooDatabase.kt    # Room database
│   │   ├── PeePooRepository.kt  # Data access layer
│   │   └── SettingsRepository.kt # DataStore preferences
│   ├── viewmodel/
│   │   ├── PeePooViewModel.kt   # Home, log, history logic
│   │   ├── StatsViewModel.kt    # Analytics and chart data
│   │   └── ExportViewModel.kt   # PDF export logic
│   ├── ui/
│   │   ├── screens/             # Home, History, Stats, Learn, Settings
│   │   ├── theme/               # Color, Type, Shape, Theme
│   │   └── AppNavigation.kt     # Nav graph
│   ├── worker/
│   │   ├── ReminderWorker.kt    # WorkManager background task
│   │   └── ReminderScheduler.kt # Schedule/cancel reminders
│   └── MainActivity.kt
```

---

## 🎨 Color Palette

| Role | Light Mode | Dark Mode |
|---|---|---|
| Primary | `#1A6FA8` Ocean Blue | `#38BDF8` Sky Blue |
| Background | `#F7F9FC` Warm White | `#0A0F1E` Deep Navy |
| Pee Accent | `#F59E0B` Warm Amber | `#FBBF24` Golden Amber |
| Poo Accent | `#C0622A` Earthy Sienna | `#FB923C` Warm Orange |
| Healthy | `#10B981` Emerald | `#34D399` Bright Emerald |

---

<div align="center">

Built by **Thar Htet Nyan** &nbsp;·&nbsp; MIT License &nbsp;·&nbsp; © 2026

</div>
