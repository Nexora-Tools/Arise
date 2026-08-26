# Website : https://nexora-tools.github.io/Arise/

# ⚔️ ARISE // THE SYSTEM

A standalone fitness RPG web application that transforms workouts into a game-like progression system.

ARISE turns the Player's fitness journey into a personal System with:

- ⚡ Daily Quests
- 🎮 XP & Levels
- 🔷 RPG Ranks
- 📊 Player Stats
- 🔥 Streaks
- 🏆 Achievements
- 🏋️ Workout Tracking
- ⏱️ Guided Workout Timer
- ⚖️ Weight Tracking
- 🔥 Estimated Calorie Expenditure
- 🥗 Nutrition Estimates
- 🧠 System Coach
- 🛌 Recovery Logic
- 💾 Local Data Storage

The project focuses on combining fitness, gamification, and interactive web design while keeping calculations and progression transparent.

---

## 👤 About Me

I'm the creator behind Nexora, interested in building modern websites, useful digital tools, and interactive web experiences.

I enjoy experimenting with technology and combining functionality with distinctive interfaces.

ARISE is one of my personal projects exploring how fitness tracking can be redesigned as an RPG-style experience.

---

## 🎮 Core System

The Player progresses through a game-like fitness system.

The application generates daily quests based on the Player's stored profile and training state.

SYSTEM ONLINE

PLAYER DETECTED

PROFILE CREATED

QUEST ENGINE ACTIVE

PROGRESSION SYSTEM ACTIVE

RECOVERY SYSTEM ACTIVE

AWAITING PLAYER ACTION...

The goal is simple:

> Train. Progress. Level Up.

---

## 📊 Player Stats

The Player dashboard displays:

- STRENGTH
- ENDURANCE
- AGILITY
- VITALITY
- DISCIPLINE
- POWER

Stats increase through level progression.

These are RPG/game statistics and are not medical measurements.

---

## 🔷 Rank System

Ranks progress through:

E → D → C → B → A → S → SS → SSS

Rank is calculated from the Player's statistics and consistency.

The current implementation does not use body weight alone to determine rank.

---

## 🔥 Streak System

Completed quests increase the Player's streak.

The current implementation includes achievements for:

- 7-day streak
- 30-day streak

Missing a quest resets the current streak.

Missing a quest also removes 50 XP, with the XP prevented from going below zero.

---

## 🏆 Achievements

The current code contains these achievement definitions:

| Achievement | Requirement |
|---|---|
| First Quest | Complete first quest |
| First Workout | Log first workout |
| 7 Day Streak | Reach 7-day streak |
| 30 Day Streak | Reach 30-day streak |
| 100 Workouts | Complete 100 workouts |
| First Personal Record | Set first PR |
| 1000 Total Reps | Achievement definition exists |
| 10 Hours Training | Log 10 hours |
| Consistency King | Complete 5 quests in a week |
| Early Awakening | Complete a quest before 8 AM |
| Boss Defeated | Achievement definition exists |
| Rank D Reached | Reach Rank D |

Some achievement definitions currently exist without a complete unlock implementation.

---

## 📈 Personal Records

The System records personal records for rep-based exercises.

For example:

PUSH-UP  
Best: 32 reps

A new record is stored when the current repetition value exceeds the previous stored value.

---

## ⚖️ Weight Tracking

Players can record their body weight.

Weight entries are stored with:

- date
- weightKg

The Progress screen displays the recorded weight trend.

The interface also explains that short-term weight changes can have causes other than changes in body fat.

---

## 🔥 Calorie Estimation

The application calculates BMR using the Mifflin-St Jeor equation.

### Male

10 × weight  
+ 6.25 × height  
- 5 × age  
+ 5

### Female

10 × weight  
+ 6.25 × height  
- 5 × age  
- 161

TDEE is estimated using the selected activity multiplier.

The application also calculates a suggested calorie target based on the selected goal.

Calorie results are explicitly presented as estimates rather than exact measurements.

---

## 🏃 Exercise Calorie Estimation

Exercise calories are estimated using MET values.

The current code contains MET values for the exercises in the database.

The calculation is:

Calories/minute = MET × 3.5 × body weight(kg) / 200

The result is treated as an estimate rather than an exact measurement.

Workout logs store a lower and upper estimate using an 85%–115% range around the calculated value.

---

## 🥗 Nutrition Screen

The Nutrition screen displays:

- Estimated daily calorie target
- BMR
- Estimated TDEE
- Protein estimate
- Carbohydrate estimate
- Fat estimate
- Fat-loss explanation
- Warning when the calculated target is unusually low

The current application does not contain food logging or a food database.

---

## 🧠 System Coach

The Profile screen contains a built-in System Coach.

Current preset questions include:

- What should I do today?
- Why this workout?
- Can I replace an exercise?
- I missed yesterday.

The current coach uses local JavaScript responses based on the current System state.

It is not connected to an external AI API.

---

## 📜 Workout History

Completed quests are stored in the workout log.

Each entry can contain:

- Date
- Exercises
- Sets
- Repetitions
- Duration
- Estimated calories
- XP
- Completion status
- Recovery status

The Progress screen displays recent workout entries.

---

## 💾 Local Storage

Player data is stored locally in the browser using localStorage.

Storage key:

arise_system_state_v1

The stored state contains:

- Player profile
- XP
- Level
- Streak
- Rank
- Stats
- Achievements
- Workout history
- Personal records
- Weight history
- Quest state
- Fatigue reports
- Settings

No backend database is required for the current version.

---

## 📤 Data Export

The Profile screen provides:

Export Workout Data (JSON)

The current System state can be exported as a JSON file.

---

## ⚙️ Settings

The current settings include:

- Sound
- Animations
- Notifications
- Reduced Motion

These settings are stored in localStorage.

---

## 🗑️ Reset Data

The Profile screen includes:

Delete Account / Reset Data

This removes the application's local storage data and reloads the application.

The current implementation does not delete a server account because there is no server account system.

---

## 📱 Navigation

The application uses five bottom navigation sections:

- HOME
- QUEST
- PROGRESS
- NUTRITION
- PROFILE

---

## 🎨 Interface

The current UI uses a futuristic RPG/HUD design.

Visual characteristics include:

- Dark interface
- Cyan system glow
- Violet rank accents
- Futuristic panels
- Glowing borders
- XP bars
- RPG rank indicators
- Full-screen timer
- Mobile navigation
- Responsive layout
- Animated transitions

### Fonts

- Orbitron
- Rajdhani
- Inter
- JetBrains Mono

---

## 🧩 Technologies

The current implementation is a standalone HTML application.

- HTML5
- CSS3
- JavaScript
- SVG
- localStorage
- Google Fonts

There is no React, TypeScript, Supabase, or external database in the code currently contained in this project.

---

## 📁 Project Structure

The current version can run as a single HTML file:

ARISE/
└── arise-fitness-rpg.html

The file contains:

- HTML
- CSS
- JavaScript
- Exercise Database
- Quest Engine
- XP System
- Level System
- Rank System
- Achievement System
- Timer
- Nutrition Calculations
- Recovery Logic
- Local Storage

---

## ⚠️ Current Limitations

The current code does not yet implement:

- User accounts
- Cloud synchronization
- Backend database
- Real AI API
- Food database
- Health API integration
- Wearable integration
- Social accounts
- Leaderboards
- Real push notifications
- Camera-based form analysis
- Video exercise demonstrations
- Full exercise substitution UI
- Full nutrition logging
- Advanced progress charts
- Actual Boss Battle system

These should not be represented as currently working features until implemented.

---

## 👤 Creator

### Nexora

A personal project exploring the combination of:

Fitness + Gamification + Web Development + Interactive UI

---

# ⚔️ ARISE // THE SYSTEM

SYSTEM ONLINE

PLAYER DETECTED

PROFILE CREATED

QUEST ENGINE ACTIVE

PROGRESSION SYSTEM ACTIVE

RECOVERY SYSTEM ACTIVE

AWAITING PLAYER ACTION...

**Train. Progress. Level Up.**
