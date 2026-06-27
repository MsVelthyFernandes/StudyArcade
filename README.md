# StudyArcade

A platform that combines the structure of a Learning Management System (LMS) with the immersive engagement of modern gamification and the adaptive power of AI.
Designing learning as an interactive adventure (resembling a Role-Playing Game, or RPG), to shift student's mindset from passive compliance ("I have to pass this test") to active progress ("I want to level up my skills").

Teacher_interface_guide.md
# StudyArcade AI — Teacher Interface Documentation

Welcome to the **StudyArcade AI Teacher Interface**. This document serves as a complete functional and design reference guide for the educator-facing dashboard of the StudyArcade platform.

---

## 📋 1. Nested Navigation Control Sub-Tabs
The Teacher control room features a clean, responsive sub-tab navigation bar allowing instructors to seamlessly cycle through critical educational administration tasks:

1. **Roster (Student Guild Ledger)**: Review, search, and manage students.
2. **Gemini Quest Architect (Curriculum & Forge)**: Build, edit, and gamify homework assignments and quests.
3. **Performance Advisor (AI Analytics)**: Evaluate class-wide trends and summon generative progress reports.
4. **Profile & Classroom Settings**: Reconfigure class identifiers, subject matrices, and administrative presets.

---

## 👥 2. Student Guild Ledger (Roster Tab)
The **Student Guild Ledger** provides a birds-eye view of your student body, reimagined as a heroic adventurers guild.

* **Class Analytics Stats Grid**: Displays visual indicators for Class Size, Combined Guild Level, and Quests Completed.
* **Student Roster Search**: A real-time filterable directory by student name or RPG class.
* **Dynamic Student Cards**: Displays each student's current lvl, class, active quest counts, collected inventory gold, and level-up progress.
* **Direct Manual Aid**: Teachers can directly award bonus items, custom XP boosts, or administrative gold directly to a student to motivate struggling learners.

---

## 🛡️ 3. Gemini Quest Architect Dashboard (rpg_architect Tab)
This dashboard is the command center for lesson creation, quest deployment, and curriculum gamification.

### A. Handcrafted Homework Activity Forge (Activity Creator & Editor)
A robust form allowing educators to author homework exercises that seamlessly translate into RPG-style quests for students:
* **Curriculum Fields**: Customize the Activity Title, Description, Subject Category, Skill Lock/Unlocks, and XP/Gold rewards.
* **Adaptive Quiz Creator**: Directly attach multiple-choice questions complete with four custom options, a correct answer, and an adaptive hint.
* **Persistent Activity Editor**:
  * Clicking the **✏️ Edit** button on any deployed activity instantly populates the Forge form.
  * Teachers can refine spelling, correct formulas, update multiple-choice questions, or balance rewards.
  * Submitting changes instantly saves and updates the activity across the student portal in real-time.

### B. AI Gamifier Theme Engine
A powerful portal powered by Gemini that adapts raw study material into deep-lore campaigns.
* **Custom Lore Settings**: Select a narrative setting such as **Cyberpunk Dungeon**, **Cosmic Void**, **High-Fantasy Guild**, or **Steampunk Airship**.
* **AI Gamify Action**:
  * Selecting any handcrafted activity and hitting **✨ Gamify** triggers the server-side Gemini API.
  * The API automatically rewrites titles, descriptions, and quiz prompts to weave the specified theme's lore around the educational objective.
  * For example, a basic math problem becomes a calculation to calibrate the energy core of a Steampunk Airship!

---

## 📊 4. Performance Advisor Dashboard (performance_advisor Tab)
The Performance Advisor bridges the gap between analytics and action by translating cold student data into actionable instructional strategies.

* **Generative Class Summarizer**:
  * Selecting an active classroom and clicking **"Brew AI Analytics Summary"** invokes our server-side Gemini model.
  * The model processes active quest volumes, roster averages, and completed metrics to output a high-fidelity narrative of class status.
* **Strategic Pedagogical Recommendations**:
  * Renders custom pedagogical strategies (e.g., advising XP booster events to boost engagement, initiating peer-guided study groups, or highlighting specific logic nodes requiring manual teacher intervention).

---

## ⚙️ 5. Profile & Classroom Settings (profile_settings Tab)
Configure classroom-wide parameters and regional curriculum setups:
* Customize the Master Class Name (e.g., *Alpha Core*, *Beta Logic*).
* Update the principal academic discipline (e.g., *Computer Science*, *Algebra*, *Physics*, *World History*).
* Instantly sync custom configurations to synchronize with student views, realigning their default curriculum maps.

Student_Interface_guide.md
# StudyArcade AI — Student Interface Documentation

Welcome to the **StudyArcade AI Student Interface**. This document serves as a complete functional and design reference guide for the gamified student-facing environment of the StudyArcade platform.

---

## 🌅 1. Interactive Student Banner & Character Dashboard
Located at the top of the interface, the Student Banner operates as an RPG-style character status screen. It visually encapsulates the student's progress and active status.

* **Character Level**: Displayed in a high-contrast badge. Leveling up occurs immediately when the XP gauge is filled.
* **Hero Class & Topic Realignment**: An active dropdown allows students to shift their "Hero Class/Subject" dynamically:
  * **Code Wizard** (Computer Science)
  * **Algebra Ranger** (Mathematics)
  * **Science Alchemist** (Science)
  * **History Paladin** (History)
  * Changing a hero class instantly realigns the adaptive skill tree paths and default curriculum quests.
* **XP Gauge (Experience Points)**: A visual progress bar detailing current XP and progress toward the next milestone.
* **Vitality Bars**:
  * **HP (Health Points)**: Tracks learning stamina.
  * **Mana**: Energy used to summon personalized exercises. Spending **15 Mana** calls the Gemini Oracle to materialize custom quests.
* **Wealth & Inventory**:
  * **Gold Cache**: Earned by completing quests; spent on unlocking or leveling up skills.
  * **Inventory Bag**: Displays acquired epic items, e.g., the *Amulet of the Flash-Lite* or *Arcane Scroll*.

---

## 🗺️ 2. Adaptive Skill Tree Map
The **Adaptive Skill Tree** represents the student's current curriculum mapped as a celestial constellation.

* **Dynamic Constellation Pathing**: High-fidelity SVG lines connect curriculum topics (e.g., *Variables*, *Conditionals*, *Functions*, *Recursion*). Path colors transition from deep slate (unlocked/inactive) to bright emerald (active and fully connected).
* **Pre-requisite Locking (🔒)**: Sub-nodes require unlocking previous parent nodes. Students must build foundational knowledge before entering advanced realms.
* **Node Upgrading & Unlocking**:
  * **Upgrade Rank (costs 50 Gold)**: Increments skill rank/level.
  * **Unlock Node (costs 100 Gold)**: Unlocks new advanced sub-nodes once pre-requisites are fulfilled.
* **Dynamic Study Quest Materialization ("Learn" button)**: Selecting any unlocked node and clicking "Learn" consumes Mana to invoke the server-side Gemini API. This generates an immediate, customized quiz quest based on that node's educational description.

---

## 📜 3. Active Chronicles (Quest Log)
The Chronicles panel serves as the active homework and study planner.

* **Quest Categories**: Displays available, currently in-progress, or completed assignments.
* **Metadata & Rewards**:
  * **Difficulty Rating**: Novice, Apprentice, Expert, etc.
  * **Loot Drops**: Outlines exactly what XP, Gold, and inventory item rewards will be gained upon completion.
* **Task Lists**: Shows required milestones for the quest, such as reading curriculum scrolls followed by solving active challenges.

---

## 🔮 4. The Alchemical Quest Console (Quiz & Oracle)
Selecting an active chronicle opens the interactive learning workspace.

* **The Challenge Arena**: Presents multiple-choice curriculum questions with custom interactive choices.
* **Interactive Evaluation**: Submitting responses triggers immediate validation (correct or incorrect feedback indicators).
* **Ask AI Hint (The Gemini Oracle)**:
  * When a student gets stuck on a question, they can consult the **Gemini Oracle**.
  * This calls our custom backend API, analyzing the question, choices, and selected answer, then rendering a contextual, helpful hint.
  * Also receives a motivational quote from legendary academy masters (such as *Archmage Sandy*) to incentivize persistent revision.
* **Quest Completion**: Completing all tasks successfully awards Gold and XP, adding the custom items into the student's inventory bag instantly.


 

