⚙️ SensorMesh
Industrial IoT / Cooperative Intelligent Systems
A Synapse 1.0 Hackathon Submission by Team Recurrex
Heavy machinery is monitored by multiple sensors measuring temperature, pressure, vibration, and speed. In harsh environments, individual sensors frequently drift, miscalibrate, or fail. Currently, monolithic anomaly detectors trigger false plant shutdowns when a single sensor fails, even if the machine itself is perfectly healthy.  
SensorMesh solves this by tracking multivariate sensor streams and cross-validating readings using physical correlation rules to establish peer consensus. By distinguishing local sensor faults from true systemic machine degradation, we isolate faulty sensors without causing unnecessary emergency shutdowns.  
🚀 Core Features
Multivariate Telemetry Tracking: Processes and monitors 14+ channels of live industrial sensor data.  
Physical Correlation Consensus: Uses a graph-based voting protocol where sensors cross-validate each other based on known physical invariants.  
Fault Classification: Dynamically categorizes system states into NORMAL, LOCAL_SENSOR_FAULT, or SYSTEMIC_FAILURE.  
Real-Time Operations Dashboard: Visualizes live telemetry streams, the consensus matrix, and a GREEN / YELLOW / RED plant status indicator.  
🛠️ Tech Stack
Machine Learning & Data: Python, PyTorch, Scikit-Learn, Pandas (using the NASA C-MAPSS Turbofan Degradation dataset)  
Backend & Streaming: FastAPI, WebSockets, Python Async
Frontend & UI: React / Next.js, WebSockets, Charting Libraries (Recharts/Chart.js)
Algorithm: NetworkX (Graph-based physical invariant logic)
⚡ Judge Stress-Test Protocol
Our system is engineered to pass the following live stress test during the demo:  
Judge Action: Inject a sudden drift/spike into Sensor 2 and Sensor 7.  
Expected Pass Condition: The consensus matrix detects the anomaly but identifies it as a LOCAL_FAULT only. The overall plant status remains GREEN (running).  
Fail Condition Avoided: False plant shutdown.  
👥 Team Recurrex
Aritraa — Machine Learning & Data Engineering (C-MAPSS dataset prep, feature extraction, and anomaly detection model)
Prithwish — Frontend & UI Dashboard (14-channel real-time visualizer, consensus matrix grid, and status indicators)  
Arghya — Consensus Logic & Algorithm Design (Physical correlation mapping and voting protocol logic)
Debarghya — Backend API & Stream Infrastructure (FastAPI server, WebSocket data routing, and stress-test injection engine)
Built for the SYNAPSE 1.0 Hackathon (IEEE SMC KGEC × IEEE Kolkata Section)
