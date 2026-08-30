# Lumora

**Android engineer** — Kotlin, Jetpack Compose, and multi-module Clean Architecture.
I build production Android apps, including ones that talk to real hardware over Bluetooth LE,
and I also work in Python on automation and data-collection tooling.

📍 United States · Open to new opportunities

---

### Core stack

**Kotlin** · Jetpack Compose · Coroutines & Flow · Hilt · Room · DataStore · Paging 3 · WorkManager · Retrofit
**Architecture** · Clean Architecture · MVVM · MVI · Gradle multi-module
**Also** · Python · Bluetooth LE · Flutter

---

## Projects

### [OPlayerSensorRing](https://github.com/lumoradevlab/OPlayerSensorRing)
Android app that pairs with OPlayer smart rings over **Bluetooth LE** and syncs health telemetry —
heart rate and HRV, SpO2, blood pressure, sleep stages, steps, temperature.

The engineering problem is continuity rather than UI: a foreground service and WorkManager keep the
sync running in the background, restore it after reboot, and recover when the device drops connection.
Clean Architecture with Hilt, Room, and DataStore; vendor SDK bridged to native Android BLE.

`Kotlin` · `Compose` · `BLE` · `WorkManager` · `Hilt` · `Room`

### [ComposeCleanArch](https://github.com/lumoradevlab/ComposeCleanArch)
A Jetpack Compose Clean Architecture starter, structured as four Gradle modules —
`app`, `domain`, `data`, `presentation` — with dependencies constrained to point inward.

Hilt DI scoped per layer, Retrofit and Room behind repository interfaces, Paging 3 through a custom
`PagingSource`, typed result wrappers, and a `buildSrc` module holding version and dependency config
in one place.

`Kotlin` · `Compose` · `Multi-module` · `Hilt` · `Paging 3` · `Room`

### [xrpl-wallet-automation](https://github.com/lumoradevlab/xrpl-wallet-automation) · [xrpl-ai-automation](https://github.com/lumoradevlab/xrpl-ai-automation)
XRPL wallet and transaction automation: monitoring, balance checks, history export, testnet payments,
and AI-assisted risk review. Built around retry with backoff and a dead-letter queue so transient
API failures are retried and never silently dropped.

`Python` · `XRPL` · `LLM APIs`

### [Job-Crawler](https://github.com/lumoradevlab/Job-Crawler)
Collects remote-US Android and Kotlin job listings from seven job boards in a single pass, writing
TXT, CSV, and JSON. Python 3 standard library only, no dependencies. Deduplicates against prior runs
and narrows its own date window so repeat runs stay inexpensive.

`Python`

---

## GitHub Stats

<p align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=lumoradevlab&show_icons=true&hide_border=true&include_all_commits=true&count_private=true&theme=default" alt="GitHub stats" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=lumoradevlab&layout=compact&hide_border=true&langs_count=8&theme=default" alt="Top languages" />
</p>

<p align="center">
  <img src="https://streak-stats.demolab.com?user=lumoradevlab&hide_border=true&theme=default" alt="Contribution streak" />
</p>

<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=lumoradevlab&hide_border=true&area=true&theme=github-light" alt="Contribution activity graph" />
</p>

---

## Contact

Open an issue on any repository here, or reach me through my GitHub profile.
