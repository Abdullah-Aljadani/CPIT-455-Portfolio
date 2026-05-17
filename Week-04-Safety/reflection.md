# 🚀 Weekly Reflection: Week 04

## 📌 Safety-Critical Systems Engineering (Autonomous Car Braking System)
This week focused on engineering high-stakes, safety-critical software. Unlike human drivers who can intuitively "feel" hardware anomalies like brake fade, an AI system relies entirely on sensor data and electronic actuators. Using the **ISO 26262 standard**, a systematic safety analysis was conducted for an **Autonomous Car Braking System**.

---

## 🛑 1. Hazard Identification & Severity
When engineering critical systems, identifying the worst-case scenario is the top priority.
* **Identified Hazard:** Unintended Acceleration or Failure to Decelerate.
* **Potential for Harm:** Extremely high. A failure here leads to high-speed collisions with obstacles, other vehicles, or pedestrians, resulting in fatalities and catastrophic property damage.

---

## 📊 2. Risk Assessment Matrix & ASIL Classification
Automotive systems use the **ISO 26262 standard** to determine the **ASIL (Automotive Safety Integrity Level)**. Because of the critical nature of deceleration, braking systems are almost always classified as **ASIL D**—demanding the highest level of engineering rigor.

### 📉 Risk Matrix Evaluation
| Probability | Negligible | Marginal | Critical |
| :--- | :--- | :--- | :--- |
| **Frequent (City Driving)** | Medium | High | **Extreme** |
| **Probable** | Low | Medium | High |
| **Occasional** | Low | Medium | High |
| **Remote** | Low | Low | Medium |

* **Risk Assessment:** Because an autonomous vehicle operates for thousands of hours on the road (**High Exposure**) and a human driver cannot intervene in time during a sudden crisis (**Low Controllability**), any failure within this system is classified as an **Extreme Risk**.

---

## 🔒 3. Formulating Safety Requirements
To mitigate this extreme risk, the system architecture must enforce "fail-operational" or "fail-safe" behaviors. The following high-level software safety requirement was defined:

> **System Requirement:** *"The system shall not inhibit braking commands from the Perception Layer when an object is detected within the Critical Safety Envelope (d < d_safe), regardless of software state."*

---

## 🧠 Key Engineering Takeaway
In safety-critical engineering, software state must never compromise physical safety. Designing an ASIL D system means guaranteeing that even if the software encounters an unexpected state or error, the ultimate fail-safe mechanism (like emergency braking) remains absolute and uninhibited.
