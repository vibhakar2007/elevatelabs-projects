EventManager – Full‑Stack Event Management System

Overview
EventManager lets customers discover events, register, download QR‑coded PDF tickets, and post reviews, while organizers create/manage events, see participants, export CSVs, and perform real‑time check‑ins.

### 💻 Tech Stack

# Backend</br>

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)

## Frontend</br>
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![React Router](https://img.shields.io/badge/React_Router-CA4245?style=for-the-badge&logo=react-router&logoColor=white)
![Axios](https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge&logo=axios&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)

## Realtime </br>
![Socket.IO](https://img.shields.io/badge/Socket.IO-010101?style=for-the-badge&logo=socket.io&logoColor=white)

## PDFs / QR</br>
![html2canvas](https://img.shields.io/badge/html2canvas-5A5A5A?style=for-the-badge)
![jsPDF](https://img.shields.io/badge/jsPDF-CA4245?style=for-the-badge)
![QR_Code](https://img.shields.io/badge/Custom_QR-000000?style=for-the-badge&logo=qrcode&logoColor=white)

## Tooling</br>
![ESLint](https://img.shields.io/badge/ESLint-4B32C3?style=for-the-badge&logo=eslint&logoColor=white)
![Prettier](https://img.shields.io/badge/Prettier-F7B93E?style=for-the-badge&logo=prettier&logoColor=black)
![Nodemon](https://img.shields.io/badge/Nodemon-76D04B?style=for-the-badge&logo=nodemon&logoColor=white)
![PostCSS](https://img.shields.io/badge/PostCSS-DD3A0A?style=for-the-badge&logo=postcss&logoColor=white)


Monorepo Structure
- backend/ – Express API, Socket.IO, MongoDB models, routes, controllers
- frontend/ – Vite React app (Tailwind), pages and hooks

Getting Started
Prerequisites
- Node.js 18+
- MongoDB running locally or a connection string

1) Clone and install
```bash
git clone https://github.com/vibhakar2007/elevatelabs-projects/evently
cd evently

# Backend deps
cd backend && npm install

# Frontend deps
cd ../frontend && npm install
```

2) Configure environment
Create `backend/.env` with values similar to:
```env
PORT=5050
MONGODB_URI=mongodb://localhost:27017/eventmanager
JWT_SECRET=supersecret
CLIENT_ORIGIN=http://localhost:5173
```

3) Run locally
Terminal A (backend):
```bash
cd backend
npm run dev
```

Terminal B (frontend):
```bash
cd frontend
npm run dev
```

Seeding (optional)
```bash
cd backend
node src/seed.js
```

Demo Accounts
- Customer: customer@example.com / password
- Organizer: organizer@example.com / password
- Admin: admin@example.com / password

Key Features
- Customers: browse events, register, download branded PDF tickets with QR, post reviews
- Organizers: create/manage events, view participants, export CSV, real‑time check‑in
- Admin: approve/reject events
- Home: recommendations, all events, statistics
- Dark mode, toast notifications, responsive UI

Notable Hooks
- useTicketPDF: generate branded ticket PDFs from HTML
- useQrCheckIn: perform QR/ID check‑ins with live status (Socket.IO)

Scripts
Backend (`backend/package.json`):
- `npm run dev` – start server with nodemon

Frontend (`frontend/package.json`):
- `npm run dev` – start Vite dev server
- `npm run build` – production build
- `npm run preview` – preview build

Deployment Notes
- Set environment variables (`PORT`, `MONGODB_URI`, `JWT_SECRET`, `CLIENT_ORIGIN`)
- Serve frontend build (Vite `dist/`) via your host or CDN
- Run backend as a service (PM2/Docker) and ensure CORS allows your frontend origin

License
MIT


