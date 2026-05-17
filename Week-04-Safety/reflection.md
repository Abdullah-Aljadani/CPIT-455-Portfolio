# 🚀 Weekly Reflection: Week 04

## 📌 Safety-Critical Systems Engineering (Autonomous Car Braking System)
This week focused on engineering high-stakes, safety-critical software. [cite_start]Unlike human drivers who can intuitively "feel" hardware anomalies like brake fade [cite: 4][cite_start], an AI system relies entirely on sensor data and electronic actuators[cite: 4]. [cite_start]Using the **ISO 26262 standard**, a systematic safety analysis was conducted for an **Autonomous Car Braking System**[cite: 3, 9].

---

## 🛑 1. Hazard Identification & Severity
When engineering critical systems, identifying the worst-case scenario is the top priority.
* [cite_start]**Identified Hazard:** Unintended Acceleration or Failure to Decelerate[cite: 6].
* [cite_start]**Potential for Harm:** Extremely high[cite: 7]. [cite_start]A failure here leads to high-speed collisions with obstacles, other vehicles, or pedestrians, resulting in fatalities and catastrophic property damage[cite: 7].

---

## 📊 2. Risk Assessment Matrix & ASIL Classification
[cite_start]Automotive systems use the **ISO 26262 standard** to determine the **ASIL (Automotive Safety Integrity Level)**[cite: 9]. [cite_start]Because of the critical nature of deceleration, braking systems are almost always classified as **ASIL D**—demanding the highest level of engineering rigor[cite: 10].

### [cite_start]📉 Risk Matrix Evaluation [cite: 11]
| Probability | Negligible | Marginal | Critical |
| :--- | :--- | :--- | :--- |
| **Frequent (City Driving)** | Medium | High | **Extreme** |
| **Probable** | Low | Medium | High |
| **Occasional** | Low | Medium | High |
| **Remote** | Low | Low | Medium |

* [cite_start]**Risk Assessment:** Because a autonomous vehicle operates for thousands of hours on the road (**High Exposure**) and a human driver cannot intervene in time during a sudden crisis (**Low Controllability**), any failure within this system is classified as an **Extreme Risk**[cite: 12].

---

## 🔒 3. Formulating Safety Requirements
[cite_start]To mitigate this extreme risk, the system architecture must enforce "fail-operational" or "fail-safe" behaviors[cite: 13]. The following high-level software safety requirement was defined:

> [cite_start]**System Requirement:** *"The system shall not inhibit braking commands from the Perception Layer when an object is detected within the Critical Safety Envelope ($d < d_{safe}$), regardless of software state."* [cite: 14]

---

## 🧠 Key Engineering Takeaway
In safety-critical engineering, software state must never compromise physical safety. [cite_start]Designing an ASIL D system means guaranteeing that even if the software encounters an unexpected state or error, the ultimate fail-safe mechanism (like emergency braking) remains absolute and uninhibited[cite: 10, 14].
