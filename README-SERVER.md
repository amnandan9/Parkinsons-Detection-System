# Server Setup Instructions

## Quick Start

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Start the backend server:**
   ```bash
   npm run server
   ```

   The server will run on `http://0.0.0.0:3001` and will be accessible from your network at `http://10.177.156.54:3001`

3. **Start the React app (in a separate terminal):**
   ```bash
   npm run dev
   ```

   The React app will run on `http://localhost:8080` and be accessible from your network at `http://10.177.156.54:8080`

## Alternative: Run Both Together

If you have `concurrently` installed globally:
```bash
npm install -g concurrently
npm run dev:all
```

## Server Endpoints

- `POST /api/sync` - Sync data (patient records, appointments, login/logout)
- `GET /api/patient-records` - Get all patient records
- `GET /api/appointments` - Get all appointments
- `GET /api/health` - Health check

## Data Storage

All data is stored in `server-data.json` in the project root. This file is created automatically when the server starts.

## Network Access

Make sure:
1. Your firewall allows connections on port 3001
2. Other devices on the network can access `http://10.177.156.54:3001`
3. The server is running before accessing the React app from other devices

