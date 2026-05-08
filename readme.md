# 🏡 Real Estate Explorer

> A modern, map-first real estate platform built with Next.js 16, enabling users to discover, browse, and list properties with an interactive map experience.

<p align="center">
  <img src="./assets/Home-Page-Main.png" alt="Real Estate Explorer" width="100%" />
</p>

<p align="center">
  <a href="#overview">Overview</a> •
  <a href="#assets">Assets</a> •
  <a href="#tech-stack">Tech Stack</a> •
  <a href="#author">Author</a>
</p>

---

## Table of Contents

- [Overview](#overview)
- [Assets](#assets)
- [Tech Stack](#tech-stack)
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

## Assets

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

---

## Author

**Ahmad Bahar**
- GitHub: [@Ahmadbahar11](https://github.com/Ahmadbahar11)
- Email: ahmadbahar480@gmail.com

---

> 🔒 This is a confidential project built for a private client. Unauthorized distribution is not permitted.
