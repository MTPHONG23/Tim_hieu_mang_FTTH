# FTTH Network Operation, Monitoring & Troubleshooting at FPT Telecom

> Graduation Internship Report (Báo cáo thực tập tốt nghiệp) at FPT Telecom (INF-MN), conducted by Mạch Thế Phong & Nguyễn Anh Tuấn[cite: 6].

## 📋 Overview
This project documents the comprehensive study, architecture analysis, operational workflows, and troubleshooting procedures of the **Fiber to the Home (FTTH) / GPON** infrastructure at FPT Telecom (Southern Infrastructure Development and Management Center)[cite: 6]. It covers end-to-end signal transmission models, centralized network monitoring systems, and optical fiber testing methodologies using advanced OTDR equipment[cite: 6].

---

## 🏗️ System Architecture & Network Topology
* **Network Structure:** Implemented using both **Active Optical Networks (AON)** and **Passive Optical Networks (PON / GPON)**[cite: 6].
* **GPON Splitter Hierarchy:** Utilizes a two-tier passive optical splitter architecture (Level 1: 1:8 splitter, Level 2: 1:16 splitter) allowing a single PON port to serve up to 128 subscribers[cite: 6].
* **Core Infrastructure Components:**
  * **Central Office / POP:** Houses access switches, OLTs, and BRAS servers[cite: 6].
  * **OLT (Optical Line Terminal):** Equipment such as GCOM (GL5610-16P) and Huawei MA5800-X2 managing downstream/upstream traffic[cite: 6].
  * **ODF & FDH:** Optical distribution frames and hubs for managing and protecting fiber splices[cite: 6].
  * **FAT (Fiber Access Terminal):** Access points distributing distribution fibers to last-mile drop cables[cite: 6].
  * **ONT (Optical Network Terminal):** Customer-premises equipment (e.g., AX3000HI, HBG1000R) converting optical signals to Ethernet/Wi-Fi[cite: 6].

---

## 🛠️ Key Technical Workflows

### 1. Provisioning & Access Control (Khai thác & Vận hành)
* **Optical Path Setup:** Deploying feeder, distribution, and drop fibers while maintaining strict attenuation thresholds[cite: 6].
* **Subscriber Provisioning:** Mapping PPPoE usernames, VLAN tagging, and service profiles (Internet, IPTV, VoIP) into OSS/BSS systems[cite: 6].
* **Authentication Mechanisms:** Implementing **PPPoE** and **PPPoE+** (adding physical line data like PON port and OLT info) for precise subscriber identification and faster fault isolation[cite: 6].

### 2. Network Monitoring & State Management
* **NMS Integration:** Utilizing centralized Network Management Systems to monitor ONT states, optical power, and CRC error rates in real-time[cite: 6].
* **ONT Lifecycle States:** Tracking the 7 GPON operational states (O1 Initial, O2 Standby, O3 Serial Number, O4 Ranging, O5 Operation, O6 PopUp, O7 Emergency Stop)[cite: 6].
* **Performance Metrics:** Monitoring Optical Receive/Transmit power ($\text{Rx}/\text{Tx}$), CRC error increments, and PPPoE session stability[cite: 6].

### 3. Troubleshooting & Incident Response (Xử lý sự cố)
* Diagnosing and resolving common fiber network anomalies, including:
  * **LOS (Loss of Signal):** Identifying fiber breaks or severe attenuation[cite: 6].
  * **PON Port Hangs:** Re-initializing PON chips or migrating users to alternative ports[cite: 6].
  * **Rouge ONT:** Isolating faulty customer devices that continuously flood upstream optical signals and disrupt shared PON ports[cite: 6].
  * **IPTV / Multicast Issues:** Checking VLAN streams and upstream traffic distribution[cite: 6].

### 4. Optical Testing & Validation (OTDR & Power Meter)
* **Power Meter Testing (OPM):** Measuring absolute optical signal levels ($\text{dBm}$) at 1310 nm and 1550 nm wavelengths using Viavi USB MP-60 modules[cite: 6].
* **OTDR Testing (SmartOTDR 100AS/A/B - Viavi):** 
  * Analyzing fiber links across multiple wavelengths (1310 nm, 1550 nm, and 1625 nm monitoring wavelength)[cite: 6].
  * Evaluating total link loss, average attenuation ($\text{dB/Km}$), Optical Return Loss (ORL), and event reflections[cite: 6].

---

## 👥 Authors
* **Mạch Thế Phong** – N21DCVT072 (Student at PTIT)[cite: 6]
* **Nguyễn Anh Tuấn** – N21DCVT115 (Student at PTIT)[cite: 6]
* **Corporate Supervisor:** Nguyễn Hoàng Phương (FPT Telecom - INF-MN)[cite: 6]
* **Academic Instructor:** ThS. Nguyễn Văn Hiền[cite: 6]
