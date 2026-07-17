# SPACEAPP v5.6.x

*Real-time satellite tracking, mission intelligence, orbital analysis, and spacecraft visualization.*

---

# Overview

SPACEAPP is a desktop application designed for satellite tracking, mission exploration, and space education. It combines live orbital data, advanced search capabilities, AI-assisted mission intelligence, and interactive spacecraft visualization into a unified platform.

Whether you're monitoring Starlink satellites, researching scientific missions, exploring orbital mechanics, or tracking the International Space Station, SPACEAPP provides a streamlined environment for understanding humanity's activity in space.

---

# Capabilities

## 🛰️ Real-Time Tracking & Prediction

Monitor satellites and spacecraft using live orbital data and project their paths.

* **Live Position Tracking:** Multi-satellite monitoring with real-time speed and altitude calculations.
* **Satellite Path Prediction:** Visualize future orbital trajectories, predicted satellite positions, historical positions, and ground-track paths.
* **Raw TLE Viewing:** Inspect raw Two-Line Element (TLE) data used for orbital calculations and tracking (available for supported satellites).

---

## 🎮 Interactive 3D Spacecraft Models *(Updated in v5.6.2)*

Inspect spacecraft structures and physical appearances directly alongside mission information and tracking data.

* **Supported Models:**
* Starlink
* GPS Satellites
* Weather Satellites
* Science Satellites
* International Space Station (ISS)
* Tiangong Space Station
* James Webb Space Telescope
* Hubble Space Telescope
* **CubeSat** *(New)*
* **SpaceX Dragon** *(New)*


* **Immersive 3D Canvas:** Upgraded the 3D viewport background from a basic gray-black to an aesthetic, high-fidelity gradient blue & neon purple environment.
* **Smart Camera Transition:** Reset View and initial model loads now trigger an automated smooth zoom-in effect, keeping the target spacecraft beautifully framed and detailed instead of rendering at a far distance.

---

## 🧠 AI Mission Intelligence & RAG Profiles *(Updated in v5.6.2)*

Transform raw technical telemetry into comprehensive, context-rich educational insights.

* **RAG + Web Search Profiles:** Mission profiles are powered by Retrieval-Augmented Generation (RAG) and web-backed research systems to provide:
* Launch date, Operator, and Country
* Detailed mission description and current operational status
* Days in space and estimated completed orbits


* **Educational Insights:** AI-assisted overviews helping users understand:
* Mission objectives & scientific contributions
* Historical significance & technology highlights
* Operational purpose


* **Edge Function Multi-Key Rotation & Model Fallbacks:** Under-the-hood upgrades to the Edge network support dynamic API key rotation and multi-model fallback chains, drastically reducing the occurrence of service interruptions (503 failures) due to single-endpoint or key-quota limits.
* **Resilient Cache Fallback:** If Edge function retrievals fail, the application gracefully catches the error and pulls from your expired local cache to compile pre-structured strings for the AI overview, completely averting 503 application lockups.

---

## 🌍 Advanced Orbital & Coverage Analysis *(New in v5.6)*

Perform detailed mathematical and geometric assessments of spacecraft paths.

* **Orbital Geometry Analysis:** Explore orbit classification, orbital inclination, altitude range, orbital period, ground-track behavior, and mission-specific orbital characteristics.
* **Coverage Radius Analysis:** Visualize the estimated area a spacecraft can observe, serve, or communicate with from its current orbit. Calculated using orbital altitude and geometric analysis to provide:
* Coverage radius
* Ground footprint size
* Orbital visibility range
* Coverage characteristics


* **Lifespan Analysis:** View operational history and mission longevity information (time spent in orbit, original mission duration, mission extensions, current operational phase, and estimated service lifespan).

---

## 🔬 Research View *(New in v5.6)*

A new, information-rich workspace layout designed specifically for deeper spacecraft exploration. Research View consolidates and grants expanded access to:

* Interactive 3D Models
* Detailed Mission Profiles & Intelligence
* Orbital & Coverage Analysis
* Lifespan and Capability assessments

---

## 🔎 Advanced Search System & Databases

Find satellites quickly using multiple pre-indexed search methods.

* **Supabase Search Infrastructure:** Satellite data is pre-indexed and synchronized through Supabase for faster searches, alias support, background synchronization, and support for larger databases.
* **Search Methods:**
* Name-based search & Alias-aware searching
* Category browsing (Curated collections: Special, Starlink, Science, Weather, GPS, etc.)
* NORAD ID lookup (useful for research and tracking specific spacecraft outside curated lists)
* Global visibility searches



### Advanced Sky Search (`near:`)

Search for satellites visible from virtually anywhere on Earth using specific parameters.

**Example Query:**

```text
near: Tokyo, Japan; radius: 45

```

**Supported Parameters:**

```text
near: <place or coordinates>;
alt: <altitude>;
radius: <0-90>;
catid: <satellite category ID>;

```

*Note: If optional parameters are omitted, SPACEAPP uses your current values.*

---

## ⚡ Smart API Optimization

SPACEAPP automatically reduces API usage while maintaining a smooth tracking experience.

* **System Benefits:** Reduced API consumption, longer monitoring sessions, lower network usage, and improved overall application efficiency.
* **Performance:** Depending on usage patterns, API consumption is reduced by approximately **25% or more**.

---

## 🎨 UI Enhancements *(Updated in v5.6.2)*

A refreshed workspace experience with intuitive window management.

* **Balanced Default Layout:** The default layout split ratio for the main workspace (**Map | 3D View**) is now set to an optimized **60/40 ratio** (up from 70/30). This provides immediate visual comfort and more breathing room for interactive 3D model tracking out of the box.
* **Dynamic Splitters:** Fully customizable workspace layouts using `QSplitter` allow users to adjust and resize both panel spaces freely on the fly.
* **Visual Hierarchy:** Clean and cohesive information layouts, improved organization, expanded dynamic iconography, and better information presentation throughout the application.

---

## ⚙️ System Utilities: Updates & Communication

The application features a built-in communication system that keeps you connected with the latest development cycles.

* **Check Info System:** Connects to the official GitHub update server to display release notifications, surveys, community announcements, and important developer messages.
* **Auto-Notification:** Alerts you when a database update is recommended to preserve tracking accuracy, search reliability, and the latest satellite metadata.

---

## 🖥️ System Utilities: Cross-Platform Deployment *(New in v5.6)*

SPACEAPP is built to run natively across major desktop environments with dedicated, clean installation files.

* **Windows x64 Installer (Inno Setup):** A robust Windows installer built using Inno Setup that handles custom installation paths, registers the app securely, and ensures clean upgrades and complete uninstallation without leaving orphaned registry entries or directories.
* **macOS ZIP Build:** A fully compiled, native macOS zip package optimized for simple drag-and-drop deployment to the Applications folder, bringing smooth orbital tracking to Apple ecosystems.

---

# Setup

## Step 1 - Obtain an API Key

Create an account with N2YO and obtain an API key (License Key) [here](https://www.n2yo.com/login/edit/).

## Step 2 - Initial Setup

1. Launch SPACEAPP
2. Enter your API key when prompted
3. Complete account creation and application setup
*The setup wizard automatically appears during the first launch.*

## Step 3 - Login

1. Enter your created username during setup
2. Enter your created password during setup
3. Begin exploring
*Your API key only needs to be entered once.*

## Step 4 - Create Account
1. Launch SPACEAPP/Click Logout Icon if you're still inside the tracking window
2. Select **Signup**
3. Start entering your new Username, Password, and API Key
4. Complete your account creation
*This will create a different account on the application.*

---

# Quick Start

### Tracking a Satellite

1. Launch SPACEAPP
2. Select a category
3. Choose a satellite
4. View real-time tracking information

### Searching by NORAD ID

1. Enter a NORAD ID
2. Press **Search**
3. Review available tracking information

### Exploring Research Features

1. Open a supported spacecraft
2. Switch to **Research View**
3. Explore mission and orbital information

---

# Satellite Database

Satellite information changes over time as missions launch, evolve, and conclude.

### Supabase Database

Cloud-hosted and automatically maintained.

* Pre-indexed searches
* Alias support
* Synchronization
* Search optimization

### Local Database

Stored on your device for fast local access. SPACEAPP may occasionally recommend updates to maintain tracking accuracy, search accuracy, satellite metadata, and operational status information.

> [!NOTE]
> Database updates are recommended for the best experience.

> [!IMPORTANT]
> During setup or database updates, avoid closing the application or interrupting the process. Unexpected interruptions may corrupt local data and require recovery or reinstallation.

---

# Location Notice

SPACEAPP estimates your location using your public IP address.

* VPN usage may reduce location accuracy.
* Location data remains cached until the application closes.
* Switching accounts does not refresh location information.

**If your location changes significantly:**

1. Close SPACEAPP
2. Reopen the application

---

# Available Information Reference

Depending on availability, SPACEAPP displays the following data fields:

* Satellite Name & NORAD ID
* Live Position, Speed, and Altitude
* Ground Track & Orbital Path (TLE Data)
* Launch Date, Operator, and Country of Origin
* Mission Description & Operational Status
* Days in Space & Estimated Orbits Completed
* Mission Capabilities & Lifespan Information
* Orbital Geometry Analysis
* Mission Intelligence Summary
* Interactive 3D Models

---

# API Modes

SPACEAPP includes smart API-saving technology that automatically reduces calls for non-Starlink satellites.

| Satellite Type    | Mode          | Base Interval | Effective Update Rate              |
| ----------------- | ------------- | ------------- | ---------------------------------- |
| Starlink Only     | Efficient     | 8 s           | Every 8 s                          |
| Starlink Only     | Non-Efficient | 3 s           | Every 3 s                          |
| Non-Starlink Only | Efficient     | 8 s           | Every 16 s                         |
| Non-Starlink Only | Non-Efficient | 3 s           | Every 6 s                          |
| Mixed (Equal)     | Efficient     | 8 s           | Starlink: 8 s / Non-Starlink: 16 s |
| Mixed (Equal)     | Non-Efficient | 3 s           | Starlink: 3 s / Non-Starlink: 6 s  |

### Recommendations

**Efficient Mode**

Recommended for:

* Daily use
* Long monitoring sessions
* Reduced API consumption

**Non-Efficient Mode**

Recommended for:

* Faster refresh rates
* Short-term monitoring
* Situations where API usage is less important

---

# Privacy

SPACEAPP uses publicly available satellite and mission data sources.

No personal information is collected beyond what is required for normal application operation.

Location estimates are used solely to support tracking and visibility calculations.

---

# Support

**Email:** [tanbinhvo.hcm@gmail.com](mailto:tanbinhvo.hcm@gmail.com)

Questions, bug reports, feedback, and feature suggestions are welcome.

---

# Credits

**Vo Tan Binh (Henry Vo)**

Creator and Lead Developer of SPACEAPP.

---

# Copyright & License

© Vo Tan Binh. All rights reserved.

This software and its associated assets, models, artwork, databases, and source code are protected by copyright.

Redistribution or reuse without explicit permission from the author is prohibited.
