# 🏡 Real Estate Explorer

> A modern, map-first real estate platform built with Next.js 16, enabling users to discover, browse, and list properties with an interactive map experience.

<p align="center">
  <img src="./assets/Home-Page-Main.png" alt="Real Estate Explorer" width="100%" />
</p>

<p align="center">
  <a href="#overview">Overview</a> •
  <a href="#assets">assets</a> •
  <a href="#features">Features</a> •
  <a href="#tech-stack">Tech Stack</a> •
  <a href="#getting-started">Getting Started</a> •
  <a href="#docker-deployment">Docker</a>
</p>

---

## Table of Contents

- [Overview](#overview)
- [assets](#assets)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Pages & Routes](#pages--routes)
- [Component Architecture](#component-architecture)
- [Authentication System](#authentication-system)
- [Map System](#map-system)
- [API Integration](#api-integration)
- [State Management](#state-management)
- [Getting Started](#getting-started)
- [Environment Variables](#environment-variables)
- [Docker Deployment](#docker-deployment)
- [Author](#author)

---

## Overview

**Real Estate Explorer** is a full-featured property marketplace portal. It bridges the gap between traditional property listings and modern geospatial discovery — letting buyers, renters, agents, and agencies interact with properties directly on a live map.

Built as a **Next.js App Router** frontend communicating with a backend REST API gateway, it features:

- A rich interactive map powered by **Leaflet** with society layer overlays
- Property pin clustering and color-coded type markers
- Multi-step agent/agency onboarding
- JWT-based authentication with persistent sessions
- Full mobile responsiveness with skeleton loading states

> 🔒 **Note:** This is a proprietary, company-confidential project built for a private client. Source code and deployment are for internal use only.

### Who Is It For?

| User Type | What They Can Do |
|---|---|
| 🏠 Buyers / Renters | Search and browse properties via map or list view, filter by city, type, and price |
| 🏢 Agents & Agencies | Create a profile, list properties, and manage ads |
| 👁️ Visitors | Explore societies, view property details, and contact agents |

---

## assets

> 📸 Add your images to the `assets/` folder in the project root and they will render automatically below.

---

### 🏠 Hero / Home Page
<p align="center">
  <img src="./assets/Home-Page-Main.png" alt="Hero Section" width="100%" />
</p>

> Landing page with search bar, featured properties, map call-to-action, and advertisement banners.

---

### 🗺️ Interactive Map
<p align="center">
  <img src="./assets/Map-Section.png" alt="Interactive Map" width="100%" />
</p>

> Full-screen Leaflet map with property pins, WMS society overlays, base map switcher (street/satellite/terrain), and measurement tools.

---

### 🔍 Map Filters
<p align="center">
  <img src="./assets/Property-Maps-Sections.png" alt="Map Filters" width="100%" />
</p>

> Filter panel on the map allowing users to narrow down visible property pins by type, city, and intent (buy/rent).

---

### 🏘️ Property Listings
<p align="center">
  <img src="./assets/Project-page.png" alt="Property Listings" width="100%" />
</p>

> Browse all properties with filters for city, type (residential/commercial), price range, and buy/rent intent.

---

### 📄 Property Detail
<p align="center">
  <img src="./assets/Detail-Society-Page.png" alt="Property Detail" width="100%" />
</p>

> Full property detail page including image gallery, description, map location, pricing, and agent contact info.

---

### 💎 Premium Properties
<p align="center">
  <img src="./assets/Featured-Properties-Section.png" alt="Premium Listings" width="100%" />
</p>

> Dedicated page showcasing highlighted and featured premium property ads.

---

### 👥 Agents Directory
<p align="center">
  <img src="./assets/Agent-Page.png" alt="Agents Directory" width="100%" />
</p>

> Browse all agents and agencies with top-rated spotlights, new agency highlights, and city-based filtering.

---

### 🏢 Agency Profile
<p align="center">
  <img src="./assets/Agent-Profile.png" alt="Agency Profile" width="100%" />
</p>

> Individual agent/agency profile page with their listed properties, contact info, and staff carousel.

---

### 🏙️ Societies
<p align="center">
  <img src="./assets/Societies-Section.png" alt="Societies Page" width="100%" />
</p>

> Browse housing societies with city-based filtering and individual society detail pages with map integration.

---

### 🔐 Login
<p align="center">
  <img src="./assets/Auth.png" alt="Login Screen" width="100%" />
</p>

> Secure login page with email/password authentication and JWT session management.

---

### 📝 Signup Flow
<p align="center">
  <img src="./assets/Auth.png" alt="Signup Flow" width="100%" />
</p>

> Registration flow for individual users and agents, including the two-step agency onboarding with company details.


## Features

### 🏘️ Property Browsing
- Browse properties for **sale** and **rent**
- Filter by property type, city, price range, and intent
- **Featured Properties** section on the homepage
- **Premium Properties** section with a dedicated page
- Property detail page with full information, images, location, and nearby amenities

### 🗺️ Interactive Map
- Full-screen **Leaflet** map
- Switch between **base map styles** (Satellite, Street, Terrain)
- Toggle **WMS society layers** to visualize housing society boundaries
- **Property pins** on the map with color-coded property types
- **Opacity control** for overlay layers
- **Locate me** button (GPS geolocation)
- **Copy URL** of current map view for shareable deep-links
- **Place marker** tool for custom location pinning
- Built-in **measurement tools** (distance and area)
- Society label markers with zoom-aware visibility

### 🔐 Authentication
- **Login** with email and password
- **Individual Signup** for regular users
- **Agent/Agency Signup** with a multi-step flow:
- **Country/State/City** dropdowns for location selection
- **Secure session management** using persistent authentication cookies
- **Automatic authentication handling** for all user requests

### 👤 Agents & Agencies
- Browse all agents and agencies
- **Top-rated agencies** section
- **New agencies** spotlight section
- **Browse agents by city**
- Individual **agent profile page** with listings and contact info
- Staff carousel within agency profiles

### 🏙️ Societies
- Browse all housing societies
- Filter societies by **city**
- Individual **society detail page** with map integration
- Society layer toggle directly from the map

### 📄 Content Pages
- **About Us** — company information
- **Contact Us** — contact form
- **Legal Documentation** — property legal guides
- **Real Estate Media** — media/news section
- **Properties Transfer Process** — step-by-step guides

### ⚡ UX & Performance
- Skeleton loaders during data fetch
- Toast notifications for success/error feedback
- Fully **responsive** design (mobile, tablet, desktop)
- Dynamic imports for heavy client-side components (map)
- Breadcrumb navigation on inner pages

---

## Tech Stack

| Category | Technology |
|---|---|
| Framework | Next.js 16.1.4 (App Router) |
| UI Library | React 19.2.3 |
| Language | TypeScript 5 |
| Styling | Tailwind CSS 4.1.18 |
| Component Library | Material UI (MUI) 7.3.6 |
| Maps | Leaflet 1.9.4 + React-Leaflet 5.0.0 |
| Map Measure Tool | react-leaflet-measure 3.0.1 |
| HTTP Client | Axios 1.13.2 |
| Auth / Cookies | cookies-next 6.1.0 |
| Notifications | react-toastify 11.0.5 |
| Skeleton Loaders | react-loading-skeleton 3.5.0 |
| Icons | Lucide React 0.561.0 + react-icons 5.5.0 |
| Containerization | Docker (Node 20 Alpine) |


## Project Architecture
The project follows a modular architecture for scalability and maintainability, separating concerns between UI components, state management, and external service integrations.

## Map System
The core map experience is built with industry-standard geospatial tools, providing high-performance rendering of property locations and society boundaries with intuitive user controls.

## API Integration
All data is fetched from a secure central backend service, ensuring consistent and up-to-date property information across the entire platform.

## State Management
Global application state is managed efficiently to handle user sessions, map configurations, and property search results seamlessly.
---
## Author

**Ahmad Bahar**
- GitHub: [@Ahmadbahar11](https://github.com/Ahmadbahar11)
- Email: m.zubair@neuronixtech.com

---

> 🔒 This is a confidential project built for a private client. Unauthorized distribution is not permitted.
