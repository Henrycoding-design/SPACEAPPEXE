# SPACEAPP v5.6

*Real-time satellite tracking, mission intelligence, orbital analysis, and spacecraft visualization.*

---

# Overview

SPACEAPP is a desktop application designed for satellite tracking, mission exploration, and space education. It combines live orbital data, advanced search capabilities, AI-assisted mission intelligence, and interactive spacecraft visualization into a unified platform.

Whether you're monitoring Starlink satellites, researching scientific missions, exploring orbital mechanics, or tracking the International Space Station, SPACEAPP provides a streamlined environment for understanding humanity's activity in space.

---

# What's New in v5.6

## 🎮 Interactive 3D Spacecraft Models

SPACEAPP now includes integrated 3D spacecraft visualization.

Currently supported:

* Starlink
* GPS Satellites
* Weather Satellites
* Science Satellites
* International Space Station (ISS)
* Tiangong Space Station
* James Webb Space Telescope
* Hubble Space Telescope

Users can inspect spacecraft structure and appearance while viewing mission information and tracking data.

---

## 🧠 Mission Intelligence

Supported spacecraft now include AI-assisted mission overviews.

Mission Intelligence helps users understand:

* Mission objectives
* Scientific contributions
* Historical significance
* Technology highlights
* Operational purpose

Designed to transform technical satellite data into accessible educational content.

---

## 🌍 Orbital Geometry Analysis

Explore orbital characteristics beyond basic tracking information.

Available analysis may include:

* Orbit classification
* Orbital inclination
* Altitude range
* Orbital period
* Ground-track behavior
* Mission-specific orbital characteristics

---

## 📡 Coverage Radius Analysis

Visualize the estimated area a spacecraft can observe, serve, or communicate with from its current orbit.

Available information may include:

- Coverage radius
- Ground footprint size
- Orbital visibility range
- Coverage characteristics

Coverage estimates are calculated using orbital altitude and geometric analysis.

---

## ⏳ Lifespan Analysis

View operational history and mission longevity information.

Supported spacecraft may include:

* Time spent in orbit
* Original mission duration
* Mission extensions
* Current operational phase
* Estimated service lifespan

---

## 📚 RAG + Web Search Mission Profiles

Mission profiles are now powered by Retrieval-Augmented Generation (RAG) and web-backed research systems.

Available information may include:

* Launch date
* Operator
* Country
* Mission description
* Operational status
* Days in space
* Estimated completed orbits

This system helps provide more detailed and up-to-date spacecraft information.

---

## 🔬 Research View

A new information-rich mode designed for deeper spacecraft exploration.

Research View provides expanded access to:

* Mission profiles
* Orbital analysis
* Capability assessments
* Lifespan information
* Mission intelligence

---

## 🎨 UI Enhancements

SPACEAPP v5.6 introduces a refreshed workspace experience.

Improvements include:

* Dynamic splitter layouts
* Resizable panels
* Improved visual organization
* Expanded iconography
* Better information presentation

Users now have greater control over how information is displayed throughout the application.

---

# Core Features

## 🛰️ Real-Time Tracking

Monitor satellites and spacecraft using live orbital data.

Features include:

* Live position tracking
* Multi-satellite monitoring
* Speed information
* Altitude information
* Ground-track visualization

---

## 🛰️ Satellite Path Prediction

Visualize:

* Future orbital trajectories
* Predicted satellite positions
* Historical satellite positions
* Ground-track paths

---

## ⚡ Smart API Optimization

SPACEAPP automatically reduces API usage while maintaining a smooth tracking experience.

Benefits:

* Reduced API consumption
* Longer monitoring sessions
* Improved efficiency
* Lower network usage

Depending on usage patterns, API consumption may be reduced by approximately 25% or more.

---

## 🔎 Advanced Search System

Find satellites quickly using multiple search methods.

Supported methods:

* Name-based search
* Alias-aware searching
* Category browsing
* Global visibility searches
* NORAD ID lookup

### Advanced Sky Search (`near:`)

Search for satellites visible from virtually anywhere on Earth.

Example:

```text
near: Tokyo, Japan; radius: 45
```

Supported parameters:

```text
near: <place or coordinates>;
alt: <altitude>;
radius: <0-90>;
catid: <satellite category ID>;
```

If optional parameters are omitted, SPACEAPP uses your current values.

---

## 🗄️ Supabase Search Infrastructure

Satellite data is pre-indexed and synchronized through Supabase.

Benefits include:

* Faster searches
* Alias support
* Improved reliability
* Background synchronization
* Support for larger databases

---

## 📂 Category Browsing

Explore curated satellite collections including:

* Special
* Starlink
* Science
* Weather
* GPS

Additional categories may be added through future updates.

---

## 🆔 NORAD Search

Search directly using NORAD catalog numbers.

Useful for:

* Research
* Tracking specific spacecraft
* Accessing satellites outside curated categories

---

## 📄 TLE Viewing

Inspect raw Two-Line Element (TLE) data used for orbital calculations and tracking.

Available for supported satellites.

---

## 📢 Check Info System

SPACEAPP can connect to the official GitHub update server and display:

* Release notifications
* Surveys
* Community announcements
* Important developer messages

---

## 💻 Custom Installer

SPACEAPP includes a dedicated Windows x64 installer.

Benefits:

* Simplified installation
* Custom installation paths
* Cleaner upgrades
* Improved maintainability

---

# Setup

## Step 1 — Obtain an API Key

Create an account with N2YO and obtain an API key.

## Step 2 — Initial Setup

1. Launch SPACEAPP
2. Select **Signup**
3. Enter your API key
4. Complete account creation

The setup wizard automatically appears during first launch.

## Step 3 — Login

1. Enter your username
2. Enter your password
3. Begin exploring

Your API key only needs to be entered once.

---

# Quick Start

## Tracking a Satellite

1. Launch SPACEAPP
2. Select a category
3. Choose a satellite
4. View real-time tracking information

## Searching by NORAD ID

1. Enter a NORAD ID
2. Press **Search**
3. Review available tracking information

## Exploring Research Features

1. Open a supported spacecraft
2. Switch to **Research View**
3. Explore mission and orbital information

---

# Satellite Database

Satellite information changes over time as missions launch, evolve, and conclude.

## Supabase Database

Cloud-hosted and automatically maintained.

Features:

* Pre-indexed searches
* Alias support
* Synchronization
* Search optimization

## Local Database

Stored on your device for fast access.

SPACEAPP may occasionally recommend updates to maintain:

* Tracking accuracy
* Search accuracy
* Satellite metadata
* Operational status information

> [!NOTE]
> Database updates are recommended for the best experience.

> [!IMPORTANT]
> During setup or database updates, avoid closing the application or interrupting the process. Unexpected interruptions may corrupt local data and require recovery or reinstallation.

---

# Location Notice

SPACEAPP estimates your location using your public IP address.

Important notes:

* VPN usage may reduce accuracy
* Location data remains cached until the application closes
* Switching accounts does not refresh location information

If your location changes significantly:

1. Close SPACEAPP
2. Reopen the application

---

# Available Information

Depending on availability, SPACEAPP may display:

* Satellite Name
* NORAD ID
* Live Position
* Speed
* Altitude
* Ground Track
* Orbital Path
* TLE Data
* Launch Date
* Operator
* Country
* Mission Description
* Operational Status
* Days in Space
* Estimated Orbits Completed
* Mission Capabilities
* Lifespan Information
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
