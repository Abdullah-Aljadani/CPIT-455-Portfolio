# 🚀 Weekly Reflection: Week 02

## 📌 Case Study: Dependability Analysis of the Najm App
This week, the focus shifted toward applying engineering principles to a real-world system: the **Najm Application (Traffic Accident Management System)**. 

Najm is classified as a **Socio-Technical System** because its success heavily relies on the real-time interaction between technology (app/GPS), processes (insurance/legal regulations), and people operating under high stress. It serves as a critical platform connecting vehicle owners, liability investigators, and insurance companies.

---

## 💡 Critical Dependability Attributes Prioritized
To ensure the system functions reliably within its chaotic real-world environment, three core attributes were analyzed and prioritized:

* **Availability:** The system must be accessible at any given moment. Unavailability leads directly to severe traffic congestion and delays in legal procedures.
* **Reliability:** Accurately capturing and transmitting GPS coordinates and accident photos is crucial for evidence preservation. Corrupted data could lead to incorrect liability assignment.
* **Security:** The system processes highly sensitive Personal Identifiable Information (National IDs, license plates, insurance policies), making data protection a strict legal and ethical requirement.

---

## 🔍 Analysis of Failure Sources
True to the engineering mindset of identifying potential risks, the threats to the system were classified into three core layers:

### 1. Operational Failure (Primary Risk)
* **Context:** Human error is the most significant threat. 
* **Scenario:** Drivers involved in accidents are often panicked or stressed. A user might input incorrect vehicle data or fail to follow photography guidelines, causing a *process failure* even if the software works perfectly.

### 2. Environmental / Hardware Failure
* **Context:** The unpredictable physical environment where accidents occur.
* **Scenario:** Poor network connectivity (4G/5G) at the accident site, or hardware limitations like a low-quality camera or a dying phone battery preventing data upload.

### 3. Software Failure
* **Context:** Logic or coding errors within the application.
* **Scenario:** The application crashing during high-load periods, such as heavy rainstorms when accident rates spike significantly and overload the system.

---

## 🛠️ Proposed Dependability Strategies
To mitigate these risks and build a system that people can trust, the following architectural and design strategies were proposed:

| Risk Category | Strategy | Engineering Implementation |
| :--- | :--- | :--- |
| **Environmental Risks** | **Fault Tolerance** | Develop a robust **"Offline Mode"** to locally cache photos and incident reports, automatically synchronizing data once connectivity is restored. |
| **Operational Risks** | **Fault Prevention** | Design a **"Stress-Resistant" User Interface (UI)** with simplified layouts, large buttons, and automated data entry (e.g., scanning license plates) to minimize human error. |
| **Software Risks** | **Verification & Validation** | Conduct rigorous **Stress and Scalability Testing** under simulated "surge" conditions (e.g., 10x normal traffic) to ensure infrastructure stability. |

---

## 🧠 Key Engineering Takeaway
This analysis proved that engineering dependable systems means designing for the worst-case scenario. A resilient system must not only have solid code, but it must also withstand human panic, poor network environments, and sudden operational spikes.
