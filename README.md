# 🏭 SensorMesh

**Industrial IoT / Cooperative Intelligent Systems**

SensorMesh is a cooperative Industrial IoT platform designed to track multivariate sensor streams from heavy machinery. By utilizing physical correlation rules, the system cross-validates sensor readings to distinguish between a true systemic machine failure and a localized, false sensor fault.

This project was built for **SYNAPSE 1.0 (Synergy of Intelligent Systems)**, a National Flagship Hackathon. 

---

## ⚠️ The Problem

Heavy machinery operates in harsh environments, causing individual sensors (temperature, pressure, vibration) to drift, miscalibrate, or fail outright. Current monolithic anomaly detectors treat a single sensor failure as a systemic machine failure, triggering expensive and unnecessary false plant shutdowns.

## 🛠️ Our Solution

SensorMesh introduces a **Consensus Matrix** and a **Voting Protocol**. Instead of relying on single-point thresholds, our system cross-validates 14+ channels of telemetry. If a single sensor spikes but its physically correlated peers remain stable, the system isolates the faulty sensor and keeps the plant running.

### Key Features
*   **📡 14-Channel Telemetry Processing:** Ingests and processes multivariate streams in real-time.
*   **🤝 Cooperative Consensus Voting:** Cross-validates sensors using defined physical invariants.
*   **🚦 Smart Status Indicator:** Classifies state dynamically as `NORMAL`, `LOCAL_SENSOR_FAULT`, or `SYSTEMIC_FAILURE`.
*   **⚡ Live Stress Testing:** Handles injected anomalies mid-stream without crashing or stopping production.

---

## 🏗️ System Architecture

*   **Dataset:** NASA C-MAPSS Turbofan Degradation
*   **Perception Layer:** Statistical Feature Extraction & Z-Score Normalization
*   **Policy Layer:** Hybrid Rule-Based Invariants + Time-Series Classification
*   **Serving:** FastAPI backend routing via WebSockets to the UI
*   **Frontend:** Real-time multi-chart visualizer 

---

## 👨‍💻 Team Recurrex

*   **Aritraa Chakraborty** — Machine Learning & Data Engineering
*   **Debarghya** — Backend API & Stream Infrastructure
*   **Prithwish** — Consensus Logic & Algorithm Design
*   **Arghya** — Frontend & UI Dashboard


---

## 🚀 Setup & Installation (Coming Soon)

*(Instructions for local deployment, API endpoints, and running the live stream simulator will be added during the Pre-Finale build phase in October).*
