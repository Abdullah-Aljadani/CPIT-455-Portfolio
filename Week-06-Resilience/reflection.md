# 🚀 Weekly Reflection: Week 06

## 📌 System Resilience & The Mechanics of Failure (Najm App)
This week focused on advanced software resilience engineering, examining how systems anticipate, resist, and recover from cascading disruptions. Using the **Najm Application** as a case study, the complete lifecycle of a failure was mapped alongside multi-layered defense strategies to prevent catastrophic outages.

---

## 🔗 1. The Failure Chain Analysis
To engineer truly resilient systems, we must trace how an isolated low-level anomaly propagates into a visible user-facing outage. The breakdown follows this distinct progression:

* **Fault (The Defect):** A localized memory leak within the image-processing module dedicated to uploading accident photos.
* **Error (Internal State):** Severe exhaustion of the server's RAM, driving that specific microservice into an "Out of Memory" state.
* **Failure (Service Deviation):** The application crashes entirely or prevents the user from submitting their accident report, blocking access to vital emergency assistance.

---

## 📊 2. Recognition & Resistance (R&R) Strategy
Minimizing downtime requires implementing automated barriers to catch defects early and isolate their impact:

| Strategy | Applied Engineering Technique | Operational Goal |
| :--- | :--- | :--- |
| **Recognition** | **Heartbeat Monitoring & Threshold Alerts:** Automated monitors track real-time CPU/RAM usage. If metrics cross a 90% threshold, an instant alert triggers to catch the memory leak *before* a total crash. | Detect anomalies proactively prior to runtime system collapse. |
| **Resistance** | **Graceful Degradation (Feature Isolation):** If the image microservice drops, the app automatically shuts down photo uploads while keeping critical GPS tracking and text-based reporting active. | Safeguard core capabilities (notifying a recovery agent) even when secondary features fail. |

---

## 🧀 3. The Swiss Cheese Model of System Failure
System safety relies on multiple defense boundaries. A total system collapse only happens if vulnerabilities across all independent layers align perfectly.
