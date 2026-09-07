<img src="https://capsule-render.vercel.app/api?type=waving&color=0:24292F,100:7F52FF&height=170&section=header&text=Lumora&fontColor=ffffff&fontSize=52&fontAlignY=34&desc=Android%20Engineer%20%C2%B7%20Kotlin%20%C2%B7%20Jetpack%20Compose&descAlignY=56&descSize=16" alt="Lumora - Android engineer, Kotlin, Jetpack Compose" />

**Android engineer, 10+ years** — Kotlin, Jetpack Compose, and multi-module architecture.
I build production Android apps, including ones that talk to real hardware over Bluetooth LE,
and I also work in Python on automation and data-collection tooling.

📍 United States · Open to remote Android roles (US)

---

### Core stack

![Kotlin](https://img.shields.io/badge/Kotlin-7F52FF?style=for-the-badge&logoColor=white&logo=kotlin) ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logoColor=white&logo=python) ![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logoColor=white&logo=dart) ![Android](https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logoColor=white&logo=android)

![Jetpack Compose](https://img.shields.io/badge/Jetpack%20Compose-4285F4?style=for-the-badge&logoColor=white&logo=jetpackcompose) ![Coroutines & Flow](https://img.shields.io/badge/Coroutines%20%26%20Flow-7F52FF?style=for-the-badge&logoColor=white) ![Hilt](https://img.shields.io/badge/Hilt-2C4AA8?style=for-the-badge&logoColor=white) ![Room](https://img.shields.io/badge/Room-1B6AC6?style=for-the-badge&logoColor=white) ![DataStore](https://img.shields.io/badge/DataStore-1B6AC6?style=for-the-badge&logoColor=white) ![WorkManager](https://img.shields.io/badge/WorkManager-1B6AC6?style=for-the-badge&logoColor=white) ![Retrofit](https://img.shields.io/badge/Retrofit-48B983?style=for-the-badge&logoColor=white) ![Gradle](https://img.shields.io/badge/Gradle-02303A?style=for-the-badge&logoColor=white&logo=gradle) ![Bluetooth LE](https://img.shields.io/badge/Bluetooth%20LE-0082FC?style=for-the-badge&logoColor=white&logo=bluetooth) ![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logoColor=white&logo=flutter)

**Architecture** · Clean Architecture · MVVM · MVI · Gradle multi-module · convention plugins

---

## Projects

### [ComposeCleanArch](https://github.com/lumoradevlab/ComposeCleanArch)
A Jetpack Compose base app you can clone and start a real project from, with one unusual idea:
**screens have no ViewModels.**

Server state goes through a hand-rolled query cache — `useQuery` / `useMutation`, React Query style,
with TTL, deduplication, invalidation, retry, and interval refetch — so a read-only screen is a hook
call and a `QueryContent` block. No `uiState` class, no loading boolean, no `LaunchedEffect { load() }`.
Retrofit sits behind a `Resource` call adapter, which removes per-call `safeApiCall` wrappers, and
every error reaches the UI as one `AppError` type.

Ten Gradle modules with dependencies pointing downward only (`app → core:ui/query/network →
core:common → core:model`), `build-logic` convention plugins over a version catalog, dev/staging/prod
flavors, and detekt, ktlint, Android Lint and dependency-analysis wired as gates. It fetches real
headlines from NewsAPI, so the architecture is demonstrated end to end rather than described.

`Kotlin` · `Compose` · `Multi-module` · `Hilt` · `Room` · `DataStore`

### [Job-Crawler](https://github.com/lumoradevlab/Job-Crawler)
Collects remote-US Android and Kotlin job listings from seven job boards in a single pass, writing
TXT, CSV, and JSON. Python 3 standard library only, no dependencies. Deduplicates against prior runs
and narrows its own date window so repeat runs stay inexpensive.

`Python`

### [xrpl-wallet-automation](https://github.com/lumoradevlab/xrpl-wallet-automation) · [xrpl-ai-automation](https://github.com/lumoradevlab/xrpl-ai-automation)
XRPL wallet and transaction automation: monitoring, balance checks, history export, testnet payments,
and AI-assisted risk review. Built around retry with backoff and a dead-letter queue so transient
API failures are retried and never silently dropped.

`Python` · `XRPL` · `LLM APIs`

### [FlutterBaseApp](https://github.com/lumoradevlab/FlutterBaseApp)
A Flutter starter with the same intent as ComposeCleanArch on the Android side: a Melos workspace
split into concern-shaped packages — design system, Dio API client with retry and typed exceptions,
and a repository package — with Riverpod for state and DI, GoRouter, dev/staging/prod flavors via
`--dart-define-from-file`, and zone-guarded startup reporting to Sentry.

`Flutter` · `Dart` · `Riverpod` · `Melos`

### [OPlayerSensorRing](https://github.com/lumoradevlab/OPlayerSensorRing)
Android app that pairs with OPlayer smart rings over **Bluetooth LE** and syncs health telemetry —
heart rate and HRV, SpO2, blood pressure, sleep stages, steps, temperature.

The engineering problem is continuity rather than UI: a foreground service and WorkManager keep the
sync running in the background, restore it after reboot, and recover when the device drops
connection. Clean Architecture with Hilt, Room, and DataStore; the vendor SDK is bridged to native
Android BLE so scanning finds both OPlayer rings and generic devices.

`Kotlin` · `Compose` · `BLE` · `WorkManager` · `Hilt` · `Room`

---

## Activity

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://streak-stats.demolab.com/?user=lumoradevlab&hide_border=true&date_format=M%20j%5B%2C%20Y%5D&theme=dark">
  <img src="https://streak-stats.demolab.com/?user=lumoradevlab&hide_border=true&date_format=M%20j%5B%2C%20Y%5D" alt="GitHub contribution streak" width="495">
</picture>

---

## Contact

Telegram — [@lumoradevlab](https://t.me/lumoradevlab)
