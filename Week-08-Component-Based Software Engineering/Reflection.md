# 🚀 Weekly Reflection: Week 08

## 📌 Component-Based Software Engineering (CBSE Strategy)
This week's focus was on **Component-Based Software Engineering (CBSE)** and exploring the architectural power of *Development with Reuse*. Using the **Najm Application** as a case study, the analysis shifted from building features from scratch to the orchestration of highly mature, existing core components to optimize reliability, budget, and deployment speed.

---

## 🏗️ 1. Positioning in CBSE & Planning Factors
For a large-scale national platform like Najm, integrating industry-standard components is far more efficient than custom development. The architectural decision was driven by three core planning factors:
* **Market Availability:** Utilizing highly stable, pre-existing solutions for critical paths, such as **Google Maps SDK** for geospatial tracking and **Nafath** for trusted identity verification.
* **Development Schedule:** Leveraging off-the-shelf components allows the rapid deployment of complex system capabilities (like instant damage assessment), ensuring strict project deadlines are met.
* **Budget Optimization:** Licensing specialized, pre-secured corporate services proves significantly more cost-effective than absorbing the long-term overhead of in-house development and continuous maintenance.

---

## 🧩 2. Component Composition & Interface Design
To maintain system modularity, the infrastructure relies on explicit communication boundaries between independent components using strict **Requires/Provides** interface contracts:
