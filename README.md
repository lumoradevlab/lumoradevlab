# Lumora

**Android engineer, 10+ years** — Kotlin, Jetpack Compose, and multi-module architecture.
I build production Android apps, including ones that talk to real hardware over Bluetooth LE,
and I also work in Python on automation and data-collection tooling.

📍 United States · Open to remote Android roles (US)

---

### Core stack

**Kotlin** · Jetpack Compose · Coroutines & Flow · Hilt · Room · DataStore · WorkManager · Retrofit
**Architecture** · Clean Architecture · MVVM · MVI · Gradle multi-module · convention plugins
**Also** · Python · Bluetooth LE · Flutter

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

## Contact

Telegram — [@lumoradevlab](https://t.me/lumoradevlab)
