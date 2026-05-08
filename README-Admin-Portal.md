# PlotsMap — Admin Frontend (Private)

This repository contains **documentation only** for the PlotsMap Admin Frontend.  
Because this is a **company project**, the **source code is not published** here.

## Security / IP Notice (Important)

- **No source code** is included in this GitHub repository.
- **Do not** add application code, environment files, secrets, API keys, or internal URLs.
- Screenshots are allowed (after review), but should avoid exposing sensitive user data.

## What this app is

PlotsMap Admin Frontend is a web portal used to operate the PlotsMap platform. It provides role-based access to manage:

- Users and access permissions
- Agents and sub-agents
- Leads lifecycle and assignment
- Properties and map-based interactions
- Ads and ad placements on map
- Plans, subscriptions, upgrades, and transactions
- Societies, projects, and location configuration

## Tech stack

- **Framework**: Next.js (App Router)
- **Language**: TypeScript + React
- **UI**: Material UI (MUI) + Tailwind CSS utilities
- **State management**: Zustand (persisted auth + nav state)
- **Networking**: Axios (central API instance with interceptors)
- **Maps**: Leaflet + React-Leaflet (with measurement tools)
- **Charts**: Recharts
- **Editor / Rich text**: React Quill
- **UX**: toast notifications + top progress bar

## Environments & configuration

### Required environment variables

Create a `.env` file (kept private; **do not commit** it).

- **`NEXT_PUBLIC_GATEWAY_URL`**: Base URL of the backend gateway used by the frontend API client.
  - Example: ask project lead for the correct value per environment (dev/staging/prod).

### Authentication & session handling (high-level)

- Login and auth operations call backend endpoints under `/admin/*`.
- The API client attaches a `Bearer` token from cookies to each request.
- On authentication failure (401 / token invalid/expired), the UI triggers an automatic logout and shows a “session expired” message.

### Roles & permissions (high-level)

Roles are modeled as numeric IDs, for example:

- Admin
- Agent
- Sub-agent
- Owner

The UI gates navigation and actions using named permissions such as:

- User management (create/edit/delete/view, reset password, manage permissions)
- Ads / Properties / Agents / Sub-agents / Plans (create/edit/delete/view)
- Subscriptions, leads, societies, projects, location management, interested areas

## Main modules (screens) in the portal

The application is organized into two route groups:

- **Auth routes**: login, register, forgot/reset/set password, not-authorized
- **Main routes**: authenticated portal pages with a side navigation + top navigation layout

### Dashboard

- Overview dashboards for different roles (Admin/Agent/User)
- Stats cards and operational summaries

### Leads management

- Leads listing + details modal
- Lead assignment workflows (agent/sub-agent)
- Location-based lead breakdown (where applicable)

### Users management

- Create/edit/delete users
- Permission management (role-based + explicit permissions)
- Password reset flows

### Agents & sub-agents management

- Agents list and lifecycle management
- Sub-agent list under an agent (drill-down management)

### Properties management

- Create/edit properties
- Property images, amenities, size & location sections
- Map picker and map viewer experiences

### Ads management (Map-focused)

- Create/publish/edit ads
- Map-based ad placement and visualization
- Marker layers, opacity controls, locate controls, and related map tools

### Plans, subscription & upgrades

- Plan management (add/edit)
- Subscription history
- Upgrade flow (plan cards, payment modal, results)

### Societies, projects, locations, interested areas

- Societies & projects management screens
- Location management configuration
- Interested areas CRUD

### Transactions

- Transaction listing / history screen (billing/audit purposes)

## Directory layout (documentation-level)

- `app/`: Next.js App Router routes, layouts, and pages
- `components/`: UI components (tables, modals, navigation, map viewer, forms)
- `services/`: API client + per-module API calls (auth, users, leads, properties, maps, etc.)
- `store/`: Zustand stores (auth + nav)
- `types/`: TypeScript types for modules (dashboard, ads, plans, agents, leads, map, etc.)
- `utils/`: helpers (auth utilities, date utilities, route protection builder, validators)
- `constants/`: roles, permissions, navigation configuration

## Local development (internal use only)

> This section is intended for company/internal environments. Do not include private URLs or credentials in commits.

### Prerequisites

- **Node.js**: v20+
- **npm**: v10+

### Install & run

```bash
npm install
npm run dev
```

The app runs on `http://localhost:3000` by default.

### Production build

```bash
npm run build
npm run start
```

## Deployment notes (high-level)

- The Next.js build is configured for a **standalone** output (suitable for containerization).
- Any Docker or server deployment should inject the correct environment variables at runtime.

## Screenshots (to be added)

> Add screenshots in a `docs/screenshots/` folder (recommended), and link them here.

### Auth

- **Login**: _TODO_
- **Forgot password**: _TODO_
- **Reset/Set password**: _TODO_

### Portal

- **Dashboard**: _TODO_
- **Leads management**: _TODO_
- **Users management**: _TODO_
- **Agents & sub-agents**: _TODO_
- **Properties management**: _TODO_
- **Ads management (map)**: _TODO_
- **Plans & subscription**: _TODO_
- **Societies / Projects / Locations / Interested Areas**: _TODO_
- **Transactions**: _TODO_

## Support / access

- For environment values, access, and onboarding, contact the project lead or IT/admin team.

## License

**Private (internal company project).** Redistribution or publication of source code is not permitted.
