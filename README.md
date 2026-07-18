# MedCare

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![React](https://img.shields.io/badge/React-18-blue)
![TypeScript](https://img.shields.io/badge/TypeScript-5.0-blue)
![Express](https://img.shields.io/badge/Express-4.x-lightgrey)
![SQLite](https://img.shields.io/badge/SQLite-3-blue)
![Playwright](https://img.shields.io/badge/E2E-Playwright-green)

A prototype full-stack healthcare application demonstrating end-to-end integration of a React frontend with a local Node.js/Express backend and SQLite database. 

## System Architecture

- **Frontend**: React via Vite with TypeScript.
- **Backend**: Express (Node.js) REST APIs.
- **Database**: SQLite3 (`server/medcare.db`) for isolated, persistent local storage.
- **Testing**: Playwright for end-to-end UI and API validation.

## Local Development Setup

1. **Install Dependencies**
   ```bash
   npm install
   ```

2. **Initialize Database**
   Seeds the SQLite database with demo data (doctors, medicines, appointments).
   ```bash
   node server/seed.js
   ```

3. **Start Servers Concurrently**
   Starts both the Vite development server (`http://localhost:5173`) and the Express API server (`http://localhost:3001`).
   ```bash
   npm run dev:full
   ```

## Testing

**Backend API Validation**
Executes CRUD operations against the SQLite database via the Express endpoints:
```bash
node server/test_api.js
```

**End-to-End Testing**
Runs the Playwright suite simulating user workflows (Appointment booking, authentication, etc.).
- Headless execution:
  ```bash
  npx playwright test
  ```
- Visual execution with slow-motion tracing:
  ```bash
  python3 visual_test.py
  ```

## Attributions

- UI Components from [shadcn/ui](https://ui.shadcn.com/) (MIT License).
- Stock photography from [Unsplash](https://unsplash.com) (Unsplash License).