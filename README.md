# Spotify Playlist Switcher Bot

A production-ready Android automation that smart-switches between Spotify playlists based on context, schedule, or triggers. It removes the friction of manual switching during workouts, study sessions, or focus blocks, and ensures the right playlist is always playing at the right time. The outcome: fewer taps, more flow, and consistent listening routines — powered by robust device-level automation.

<p align="center">
  <a href="https://Appilot.app" target="_blank">
    <img src="media/appilot-baner.png" alt="Appilot Banner" width="100%">
  </a>
</p>
<p align="center">
  <a href="https://t.me/devpilot1" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%20Appilot%2C%20I'm%20interested%20in%20automation." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:support@appilot.app" target="_blank">
    <img src="https://img.shields.io/badge/Email-support@appilot.app-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://appilot.app" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>

<p align="center"> 
   Created by Appilot, built to showcase our approach to Automation!<br>
   <strong>If you are looking for custom Spotify Playlist Switcher Bot, you've just found your team — Let’s Chat.👆👆</strong>
</p>

## Introduction
This bot automates playlist switching on Spotify across Android real devices and emulators. It observes your configured rules (time-of-day, Wi-Fi/BT connect, device motion, calendar status, focus mode) and seamlessly switches playlists without needing desktop integrations.  
It solves the repetitive workflow of opening Spotify, navigating to a playlist, and tapping play — dozens of times a day.  
Benefit: consistent routine, saved time, and zero-interruption context shifts for creators, students, and teams.

### Automating Context-Aware Playlist Switching
- Time & Context Rules: switch playlists by schedule, geofence, or device triggers (e.g., headset connect).
- Stealthy & Human-like: taps, delays, and swipes mimic normal user behavior to reduce detection and UI flakiness.
- Works Across Accounts & Devices: ideal for personal use or labs managing many devices at once.
- Low-Code Orchestration: configure tasks via YAML/JSON in the Appilot dashboard; no code changes required.

## Core Features
- **Real Devices and Emulators:** Run on physical Android phones/tablets and emulator stacks (Bluestacks, Nox) with identical flows. Ensures parity across test and prod setups for Spotify app interactions.
- **No-ADB Wireless Automation:** Control devices over Wi-Fi with secure pairing; eliminate USB hubs and messy cables in device farms while preserving reliable command delivery.
- **Mimicking Human Behavior:** Randomized tap coordinates, variable delays, scrolling velocity curves, and occasional micro-pauses to simulate natural usage and reduce UI flakiness.
- **Multiple Accounts Support:** Maintain distinct sessions, cookies, and app profiles; rotate accounts safely with per-account rules, cooldowns, and optional proxy routing.
- **Multi-Device Integration:** Orchestrate 10–300+ devices concurrently with centralized schedules, per-device overrides, and aggregated logs/metrics.
- **Exponential Growth for Your Account:** Enforce routine plays for your curated playlists, improving consistency of engagement signals over time (ethical usage recommended).
- **Premium Support:** Priority debugging, device-farm onboarding, and custom rule-building by Appilot engineers.
- **Rule-Based Switching Engine:** Cron-like schedules, event triggers (Bluetooth/Headset connect, charger plugged), and calendar “focus” windows drive playlist switches.
- **Geo/Network Aware:** Switch on specific Wi-Fi SSIDs (e.g., “Gym”), cell conditions, or geofences.
- **Failsafe Recovery:** On crash or Spotify update, the bot re-detects UI, re-authenticates if needed, and resumes tasks.
- **Session Persistence:** Durable storage of app state, last played playlist, and rule versions for deterministic behavior.
- **Observability:** Structured logs, device screenshots-on-error, and run reports exported as CSV/JSON.

**Additional Feature Set**

| Feature | Description |
|---|---|
| **Adaptive UI Selectors** | Hybrid selectors (content-desc, text, bounds heuristics) auto-adapt when Spotify UI changes across versions and locales. |
| **Profile-Aware Routing** | Map rules to specific user profiles; isolate cookies, cache, and Spotify app data per profile for safety. |
| **Proxy & Network Control** | Optional per-device proxy rotation (residential/mobile) and Wi-Fi SSID pinning for location-consistent sessions. |
| **Rate & Cooldown Manager** | Enforce per-account rate limits, cooldowns between switches, and daily session caps to avoid suspicious patterns. |
| **Scheduler & Queues** | Priority queues with backoff and retries; run immediate tasks, windowed schedules, or long-running routines. |
| **Alerting & Webhooks** | Push real-time alerts to Slack/Telegram/Webhooks on failures, recoveries, and rule executions. |

</p>
<p align="center">
  <a href="https://bitbash.dev" target="_blank">
    <img src="spotify-playlist-switcher-bot-architecture.png" alt="spotify-playlist-switcher-bot-architecture" width="95%">
  </a>
</p>

## How It Works
1. **Input or Trigger** — The automation is triggered through the Appilot dashboard, where the user selects desired conditions (time schedule, Bluetooth connect, focus mode, geofence) and target Spotify playlists.  
2. **Core Logic** — Appilot controls the Android device or emulator via UI Automator/Appium/optional ADB to open Spotify, navigate to the target playlist, and tap play. It uses resilient selectors and human-like delays.  
3. **Output or Action** — The bot switches playback to the designated playlist and logs the event (device, account, rule). Optional follow-up actions include volume normalization or shuffle toggles.  
4. **Other functionalities** — Retry logic, circuit breakers, screenshot-on-error, structured logging, and parallel processing are configured in the Appilot dashboard to ensure smooth execution and fast troubleshooting.

## Tech Stack
- **Language:** Kotlin, Java, Python, JavaScript  
- **Frameworks:** Appium, UI Automator, Espresso, Robot Framework, Cucumber  
- **Tools:** Appilot, Android Debug Bridge (ADB), Appium Inspector, Bluestacks, Nox Player, Scrcpy, Firebase Test Lab, Accessibility  
- **Infrastructure:** Dockerized device farms, Cloud-based emulators, Proxy networks, Parallel Device Execution, Task Queues, Real device farm

## Directory Structure
```
spotify-playlist-switcher-bot/
│
├── src/
│ ├── main.py
│ ├── rules/
│ │ ├── scheduler.py
│ │ ├── triggers.py
│ │ └── evaluators.py
│ ├── drivers/
│ │ ├── ui_automator.py
│ │ ├── appium_client.py
│ │ └── adb_bridge.py
│ ├── spotify/
│ │ ├── selectors.py
│ │ ├── navigator.py
│ │ └── actions.py
│ ├── utils/
│ │ ├── logger.py
│ │ ├── device_pool.py
│ │ ├── humanizer.py
│ │ └── storage.py
│ └── monitoring/
│ ├── watchdog.py
│ └── webhooks.py
│
├── config/
│ ├── rules.yaml
│ ├── devices.yaml
│ ├── proxies.yaml
│ └── credentials.env
│
├── logs/
│ ├── runtime.log
│ └── device/
│ └── device-0001.log
│
├── output/
│ ├── reports/
│ │ └── run-YYYYMMDD.csv
│ └── screenshots/
│ └── error-<timestamp>.png
│
├── tests/
│ ├── test_rules.py
│ ├── test_spotify_flow.py
│ └── test_selectors.py
│
├── docker/
│ └── docker-compose.yml
│
├── requirements.txt
├── README.md
└── LICENSE
```

## Use Cases
- **Creators** use it to auto-switch from “Focus/Deep Work” to “Break/Chill” playlists at scheduled intervals, so they maintain consistent work rhythms.  
- **Gym Owners** use it to start “Workout” playlists when the gym soundbar connects, so music is always on-brand without staff intervention.  
- **Teams** use it to align playlists with meeting blocks from shared calendars, so background music supports team energy and focus.  
- **Students** use it to trigger “Study” playlists on campus Wi-Fi and “Commute” playlists when mobile data is active, saving daily taps.

## FAQs
**How do I configure this automation for multiple accounts?**  
Add each account profile in `devices.yaml` and map it to rule sets in `rules.yaml`. The bot preserves independent sessions and rotates safely with cooldowns and daily caps.

**Does it support proxy rotation or anti-detection?**  
Yes. Configure per-device or per-account proxies in `proxies.yaml`. Humanizer controls add jitter to taps, scrolls, and timings to reduce repetitive patterns.

**Can I schedule it to run periodically?**  
Absolutely. Use cron-like windows in `rules.yaml` (e.g., morning/evening blocks). The scheduler enqueues jobs and the workers execute them across devices.

**What happens when Spotify updates its UI?**  
Adaptive selectors blend content-desc, text, and bounds heuristics. If a major change occurs, selectors auto-fallback and screenshots/logs help patch quickly.

**Can it run fully wireless?**  
Yes. Use No-ADB wireless control and scrcpy/Appium over Wi-Fi to avoid USB hubs in large device racks.

## Performance & Reliability Benchmarks
- **Execution Speed:** Handles 100+ UI actions per minute per device with async queuing and minimal idle time.  
- **Success Rate:** 95% end-to-end successful playlist switches across heterogeneous devices and app versions under typical conditions.  
- **Scalability:** Proven orchestration for 50–300 devices; architecture patterns extend to 1,000 with horizontal queues and sharded device pools.  
- **Resource Efficiency:** Low CPU on controllers (<20% avg) and modest memory pressure via lightweight workers; emulator density optimized per host.  
- **Error Handling:** Automatic retries with exponential backoff, circuit breakers, screenshot-on-error, structured logs, and proactive alerts via webhooks.
##
<p align="center">
<a href="https://cal.com/app-pilot-m8i8oo/30min" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
</p>




