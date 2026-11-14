# Junior Astronaut Mission Trainer: Houston, We Have a Choice

**A free website where kids ages 7–12 learn how NASA keeps astronauts alive, then press Play to run the mission themselves in a game.**

Built for the **2026 NASA Space Apps Challenge: Build a Junior Astronaut Mission Trainer**.

**Author:** Fatima Emad, data scientist and STEM teacher (three years teaching Math, Programming and Data Science to ages 4–18).

> "If you want to build a ship, teach them to yearn for the vast and endless sea." (after Antoine de Saint-Exupéry)

---

## The problem

Kids hear that space is dangerous, but they never get to *decide* anything. A video says "space is dangerous." A game lets a child choose, and understand why.

The challenge asks: how do you make a 9-year-old feel a real space trade-off by deciding, not by watching?

## The solution

One website, no download and no account. Kids learn the idea in a world they understand, then press **Play** and the game opens right on the page. Every choice has a cost, so there is no "safe" option.

## What's on the website

| Section | What it does |
|---|---|
| **Home** | Mission briefing, progress bar, rank, and the ten real NASA and NOAA events the project is built on |
| **Play** (Launch the game) | Opens **Deep Space Run** inside the page |
| **Lessons** | 13 mission lessons, each built on a real event and written for Cadets, Navigators and Commanders, with a voice guide you can play |
| **Certificates** | Finish a lesson to unlock its certificate; finish all 13 for the Mission Commander award. Type an astronaut name and print or save as PDF |
| **How to play** | Plain-language rules for the game |
| **Sources** | Where every fact comes from, with the data tags explained |
| **For teachers** | Teacher guide, including accuracy notes |

Other touches: a sound on/off button, and progress saved in the browser.

## The game: Deep Space Run

Press **Play** and the game appears on the page. Players launch, steer through rocks, collect supplies and survive solar storms. Landing at the Station, the Moon or Mars lets them grow space lettuce and earn the Space Farmer certificate.

Game modes and features:

- **Mars Outpost:** run a base for 8 sols (Martian days), splitting a few power units each sol between air, food, shield, comms and science
- **Real mission files:** seven historical missions (Artemis II, Apollo 13, Opportunity, Lunar Night, MOXIE, Veggie Harvest, radio delay)
- **Cabin training:** run the cabin on 5 power units while a solar storm is coming
- **Storm replays and a live storm:** replay real storms, or face the strongest NASA DONKI flare of the last 30 days
- **Analog missions:** Earth-based practice (CHAPEA, HERA, Desert RATS, BASALT, NEEMO)
- **Progression:** collectible NASA cards and ranks from Space Cadet to Flight Director

### The trade-off, in Mars Outpost

| Spend power on | What it does |
|---|---|
| Life support | 2 units hold the air steady |
| Radiation shield | Each unit blocks 25% of a storm (max 75%) |
| Greenhouse | Each unit makes 3 food for the next sol |
| Comms to Earth | 1 unit shows tomorrow's forecast |
| Science | 10 research points per unit (the score) |

Players watch three meters: air, food and radiation. Power per sol depends on age band: Cadets (7–8) get 7 units, Navigators (9–10) get 6, Commanders (11–12) get 5.

Radiation added by one X9.0-class storm, as a share of the mission limit:

| Shield units | Radiation added |
|---|---|
| 0 | 29.0% |
| 1 | 22.0% |
| 2 | 14.5% |
| 3 | 7.2% |

Three shield units cut the dose by about three quarters, but those units can no longer grow food or do science. The rule is `(4 + storm size) × (1 − shield)`.

> **Honesty note:** storm sizes are the game's own design values, not NASA dose measurements. The game says so on screen.

## In the classroom

A 45-minute 5E lesson, "Houston, We Have a Choice," makes the idea physical before the game:

1. **Feel it:** drizzle or downpour? Beans on a tray show steady rays versus a sudden storm.
2. **Try it:** a paper sheet with holes is the shield. How many beans get through?
3. **Decide it:** groups plan on token boards, vote on whiteboards (so the loudest voice does not decide), then play on the projector.

The paper shield is an analogy: real shields cost mass and power and never make a crew invincible. Materials include a 6-question exit ticket (5 objectives), a mission log and an answer key. Because the website runs in a browser, children can also play at home with siblings and parents.

## Real data, honestly labelled

| Source | What we use it for |
|---|---|
| **NASA DONKI** | The strongest solar flare of the last 30 days sets the severity of the live storm |
| **Curiosity RAD** | About 0.64 mSv a day on the Mars surface anchors the radiation meter |
| **NASA OSDR (OSD-71)** | A blood-sample response to radiation, cited in the end report (the game does not simulate biology) |
| **Mission records** | Apollo 13, Opportunity, Artemis II, MOXIE and others drive the real-mission scenarios |
| **NASA career limit** | 600 mSv (NASA-STD-3001) gives context for dose |

Facts are tagged so kids know what kind of fact they are reading:

- **LIVE:** fetched from NASA at run time
- **RECENT:** from a rolling 30-day archive
- **HISTORICAL:** a real record of a past event, not a forecast
- **EXAMPLE:** a typical day, not a record
- **ANALOG:** an Earth-based practice mission

Practice numbers made up for a lesson are labelled "model numbers." If NASA's live feed fails (for example on a school network), the game says it is in **archived-data mode** and never presents archived data as live.

## Known limitations

- **Flares vs particle events:** the live feature uses DONKI flare data. Astronaut dose comes mostly from solar energetic particle events, which DONKI also lists. The flare class sets game storm severity.
- **"Live" means the last 30 days:** it shows the strongest flare in that window, not today's conditions.
- **API key:** the live fetch uses NASA's public `DEMO_KEY`, which is rate-limited and can fail on shared networks. A personal key is planned.
- **Not yet piloted:** the lessons have not yet been tested with students.

## What's next

1. **Pilot** the 45-minute lesson with each age band.
2. **Measure** with the exit ticket to see which ideas land.
3. **Improve** what students show us (one radio-delay range, a personal NASA API key for school networks, clearer wording).
4. **Share** the teacher pack (lesson plan, mission log, answer key) so other teachers can run it.

## Run it

No build step and no account. Download the repository and open `Junior_Astronaut_Mission_Trainer.html` in a modern browser, then press **Launch the game**.

An internet connection is needed for live NASA data and for the fonts and three.js library loaded from CDNs.

## Built with

Plain HTML, CSS and JavaScript in a single file, three.js (r128) for the game's 3D scenes, and NASA's public APIs.

## Credits and disclaimer

Facts come from NASA (DONKI, OSDR, Curiosity RAD, Artemis, MOXIE, JPL), NOAA SWPC and the other sources on the in-app Sources page.

This is an unofficial educational project and is not affiliated with or endorsed by NASA, NOAA or JAXA. Certificates are for fun and learning, not official awards.

*Created by Fatima Emad for the 2026 NASA Space Apps Challenge.*
