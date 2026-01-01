## Hi there 👋

My name is Martin, I'm an Engineering student in Electronics and ICT at KU Leuven. Interested in all things Cybersec and Data Science!

- 🔭 I’m currently working on creating an interactive website with html, css, and javascript for a friend of mine.

- 📚 I’m currently learning how to suistainably synchronize multiple threads and processes in C.

### About my repos:

#### One-line summaries 🔧🧩
1) sensor-gateway (C) -> December 2025 -> Two processes in one execution: A sensor gateway server recording data from sensors into a csv file in real-time, and a logger process printing messages in a .log file
2) jitter-analysis-and-UI (Python) -> August 2025 -> A tool that analyzes and visualizes the rising-edge jitter between two network slaves using oscilloscope-generated CSV data.
3) maker-link (Java) -> May 2025 -> MakerLink is a DIY-focused social Android-compatible that lets users create, share, discover, and collaborate on hands-on projects while connecting with others through community and location-based features.
4) bike-bolt (Java) -> April 2025 -> Bike-Bolt is an Android application designed to monitor and control a smart bike by tracking lighting, locking, and environmental states through dedicated interfaces.

#### Five-line summaries 🧠🌐

1) sensor-gateway
- Developed in CLion, VM: Ubuntu 24.04 LTS. The sensor gateway (server) handles concurrent data sent by multiple sensor nodes (clients) in real-time through a TCP connection. It stores the readings in a
  synchronized shared buffer, implemented as a linked-list. Real-time data aggregation is done using POSIX threads.
  Data is retrieved by the shared buffer from separate threads, and added to a csv file. All actions and readings are tracked by a logger process, which receives continuous updates through a pipeline.
  It includes graceful shutdown of processes, synchronization using mutexes, robust error handling, and thorough testing under several working conditions. No memory leakages, as per Valgrind.

2) jitter-analysis-and-UI
- Developed on VS Code, this project evaluates timing jitter as the error between a reference and measured slave’s response to a SYNC0 signal, with an expected bound of ±100 ns. An oscilloscope samples the SYNC0
  pin of each slave at 1 ns resolution and exports the results as CSV files containing sample indices, slave states, and timestamps. The software parses a folder of these CSV files, computes jitter metrics, and
  displays rising-edge visualizations alongside quantitative results. It focuses strictly on data extraction and analysis from CSV inputs, not on hardware operation or jitter mitigation strategies. Programming
  features and tools used: PyQt6 for the UI, Object-oriented programming, multi-threading, and extensive use of numpy and matplot libraries.

3) maker-link
- MakerLink is built on Android Studio and provides a framework for user-generated DIY content spanning multiple domains. The application relies heavily on RecyclerViews for efficient
  rendering of dynamic content feeds such as posts, playlists, communities, and leaderboards. Multi-threading is implemented to handle network operations and data processing of user interactions. User input is stored in external databases, with front and back-end communication enabled by JSON-based data exchange via a web API provided by KU Leuven. Additional integrations include Firebase
  for messaging and notifications, as well as Google Maps APIs to support location-based tool discovery.
  
4) bike-bolt
- Bike-Bolt was developed in Android Studio as a companion app for a smart bike system built around a custom PCB and sensor setup. The hardware integrates an LDR for light detection, an RFID sensor for lock
  control, and a rain sensor, all connected to a Raspberry Pi. Sensor data is read by Python scripts running on the Raspberry Pi and communicated to a PC, which serves as the bridge to the mobile
  application via back-end services (similar to MakerLink). The app provides dedicated activities to display the bike’s state, including light status, lock state (unlockable via RFID tag or directly from the phone), and weather conditions. Additional features include timestamped notifications and real-time status tracking.

<!--
**martinpedata/martinpedata** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
