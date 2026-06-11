# OctoFit Tracker

A modern multi-tier application built with React 19, Node.js/Express, TypeScript, and MongoDB.

## Project Structure

```
octofit-tracker/
├── frontend/          # React 19 + Vite + TypeScript
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── vite.config.ts
└── backend/          # Node.js + Express + TypeScript + Mongoose
    ├── src/
    ├── package.json
    ├── tsconfig.json
    ├── .env
    └── .gitignore
```

## Tech Stack

### Frontend
- React 19
- Vite 5
- TypeScript
- Port: 5173

### Backend
- Node.js
- Express 4.18
- TypeScript
- Mongoose 8 (MongoDB ODM)
- CORS enabled
- Port: 8000

### Database
- MongoDB
- Port: 27017

## Getting Started

### Prerequisites
- Node.js 18+ and npm
- MongoDB running locally or connection string configured

### Frontend Setup

```bash
cd frontend
npm run dev
```

The frontend will be available at `http://localhost:5173`

### Backend Setup

```bash
cd backend
npm run dev
```

The backend will be available at `http://localhost:8000`

### Environment Configuration

**Backend (.env)**
```
PORT=8000
MONGODB_URI=mongodb://localhost:27017/octofit
NODE_ENV=development
```

## Available Scripts

### Frontend
- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build

### Backend
- `npm run dev` - Start development server with hot-reload
- `npm run build` - Build TypeScript to JavaScript
- `npm start` - Start production server
- `npm run lint` - Run ESLint

## API Health Check

Once the backend is running:
```bash
curl http://localhost:8000/health
```

Expected response:
```json
{ "status": "healthy" }
```

## MongoDB Connection

The backend automatically connects to MongoDB on startup. Ensure MongoDB is running on `mongodb://localhost:27017/octofit` or update the `MONGODB_URI` in the `.env` file.

## Development

Both frontend and backend run independently. You can develop and test them separately or run them side-by-side.

- Frontend communicates with backend API
- Backend serves as the REST API
- MongoDB stores application data

---

**Current Status**: Project initialization complete with all dependencies installed and ready for development.
