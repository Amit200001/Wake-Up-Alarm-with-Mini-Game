# WakeUpAlarm: Game Edition ⏰🎮

**WakeGuard** is an interactive, mini-game integrated alarm system designed to prevent oversleeping by requiring users to complete brain-stimulating challenges before an alarm can be dismissed. It features a live digital dashboard paired with a simulated Java/SQL backend engine to demonstrate database persistence, execution logging, and real-time event handling.

---

## 🚀 Features

* **Interactive Mini-Games for Dismissal:**

* 🧮 **Math Speed Challenge:** Requires solving arithmetic equations (e.g., addition) under pressure.


* 🧠 **Memory Tile Match:** A flip-card matching challenge to sharpen cognitive recall.


* ⚡ **Target Tap:** A fast-paced reaction and accuracy game.




* **Web Audio API Synthesizer:** Built-in audio tone generator supporting multiple sound profiles (Classic Digital Beep, Loud Siren Alert, Retro Synth Arpeggio) without external audio file dependencies.


* **Live Digital Dashboard:** Real-time clock display (12-hour format with AM/PM indicator, seconds, and date) and active alarm tracking.


* **Simulated Java/SQL Engine Tab:**

* View relational database structures (`alarms` and `dismissal_logs`).


* Live Spring Boot / JDBC execution console simulation tracking triggers, inserts, updates, and truncations.


* Options to seed sample logs or clear existing execution history.





---

## 🛠️ Tech Stack

* **Frontend:** HTML5, JavaScript (ES6+), Web Audio API


* **Styling & UI:** Tailwind CSS (via CDN), FontAwesome Icons, Google Fonts (Orbitron & Inter)


* **Backend Architectural Simulation:** Java (JDK 17 / Spring Boot Service layer simulation), JDBC Driver v8.0.32, Relational SQL schema (`alarms`, `dismissal_logs`)



---

## 📂 Database Schema Overview

The application simulates the following relational database tables:

### 1. Table: `alarms`

| Column Name | Data Type | Description |
| --- | --- | --- |
| `id` | BIGINT / INT | Primary key identifier for the alarm

 |
| `time` | VARCHAR | Scheduled time in 24-hour format (e.g., `07:00`)

 |
| `label` | VARCHAR | User-defined label or title

 |
| `game_type` | VARCHAR | Required mini-game (`math`, `memory`, `reaction`)

 |
| `is_active` | BOOLEAN / TINYINT | Active toggle state (`1` for enabled, `0` for disabled)

 |

### 2. Table: `dismissal_logs`

| Column Name | Data Type | Description |
| --- | --- | --- |
| `log_id` | VARCHAR | Unique log reference ID (e.g., `LOG-901`)

 |
| `timestamp` | DATETIME | Time of alarm completion

 |
| `game` | VARCHAR | Mini-game completed to turn off the alarm

 |
| `duration` | VARCHAR | Time taken to successfully dismiss the alarm

 |
| `status` | VARCHAR | Completion status (e.g., `SUCCESS`)

 |

---

## 📖 How to Run

1. Clone or download this repository to your local machine.
2. Open `index.html` directly in any modern web browser (Google Chrome, Firefox, Safari, or Edge).


3. Click anywhere on the webpage to enable Web Audio API permissions for audio playback.



---

## 🎮 How to Use

1. **Setting an Alarm:** Navigate to the **Dashboard** tab, select a time, enter a label, choose a mini-game challenge and sound tone, then click **Save Alarm**.


2. **Testing Alarms:** Click the **Test Alarm** button on any listed alarm card to trigger the overlay modal and sound manually.


3. **Dismissing Alarms:** When an alarm triggers, solve the required mini-game challenge (e.g., solve 3 math equations, match 4 tile pairs, or tap the targets) to stop the sound and lock in the log.


4. **Viewing Database Logs:** Switch to the **Java/SQL Engine** tab to inspect active table rows, inspect simulated Java service terminal logs, or seed test data.
