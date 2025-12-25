# GUARDIA  
**Geo-fenced Unified Alert & Response for Dynamic Incident Assistance**

A smart tourism safety ecosystem designed to make travel in North-Eastern region of India **safe, structured, and stress-free**.

---

## Overview

Tourism in the North-East offers immense natural and cultural value, but tourists often face three critical challenges:
- Unstructured trip planning
- Delayed or unreliable emergency response
- Poor network connectivity in remote and hilly areas

**GUARDIA** addresses these challenges through an integrated system that combines a mobile application, an authority monitoring backend, AI-driven safety scoring, and an offline-capable mesh network.  
Assam is used as the pilot region for demonstration and implementation.

This project was developed as part of **Smart India Hackathon (SIH)**, aligned with problem statements from the **Ministry of Development of North Eastern Region (DoNER)**.

---

## Key Features

### Tourist Mobile Application
- Trip itinerary planning with destination selection and guidelines
- KYC-based digital identity using Aadhaar / passport / valid ID
- Unique QR code for seamless checkpoint verification
- Real-time maps, safety alerts, and location-based updates
- Multilingual support for domestic and international tourists

### Three-View System
- **User View** – itinerary, safety score, alerts, navigation
- **Friends / Family View** – live location tracking and SOS notifications
- **Authority View** – QR verification, tourist monitoring, SOS handling

### Emergency Handling
- **Heavy Emergency (SOS):**
  - Direct geo-tagged alerts to authorities
  - Simultaneous notification to trusted contacts
- **Light Emergency:**
  - Navigation assistance
  - Area danger alerts and local news
  - Context-aware safety guidance

### AI-Based Safety Scoring
- Predictive safety score for locations
- Based on GPS activity density, historical data, and reviews
- Helps tourists make informed travel decisions

### Low Connectivity Support
- Hardware-assisted mesh / peer-to-peer network
- Offline SOS triggering and relay
- Cached itineraries and offline maps
- Designed for remote, low-signal regions

---

## System Architecture >

+----------------------------+
|        Tourist App         |
|   (React Native – iOS/Android)
|                            |
|  - Login / Signup          |
|  - KYC Verification        |
|  - QR Code Identity        |
|  - Trip Planning           |
|  - SOS Button              |
|  - Maps & Safety Alerts    |
|  - Multilingual UI         |
+-------------+--------------+
              |
              | HTTPS / REST APIs
              v
+----------------------------+
|        Backend Server      |
|        (Node.js)           |
|                            |
|  - Auth & KYC Validation   |
|  - QR Code Generation      |
|  - Trip & Destination Data |
|  - Emergency Routing       |
|  - Safety Score Engine     |
|                            |
|  Data Sources:             |
|  - destinations.csv       |
|  - reviews.csv            |
+------+------+--------------+
       |      |
       |      |
       |      v
       |  +------------------------+
       |  |   AI / Safety Engine   |
       |  |                        |
       |  | - GPS-based Analysis   |
       |  | - Incident Density     |
       |  | - Risk Scoring Model   |
       |  +------------------------+
       |
       v
+----------------------------+
|     Authority Dashboard    |
|                            |
|  - QR Scan & Verification  |
|  - SOS Monitoring          |
|  - Tourist Density View    |
|  - Incident Management     |
+-------------+--------------+
              |
              |
              v
+----------------------------+
|    Emergency Response      |
|  (Police / Medical / Admin)|
+----------------------------+


+--------------------------------------------------------+
|            Low Connectivity / Mesh Network              |
|                                                        |
|  Tourist Devices (Peer-to-Peer / LoRa / Mesh)          |
|                                                        |
|  - Offline SOS Trigger                                 |
|  - Cached Itinerary Access                             |
|  - Offline Maps                                       |
|                                                        |
|  SOS hops across nearby devices until connectivity     |
|  is restored or authority node is reached              |
+--------------------------------------------------------+


---

## Repository Structure

This project is organized as a multi-repo system:

- **Mobile Application Repository:**  
  [https://github.com/TrueCoderSja/SafeLink-client]

- **Backend & API Repository:**  
  [https://github.com/777mudit/SafeLink-backend]

- **AI / Safety Scoring Module Repository:**  
  [https://github.com/VS2412/Enpitsu]

---

## Scope & Notes

- The system is designed to be scalable across all North-Eastern states
- Focus is on real-world constraints such as connectivity, safety, and authority coordination

---

## Why This Project Matters

GUARDIA is not just a travel app.  
It is a **safety-first tourism infrastructure** that builds trust between tourists, families, and authorities while enabling faster emergency response and better planning in underserved regions.

---

## Team

Built by the team as part of Smart India Hackathon (SIH), with a focus on real-world applicability, system design, and scalability.



## License
This project is licensed under the MIT License.
