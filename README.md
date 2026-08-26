# 🚘 Smart Parking Management System — Frontend Web App

<p align="center">
  <img src="https://img.shields.io/badge/React-18%2F19-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React" />
  <img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white" alt="Vite" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS" />
  <img src="https://img.shields.io/badge/Three.js-3D_Twin-000000?style=for-the-badge&logo=threedotjs&logoColor=white" alt="Three.js" />
  <img src="https://img.shields.io/badge/WebSocket-STOMP-010101?style=for-the-badge&logo=socketdotio&logoColor=white" alt="WebSocket" />
</p>

---

## 📌 Project Overview
**Smart Parking Management System Frontend** is a modern, responsive Single Page Application (SPA) designed to serve multiple actors in a smart parking building: **Drivers, Staff, Managers, Security Officers, and System Administrators**.

* **Course / Project**: SWP391 — FPT University HCM
* **UI/UX Philosophy**: High-contrast, dashboard-oriented design, real-time live updates without page reloads, and visual 3D/2D digital-twin parking maps.

---

## 🛠️ Tech Stack

- **Framework**: React (Hooks, Context API, Modular Components)
- **Bundler & Tooling**: Vite, ESLint
- **Styling**: Tailwind CSS, Lucide React Icons
- **Real-Time Client**: StompJS / SockJS over WebSocket
- **3D Visualization**: Three.js / Canvas for 3D parking slot simulation
- **HTTP Client**: Axios with centralized interceptors for JWT token handling & error toasts
- **Charts & Data Viz**: Chart.js / Recharts / D3.js

---

## 🌟 Key Portals & Features

### 1. 🚗 Driver Portal
- **Real-time Availability Map**: Visual representation of free/occupied spots across building floors.
- **Reservation & Booking**: Select zone, reserve parking slot, and receive instant QR access ticket.
- **Subscription Management**: Register monthly/quarterly parking passes with integrated VNPay checkout.

### 2. 🛂 Staff Check-In / Check-Out Station
- Rapid vehicle entry processing: Manual plate input, QR Code scanning, or camera capture.
- Intelligent lane & zone recommendation.
- Live checkout fee calculation with cash or VNPay QR confirmation.

### 3. 📊 Manager Analytics & Dashboard
- Visual revenue trends, peak-hour distributions, and turnover rates.
- Deep Excel Export functionality for financial and operational reporting.
- 3D Digital Twin simulation for overall parking occupancy.

### 4. 🛡️ Security Station & Exception Center
- Real-time Blacklist alert popup when suspicious license plates enter.
- Incident logging (Lost ticket, vehicle damage) with proof photo upload.
- Emergency SOS button with instant barrier release sync across all gates.

### 5. ⚙️ Admin Control Panel
- Building infrastructure hierarchy management: Building $\rightarrow$ Floor $\rightarrow$ Zone $\rightarrow$ Gate.
- Dynamic pricing rules configuration (grace periods, holiday multipliers, vehicle type formulas).

---

## 👨‍💻 My Role & Key Contributions (Khắc Toàn)

* **Role**: Fullstack / Frontend Contributor
* **Key Implementations**:
  - **Manager Dashboard & Analytics**: Implemented statistical charts, revenue overview, and real-time transaction tables.
  - **VNPay Payment Flow**: Built payment return redirect handlers, status polling, and payment confirmation screens.
  - **Staff & Security Interaction**: Contributed to staff check-in/out layouts, draggable exception report modals, and license plate auto-format validators.
  - **Project Documentation**: Authored and maintained quick demo test sheets and API integration guides (`docs/tai_lieu_demo.md`).

---

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- npm / yarn / pnpm

### Running Locally

1. **Clone repository**:
   ```bash
   git clone https://github.com/KhacToanNguyen-23/parking-management-frontend.git
   cd parking-management-frontend
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Configure Environment**:
   Create a `.env` file in the root directory:
   ```env
   VITE_API_BASE_URL=http://localhost:8080/api
   VITE_WS_URL=http://localhost:8080/ws
   ```

4. **Start Development Server**:
   ```bash
   npm run dev
   ```
   Open `http://localhost:5173` in your browser.

---

## 📄 License
This project is developed for educational and portfolio demonstration purposes.
