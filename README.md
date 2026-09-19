# 🌾 HexaFarm — KISAN PRAVAH

**Improving the Farmer Procurement Experience**

 **Anticipate · Orchestrate · Assure**

**KISAN PRAVAH** is an AI-enabled, multilingual procurement coordination platform that connects farmers and procurement centres — from crop planning all the way to payment.

Instead of reacting to farmers after they arrive at a centre, KISAN PRAVAH **forecasts demand before congestion occurs**. Farmers pre-register their crops, centres see expected arrivals and quantities in advance, and everyone gets clear, real-time visibility of queues, slots and payments.

| **Event** | Smart India Hackathon 2026 |
| **Problem Statement ID** | SIH26032 |
| **Theme** | Smart Automation |
| **PS Category** | Software |
| **Team Name** | HexaFarm |
| **Team ID** | 135883 |

## 🚜 Problem

Farmers often face long waiting times, a lack of information about procurement schedules, and uncertainty about procurement status. On the ground, this shows up as:

- No advance visibility of demand, so centres cannot plan capacity, staff, storage or weighing facilities
- Poor communication between farmers and procurement centres
- Long queues and unnecessary, repeated travel to centres
- Uncertainty about where, when and at what rate to sell
- Little transparency in procurement progress and payment status
- Difficulty for low-literacy and non-smartphone users in accessing information

---

## 💡 Our Solution

KISAN PRAVAH gives farmers, procurement centres and government authorities one shared platform that supports **informed selling** and **planned procurement**.

**For farmers**

- 🌱 Pre-register crops (crop + quantity + expected date) before harvest
- 📝 Digital registration and document verification
- 📍 Crop-based procurement-centre recommendation
- 🕐 Real-time queue and waiting-time estimation
- 🎟️ Slot / token booking with a QR code
- 🔔 SMS / app alerts and reminders
- 📋 Quality guidelines for crops
- 🧾 Receipts and procurement-to-payment tracking
- 📊 MSP, demand and weather insights to decide *where* and *when* to sell
- 🗣️ Voice-enabled multilingual interface and SMS-based services for low-literacy and non-smartphone users

**For procurement centres**

- Dashboards for demand forecasting and capacity planning
- Advance view of expected crops, quantities and arrival periods
- Slot, queue and workload management
- Better planning of staff, storage and weighing facilities

**For government authorities**

- Real-time, district-level visibility into demand, congestion, centre utilisation, procurement progress and payments

---

## 🔄 How It Works — Process Flow

```
+----------------------------+
|          DECLARE           |
|      Crop + Quantity       |
+----------------------------+
               |
               v
+----------------------------+
|          PREDICT           |
|        AI Forecast         |
+----------------------------+
               |
               v
+----------------------------+
|          ALLOCATE          |
|       Centre + Slot        |
+----------------------------+
               |
               v
+----------------------------+
|           ARRIVE           |
|        Farmer Alert        |
+----------------------------+
               |
               v
+----------------------------+
|          PROCURE           |
|     Planned Processing     |
+----------------------------+
               |
               v
+----------------------------+
|           TRACK            |
|     Transaction Status     |
+----------------------------+
```

1. **Declare** – The farmer registers (OTP verification) and declares crop and quantity ahead of time.
2. **Predict** – The AI engine forecasts arrivals, quantities, congestion and workload for each centre.
3. **Allocate** – The decision engine recommends a suitable centre and an available slot.
4. **Arrive** – The farmer gets an alert and arrives at the booked time, avoiding long waiting.
5. **Procure** – The centre processes the produce in a planned, orderly way.
6. **Track** – The farmer follows the transaction from bill submission to payment.

---

## ✨ Key Features

### 👨‍🌾 Farmer Portal
- OTP-based registration and login, farmer profile
- Crop pre-registration (crop, quantity, expected date)
- Document upload and verification
- Nearby centre discovery with distance, queue size and predicted waiting time
- AI chatbot / assistant to help choose a centre
- Slot booking with QR code confirmation
- Notifications for documents, schemes, training videos, alerts and reminders
- Procurement and payment status tracking

### 🏢 Procurement Centre Portal
- Centre registration and profile
- Approval of farmer applications
- Demand forecast and capacity planning dashboard
- Slot, queue and resource management
- Farmer feedback loop for continuous service improvement

### 🛡️ Admin / Government Portal
- Real-time monitoring of demand, congestion and centre utilisation
- Procurement progress and payment visibility
- Data management and district-level analytics

### 🧠 AI & Decision Engine
- Forecasts expected arrival timing, crop quantity, centre workload distribution, congestion risk and capacity/resource requirements
- Converts predictions into actions: centre recommendation, slot allocation, resource planning and farmer notifications
- Starts with verified historical data and rule-based estimates, then improves by comparing forecasts with actual arrivals

### 🌐 Accessibility & Inclusion
- Multilingual voice assistance and SMS-based services
- Progressive Web App with offline support that syncs automatically when connectivity returns
- Centre-assisted registration for farmers with limited digital access

---

## 🏗️ System Architecture

+----------------------------------------------------------------+
|                          DATA INPUTS                           |
|                                                                |
|      Farmer Declarations  |  Historical Procurement Data       |
|        Seasonality & Crop Calendar  |  Centre Capacity         |
+----------------------------------------------------------------+
                                |
                                v
+----------------------------------------------------------------+
|  AI / ML PREDICTION ENGINE (Python, Scikit-learn, Vertex AI)   |
|                                                                |
|       Expected arrival timing  |  Expected crop quantity       |
|        Centre workload distribution  |  Congestion risk        |
|                Capacity & resource requirement                 |
+----------------------------------------------------------------+
                                |
                                v
+----------------------------------------------------------------+
|                        DECISION ENGINE                         |
|                                                                |
|           Centre Recommendation  |  Slot Allocation            |
|           Resource Planning  |  Farmer Notification            |
+----------------------------------------------------------------+
                                |
                                v
+----------------------------------------------------------------+
|         USER LAYER (Role-based portals - Angular PWA)          |
|                                                                |
|  Farmer Portal  |  Procurement Centre Portal  |  Admin Portal  |
|   External Users (Govt systems, Partners, Service providers)   |
+----------------------------------------------------------------+
                                ^
                                |   REST APIs / WebSockets
                                v
+----------------------------------------------------------------+
|      BACKEND SERVICES (Node.js + Express.js + Socket.IO)       |
|                                                                |
|       Authentication & Authorization  |  Business Logic        |
|         Real-time Queues  |  External API Integration          |
|   Notifications & Communication  |  File & Media Management    |
+----------------------------------------------------------------+
                ^                                 ^
                |                                 |
                v                                 v
+------------------------------+  +------------------------------+
|           DATABASE           |  |    EXTERNAL INTEGRATIONS     |
|      MongoDB + Mongoose      |  |                              |
|         Redis Cache          |  |          OpenAI API          |
|                              |  |    WhatsApp Business API     |
|        Users & Roles         |  |         SMS Gateway          |
|       Application Data       |  |   Firebase Cloud Messaging   |
|         Transactions         |  |      Weather & MSP APIs      |
|       Logs & Analytics       |  |      Google Maps / GPS       |
+------------------------------+  |       Government APIs        |
                                  +------------------------------+


---

## 🧠 Technology Stack

| Layer                     | Technologies |
| **Frontend**              | Angular, TypeScript, Tailwind CSS, Progressive Web App (PWA) |
| **Backend**               | Node.js, Express.js, REST APIs, Socket.IO |
| **Database**              | MongoDB, Mongoose, Redis Cache |
| **AI & Prediction**       | Python, Scikit-learn, OpenAI API (multilingual assistance), demand forecasting and waiting-time prediction |
| **Integrations**          | Weather and MSP APIs, Google Maps / GPS, SMS Gateway, WhatsApp API |
| **Google Cloud Platform** | Cloud Run, Cloud Storage, Vertex AI, Firebase Cloud Messaging, Cloud Monitoring |
| **Security**              | OTP Authentication, Role-Based Access Control, HTTPS/TLS, Data Encryption |
| **Development**           | Docker, Git, GitHub, CI/CD |

- The technology stack may be refined as development progresses.

## 🛠️ Methodology

HexaFarm follows a **farmer-first, agile and data-driven approach**.

**Analyze → Prototype → Develop → Integrate → Pilot Test → Deploy on GCP → Improve**

Development begins with requirement analysis and rapid prototyping, followed by building multilingual registration, AI prediction, centre recommendation, slot booking and payment-tracking modules. Weather, MSP, maps and SMS are then integrated. After pilot testing with farmers and procurement centres, the platform is securely deployed on Google Cloud Platform and continuously improved using operational data and stakeholder feedback.

---

## ✅ Feasibility & Challenges

| Area            | Approach |
| **Technical**   | Proven, scalable technologies — AI, GCP, GPS, SMS and secure authentication |
| **Operational** | Phased, centre-wise rollout that fits into existing procurement processes without disrupting operations |
| **Adoption**    | Simple interface with multilingual voice, SMS and centre-assisted registration |
| **Scalability** | Modular, cloud-native architecture that can grow from pilot centres to district, state and national networks |
| **Economic**    | Cloud-based deployment, reusable modules and digital communication reduce infrastructure cost and manual workload |

**Key challenges and mitigation**

- **Adoption and digital literacy** – multilingual voice assistance, SMS, local demonstrations, centre-assisted registration, and offline-capable PWA
- **Disruption to existing processes** – phased workflow integration with pilot testing and staff training
- **Dependency on government systems** – standard APIs and configurable adapters, starting with mock/sandbox environments before authorised live integration
- **Payments** – secure, auditable connections with approved government payment systems, without storing sensitive banking information
- **Privacy and security** – consent-based data collection, encryption, OTP authentication, role-based access and audit logs
- **Prediction accuracy** – start with verified historical data and rule-based estimates, then keep improving by comparing forecasts with actual arrivals

---

## 🔍 Research

**Primary research – field visit**
District Marketing Office, Shahu Market Yard, Kolhapur. The team interacted with officials and observed the existing procurement workflow — farmer registration, crop arrival, weighing, storage and payment. The visit highlighted gaps in advance demand visibility, farmer communication,
