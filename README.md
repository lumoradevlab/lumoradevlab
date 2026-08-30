# Hi, I'm Lumora 👋

**Android engineer** — Kotlin, Jetpack Compose, and clean multi-module architecture.
I build production apps that talk to real hardware, and I keep the layers honest: `domain` never
imports `data`, ViewModels never see a DTO, and every screen has a state class it can be tested against.

📍 United States · 🟢 Open to new opportunities

---

## What I work with

**Languages** · Kotlin · Python · Dart · Java

**Android** · Jetpack Compose · Material 3 · Coroutines & Flow · Hilt · Room · DataStore · Paging 3 · WorkManager · Navigation · Retrofit/OkHttp

**Architecture** · Clean Architecture · MVVM · MVI · Gradle multi-module (`buildSrc` version catalogs)

**Also** · BLE / Bluetooth LE · Foreground services · Flutter · REST API design

---

## Selected work

### 🔵 [OPlayerSensorRing](https://github.com/lumoradevlab/OPlayerSensorRing)
An Android app that pairs with **OPlayer smart rings over Bluetooth LE** and syncs health telemetry —
heart rate & HRV, SpO2, blood pressure, sleep stages, steps, temperature, stress.

The interesting part isn't the UI, it's staying connected: a foreground service plus WorkManager keep
the sync alive in the background, survive reboot via a `BootReceiver`, and reconnect when the ring drops off.
Clean Architecture + MVVM, Hilt, Room + DataStore, vendor SDK bridged to native Android BLE.
Ships with `ARCHITECTURE.md`, `SENSOR_SYNC_ARCHITECTURE.md`, and an honest `KNOWN_ISSUES.md`.

`Kotlin` `Compose` `BLE` `WorkManager` `Hilt` `Room`

---

### ⭐ [ComposeCleanArch](https://github.com/lumoradevlab/ComposeCleanArch)
A **Jetpack Compose Clean Architecture starter** — my most-starred repo, and the template I reach for
when a new app needs a spine on day one.

Four real Gradle modules (`app` · `domain` · `data` · `presentation`) with dependencies wired so they
can only point inward. Hilt DI per module, Room + Retrofit behind repository interfaces, Paging 3
through a custom `ArticlePagingSource`, DataStore preferences, a connectivity interceptor, typed
`DataState` wrappers, and a `buildSrc` module holding every version in one place.

`Kotlin` `Compose` `Multi-module` `Hilt` `Paging 3` `Room` `Retrofit`

---

### 🧭 [MVI-CleanArchitecture](https://github.com/lumoradevlab/MVI-CleanArchitecture)
The same problem solved with **MVI** instead of MVVM — `BaseMviAction`, reducers, and unidirectional
state flow, for when a screen's logic deserves a state machine rather than a pile of `MutableStateFlow`s.

`Kotlin` `MVI` `Clean Architecture`

---

### 🧱 [Modularization](https://github.com/lumoradevlab/Modularization)
A focused reference for **splitting an Android app into Gradle modules** — feature boundaries,
shared UI, and build config that scales past one `app/` folder.

`Kotlin` `Gradle` `Compose`

---

### 🐍 [Job-Crawler](https://github.com/lumoradevlab/Job-Crawler)
Sweeps **seven job boards** for remote-US Android/Kotlin roles in a single pass and writes TXT, CSV,
and JSON. Python 3 **stdlib only — zero dependencies**. Dedupes against everything it has seen before
and auto-shrinks its own date window so repeat runs stay cheap.

`Python`

---

### ⛓️ [xrpl-wallet-automation](https://github.com/lumoradevlab/xrpl-wallet-automation) · [xrpl-ai-automation](https://github.com/lumoradevlab/xrpl-ai-automation)
XRPL wallet automation — transaction monitoring, balance checks, history export, testnet payments,
and AI-assisted risk review. Built with **retry/backoff and a dead-letter queue**, because
"the API blipped" shouldn't mean a lost transaction.

`Python` `XRPL` `LLM APIs`

---

## Also on the shelf

[`FlutterBaseApp`](https://github.com/lumoradevlab/FlutterBaseApp) — Flutter starter ·
[`Pokedex`](https://github.com/lumoradevlab/Pokedex) — Compose + API sample ·
[`RecyclerWithDiffUtill`](https://github.com/lumoradevlab/RecyclerWithDiffUtill) — DiffUtil done right ·
[`MemoryLeak`](https://github.com/lumoradevlab/MemoryLeak) — leak patterns & fixes ·
[`revokePermission`](https://github.com/lumoradevlab/revokePermission) — runtime permission handling ·
[`ProfilesRestApi`](https://github.com/lumoradevlab/ProfilesRestApi) — Django REST API

---

## 📊 Stats

<p>
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=lumoradevlab&show_icons=true&hide_border=true&include_all_commits=true&count_private=true&theme=default" alt="GitHub stats" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=lumoradevlab&layout=compact&hide_border=true&langs_count=8&theme=default" alt="Top languages" />
</p>

---

## 📫 Get in touch

Open an issue on any repo here, or reach me through my GitHub profile.

*Happy to talk about Android architecture, BLE, or why your ViewModel shouldn't know what JSON is.*
