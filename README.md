# 🌱 ShareBite — Surplus Food Sharing Platform & Alert Extension

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform: Web](https://img.shields.io/badge/Platform-Web%20SPA-orange.svg)](index.html)
[![Extension: Manifest V3](https://img.shields.io/badge/Chrome%20Extension-Manifest%20V3-blue.svg)](extension/manifest.json)
[![Tailwind CSS](https://img.shields.io/badge/TailwindCSS-v3.4-38B2AC.svg)](https://tailwindcss.com/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

> **"Good food deserves a good home."**  
> ShareBite is a real-time community food rescue platform connecting neighborhood bakeries, restaurants, and grocery stores directly with local shelters and soup kitchens to eliminate edible food waste.

---

## 🌟 Overview

Every day, hundreds of tons of fresh, high-quality surplus meals are discarded due to tight operational windows. **ShareBite** bridges this gap with a lightweight, responsive web application and an integrated desktop browser extension:

1. **Donors (Bakeries, Delis, Caterers):** Post surplus food batches in under 60 seconds with photos, quantities, allergen notes, and pickup deadlines.
2. **Receivers (Shelters, Community Kitchens):** Instantly browse nearby surplus, filter urgent expiring items, and claim with 1-click.
3. **Volunteers & Drivers:** Coordinate handoffs with a secure 4-digit pickup code and track live order progress from pickup to delivery.
4. **Community Watch:** View real-time aggregate environmental and social metrics (meals served, kg rescued, CO₂ emissions prevented).

---

## ✨ Features

### 🏬 1. Donor Surplus Hub
- **Rapid Posting in 60s:** Input food type, portion sizes, deadlines, and pickup instructions.
- **Convenient Presets:** Instant deadline shortcuts (`Today 5 PM`, `Closing 7:30 PM`, `Tomorrow 9 AM`).
- **Surplus Inventory Management:** Active dashboard tracking available vs. in-transit pickups.

### 🥗 2. Receiver & Shelter Portal
- **Category Filtering:** Bakery & Bread, Hot / Prepared Meals, Fresh Produce, Dairy & Chilled, Pantry Staples.
- **Urgent Pickup Filter:** One-tap filter highlighting food needing rescue within 2 hours.
- **Instant Search:** Search across food names, donor business names, and notes.

### 🚚 3. Real-Time Handshake & Delivery Tracker
- **4-Step Status Pipeline:**
  $$\text{Available} \longrightarrow \text{Claimed} \longrightarrow \text{Picked Up} \longrightarrow \text{Delivered}$$
- **Secure 4-Digit Claim Codes:** Ensures safe and verified handoff at donor backdoors.
- **Progress Simulation:** Live reactive stepper showing driver dispatch and delivery confirmations.

### 📊 4. Environmental Impact Analytics
- **Live Metrics Counter:** Real-time calculation of meals provided, kg of food diverted, and metric tons of CO₂ avoided.
- **Weekly Rescue Bar Chart:** Visual trend of community distribution volume across the week.
- **Live Activity Feed:** Feed showing real-time handovers.

### 🔔 5. Companion Chrome Extension (`FoodRescue Alerts`)
- **Manifest V3 Architecture:** Built with high performance and minimal background memory overhead.
- **Desktop Alerts:** Automatic Chrome notifications when urgent food surplus is dropped nearby.
- **Toolbar Quick-Action Popup:** View urgent listings and claim directly without navigating away from your work.

---

## 📁 Repository Structure

```text
sharebite-food-rescue/
├── index.html                  # Core ShareBite Web Application (Single-page app)
├── README.md                   # Project documentation, guides, and setup instructions
├── LICENSE                     # Open-source MIT License
├── .gitignore                  # Git ignore rules for clean repository state
├── extension/                  # Companion Chrome Extension (Manifest V3)
│   ├── manifest.json           # Extension metadata & permission configurations
│   ├── background.js           # Service worker handling alarms and alert notifications
│   ├── popup/
│   │   ├── popup.html          # Toolbar popup user interface
│   │   └── popup.js            # Toolbar interactive claiming logic
│   └── icons/
│       ├── icon-16.png         # 16x16 Toolbar icon
│       ├── icon-48.png         # 48x48 Extension manager icon
│       └── icon-128.png        # 128x128 Chrome Web Store icon
└── publish-to-github.ps1       # Automated script to push directly to GitHub via API
