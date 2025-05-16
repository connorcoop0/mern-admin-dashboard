# MERN Admin Dashboard

A full-stack admin dashboard built with the MERN stack (MongoDB, Express, React, Node).  
The application provides real-time data visualisation, CRUD operations, and an intuitive UI for managing users, products, and transactions.

---

## Team

| Name                | Email                |
|---------------------|----------------------|
| Renzo Broggi        | rb21q@fsu.edu        |
| Jacob Mannix        | jcm18e@fsu.edu       |
| Ian Rockette        | ibr22@fsu.edu        |
| Tatiana Cue         | tbc20n@fsu.edu       |
| Connor Coop         | cjc22m@fsu.edu       |

---

## Features

### Dashboard  
- At-a-glance KPIs (total users, sales, active sessions, etc.).  
- Charts rendered with Recharts (area, bar, and line charts).

### Geography Page  
- Interactive world map with country-level shading.  
- Heat-map colouring: darker blue indicates more users in that country.

### Transactions Page  
- Paginated table of recent transactions (server-side pagination).  
- Search, sort, and adjustable page size.  
- CSV export.

### Additional Pages  
- User management with add / edit / delete.  
- Product catalogue with inventory status.  
- Profile settings and JWT-based authentication.

---

## Tech Stack

| Layer               | Library / Tool                |
|---------------------|--------------------------------|
| Front-end           | React 18, React Router, Redux Toolkit |
| Styling             | Material-UI v5                 |
| Charts              | Recharts, Nivo                |
| Map                 | `@nivo/geo` + world-110m TopoJSON |
| Back-end            | Node.js, Express              |
| Database            | MongoDB (Mongoose)            |
| Auth                | JSON Web Tokens, bcrypt       |
| Testing             | Jest, React Testing Library   |
| Build / CI          | Vite / Webpack, ESLint, Prettier |

---

## Prerequisites

- Node.js 18+ and npm  
- MongoDB instance (local or Atlas)  
- Optional: Docker for containerised setup

---

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/connorcoop0/mern-admin-dashboard.git
   cd mern-admin-dashboard
   ```

2. Install dependencies for both client and server:

   ```bash
   npm install          # installs root (server) deps
   cd client
   npm install          # installs React deps
   cd ..
   ```

3. Configure environment variables:

   ```bash
   # server/.env
   PORT=5000
   MONGO_URI=<your-mongodb-connection-string>
   JWT_SECRET=<random-long-string>
   ```

4. (Optional) Seed sample data:

   ```bash
   npm run seed
   ```

5. Start development (concurrently runs client and server):

   ```bash
   npm run dev
   ```

   - React dev server: `http://localhost:3000`  
   - API server: `http://localhost:5000/api`

---

## Scripts

| Command              | Description                      |
|----------------------|----------------------------------|
| `npm run dev`        | Run client and server concurrently |
| `npm run server`     | Start Express API                |
| `npm run client`     | Start React dev server           |
| `npm run build`      | Build React for production       |
| `npm run seed`       | Populate MongoDB with mock data  |
| `npm test`           | Run unit and integration tests   |

---

## Folder Structure

```
root
 ├─ client/            # React front-end
 │   ├─ src/
 │   │   ├─ components/
 │   │   ├─ pages/
 │   │   └─ redux/
 │   └─ vite.config.js
 ├─ server/
 │   ├─ controllers/
 │   ├─ models/
 │   ├─ routes/
 │   └─ server.js
 ├─ seed/              # mock data scripts
 ├─ .env.example
 └─ README.md
```

---

## Roadmap

- Role-based access control (RBAC)  
- Docker Compose for local development  
- Unit tests for Express routes  
- Dark / light theme toggle

---
