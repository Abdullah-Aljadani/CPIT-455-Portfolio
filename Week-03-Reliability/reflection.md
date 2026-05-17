# 🚀 Weekly Reflection: Week 03

## 📌 Reliability Engineering in Critical Systems (Najm App)
This week focused on a deep dive into **Reliability Engineering** and software dependability patterns, applying these core concepts to the **Najm Application** case study. The goal was to systematically define user profiles, choose the correct engineering metrics, and propose architectural strategies to prevent system failures.

---

## 👥 1. System Profile & Usage Pattern
Understanding *how* a system is used is the first step in engineering its reliability. For the Najm application:
* **Target Users:** Vehicle drivers in Saudi Arabia who are involved in traffic accidents.
* **Usage Pattern:** **Intermittent and Critical.** Users do not interact with the app continuously; instead, they request its services strictly during emergencies when an accident occurs.

---

## 📊 2. Engineering Metric Selection: POFOD
Selecting the right metric defines how system success is quantified. For Najm, the chosen metric is **POFOD (Probability of Failure on Demand)**.

### 🔍 Justification:
* **Why POFOD?** According to software dependability principles, POFOD is specifically tailored for critical systems with intermittent use. 
* **The Context:** Najm does not handle continuous high-volume transactions (which would require **ROCOF**), nor is its primary focus merely minimizing general downtime (**AVAIL**). 
* **The Real-World Impact:** The most critical objective is ensuring the system does not fail at the exact millisecond a user demands it. A failure on demand means a user is left stranded on the road, directly causing massive traffic disruption. Therefore, ensuring the system responds to every single emergency request is the true measure of its reliability.

---

## 🏗️ 3. Architectural Strategy: Redundancy Pattern
To guarantee high reliability during critical moments, an architectural decision based on the **Redundancy Pattern** was established.

* **Description:** Redundancy involves running multiple identical components in parallel to safeguard against hardware failure.
* **Implementation for Najm:** Deploying redundant servers to handle extreme spikes in system load.
* **The Scenario:** During severe weather conditions (e.g., heavy rain), traffic accidents increase drastically, causing sudden spikes in application demand. 
* **The Mechanics:** Having redundant servers ensures that if a **Fault** occurs in a primary active server, a backup redundant server takes over immediately. This prevents the internal **Error** from transitioning into a complete **Failure** visible to the user.

---

## 🧠 Key Engineering Takeaway
True reliability engineering means aligning system architecture with real-world human behavior. By designing for an *intermittent yet critical* demand pattern, we shift our focus from generic uptime to absolute readiness—ensuring the system stands resilient when the user needs it most.
