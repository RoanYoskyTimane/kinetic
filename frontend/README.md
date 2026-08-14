# Kinetic Frontend (React)

## What it is
A React + TypeScript + Vite single-page dashboard application frontend for the Kinetic Workout Tracker.

## What it does
* **Responsive Dashboard**: Delivers a workout tracker interface optimized for mobile and desktop screens.
* **Modern Design System**: Features smooth interactive animations built with `framer-motion` and structured icons from `lucide-react`.
* **Session Management**: Connects to the backend REST API, managing secure JWT auth states and API requests using `axios`.
* **Cloudflare Integrated**: Ready to deploy using Cloudflare Wrangler CLI.

## How to execute it
### Prerequisites
* [Node.js](https://nodejs.org/) (v18 or higher).
* npm package manager.

### Steps
1. **Configure Environment Variables**:
   Create a `.env` file in the root `frontend` directory:
   ```env
   VITE_API_URL=http://localhost:8080/api/v1
   ```

2. **Install Dependencies**:
   ```bash
   npm install
   ```

3. **Run Development Server**:
   ```bash
   npm run dev
   ```
   Navigate to the URL displayed in the console (usually `http://localhost:5173`).

### Deploying (Cloudflare wrangler)
* **Local Wrangler Dev Server (Preview)**:
   ```bash
   npm run preview
   ```
* **Deploy to Cloudflare Pages**:
   ```bash
   npm run deploy
   ```
