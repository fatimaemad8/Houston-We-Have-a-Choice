# Houston, We Have a Choice 🚀
### Junior Astronaut Mission Trainer — 2026 NASA Space Apps Challenge

**A free, browser-based website where kids ages 7–12 learn how NASA keeps astronauts alive, then press Play to run the mission themselves in a 3D simulation game.**

Built for the **2026 NASA Space Apps Challenge** (Challenge: *Build a Junior Astronaut Mission Trainer*).

**Author:** Fatima Emad — Data Scientist and STEM Teacher (3 years teaching Math, Programming, and Data Science to ages 4–18).

> *"If you want to build a ship, don't drum up people to collect wood... teach them to yearn for the vast and endless sea."* — Antoine de Saint-Exupéry

---

## 🧠 The Problem
Kids hear that space is dangerous, but they never get to *decide* anything. A video says "space is dangerous." A game lets a child choose, and understand *why*. The challenge asks: how do you make a 9-year-old feel a real space trade-off by deciding, not by watching?

## 💡 The Solution
One website. No downloads, no accounts. Kids learn the idea in a world they understand, then press **Play** and the game opens right on the page. **Every choice has a cost, so there is no "safe" option.**

---

## 🌟 What's on the website?

| Section | What it does |
|---|---|
| **Home** | Mission briefing, progress bar, rank, and 10 real NASA/NOAA events the project is built on. |
| **Play** | Opens **Deep Space Run** (a 3D game) right inside the page. |
| **Lessons** | 13 mission lessons built on real events, for Cadets (7-8), Navigators (9-10), and Commanders (11-12), with a text-to-speech voice guide. |
| **Certificates** | Finish a lesson to unlock its certificate; finish all 13 for the Mission Commander award. |
| **How to play** | Plain-language rules for the game. |
| **Sources** | Where every fact comes from, with the data tags explained. |
| **For teachers** | A complete 45-minute lesson plan, teacher guide, and accuracy notes. |

*Extra touches: a sound on/off button, and progress saved automatically in the browser.*

---

## 🎮 The Game: Deep Space Run
Players launch, steer through rocks, collect supplies, and survive solar storms. Landing at the Station, Moon, or Mars lets them grow space lettuce in a 3D Veggie garden!

**Game modes and features:**
*   **Mars Outpost:** Run a base for 8 sols (Martian days), splitting a few power units each sol between air, food, shield, comms, and science.
*   **A Day in the Outpost:** Live one astronaut day in 5 choices (Morning Check, Morning Work, Midday, Afternoon, Evening). Every option shows its **Reward, Risk, and Penalty**.
*   **Cabin Training (360°):** Run a 3D cargo bay on 5 power units while a solar storm is coming. Learn real Apollo 13 history while doing it.
*   **My 3 Resources:** Players choose which 3 resources to manage before they start (Air, Food, Shield, Comms, Science). The rest run on autopilot.
*   **Real Mission Files:** 7 historical missions (Artemis II, Apollo 13, Opportunity, Lunar Night, MOXIE, Veggie Harvest, Mars Radio Delay) as interactive puzzles.
*   **Live Storm:** Face the strongest NASA DONKI flare of the last 30 days.
*   **3D Veggie Garden:** Land on the Moon or Mars to grow, harvest, and taste space lettuce, replicating the 2015 ISS experiment.
*   **Progression:** Collectible NASA cards and ranks from Space Cadet to Flight Director.

### ⚖️ The Trade-off (Mars Outpost)
| Spend power on | What it does |
|---|---|
| Life support | 2 units hold the air steady |
| Radiation shield | Each unit blocks 25% of a storm (max 75%) |
| Greenhouse | Each unit makes 3 food for the next sol |
| Comms to Earth | 1 unit shows tomorrow's forecast |
| Science | 10 research points per unit (the score) |

**Radiation added by one X9.0-class storm** (as a share of the mission limit):
*   0 Shield units: **29.0%**
*   1 Shield unit: **22.0%**
*   2 Shield units: **14.5%**
*   3 Shield units: **7.2%**

*Three shield units cut the dose by ~75%, but those units can no longer grow food or do science. The formula is `(4 + storm size) × (1 − shield)`.*

> **Honesty note:** Storm sizes are the game's own design values, not NASA dose measurements. The game says so on screen.

---

## 🍎 In the Classroom
A 45-minute 5E lesson (*Engage, Explore, Explain, Elaborate, Evaluate*), makes the idea physical before the game:
1.  **Feel it:** Drizzle vs. Downpour? Beans on a tray show steady rays vs. a sudden storm.
2.  **Try it:** A paper sheet with holes is the shield. How many beans get through?
3.  **Decide it:** Groups plan on token boards, vote on whiteboards (so the loudest voice doesn't decide), then play on the projector.
4.  **Evaluate it:** A 6-question exit ticket linked to 5 specific learning objectives.

---

## 📊 Real Data, Honestly Labelled
| Source | What we use it for |
|---|---|
| **NASA DONKI** | The strongest solar flare of the last 30 days sets the severity of the live storm. |
| **Curiosity RAD** | About 0.64 mSv a day on the Mars surface anchors the radiation meter. |
| **NASA OSDR (OSD-71)** | A blood-sample response to radiation, cited in the end report. |
| **Mission records** | Apollo 13, Opportunity, Artemis II, MOXIE, etc., drive the real-mission scenarios. |
| **NASA career limit** | 600 mSv (NASA-STD-3001) gives context for dose. |

Facts are tagged so kids know what kind of fact they are reading:
*   **LIVE:** fetched from NASA at run time.
*   **RECENT:** from a rolling 30-day archive.
*   **HISTORICAL:** a real record of a past event.
*   **EXAMPLE:** a typical day, not a record.
*   **ANALOG:** an Earth-based practice mission.
*   **MODEL NUMBERS:** practice numbers made up for a lesson are clearly labelled.

*If NASA's live feed fails (e.g., on a school network), the game says it is in **archived-data mode** and never presents archived data as live.*

---

## ⚠️ Known Limitations
*   **Flares vs. particle events:** The live feature uses DONKI flare data. Astronaut dose comes mostly from solar energetic particle events (DONKI also lists these). The flare class sets game storm severity.
*   **"Live" means the last 30 days:** It shows the strongest flare in that window, not today's exact conditions.
*   **API key:** The live fetch uses NASA's public `DEMO_KEY`, which is rate-limited and can fail on shared networks. A personal key is planned for schools.
*   **Not yet piloted:** The lessons have not yet been tested with a full classroom of students (planned next).

---

## 🚀 What's Next
1.  **Pilot** the 45-minute lesson with each age band in real classrooms.
2.  **Measure** with the exit ticket to see which ideas land.
3.  **Improve** the API key handling and expand the lesson plans based on teacher feedback.

---

## 🛠️ How to Run
No build step and no account needed.
1.  Download the repository.
2.  Open **`index.html`** in any modern browser.
3.  Press **Launch the game**.

*(Note: An internet connection is needed for live NASA data and for the fonts/three.js library loaded from CDNs).*

**Built with:** Plain HTML, CSS, and JavaScript. `three.js` (r128) for the 3D game scenes. NASA's public APIs.

---

## 📜 Credits and Disclaimer
Facts come from NASA (DONKI, OSDR, Curiosity RAD, Artemis, MOXIE, JPL), NOAA SWPC, and the other sources listed on the in-app Sources page.

This is an unofficial educational project and is **not affiliated with or endorsed by NASA, NOAA, or JAXA.** Certificates are for fun and learning, not official awards.

*Created by Fatima Emad for the 2026 NASA Space Apps Challenge.*
