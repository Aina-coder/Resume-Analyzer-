# AI Job Preparation & Resume Analyzer Platform

An intelligent full-stack web application built to streamline interview preparation. Users can securely authenticate, upload their resumes, evaluate core skill gaps against custom job descriptions, simulate complex technical/behavioral interview environments, and generate custom ATS-optimized resume PDFs.

## 🚀 Key Engineering Pillars
- **Secure Authentication & Middleware:** State-managed JWT cookies paired with custom server-side Token Blacklisting for absolute session isolation during logouts.
- **Strict GenAI Orchestration:** Structured Zod-to-JSON validation layer binding the Google Gemini API to predictable array schemas.
- **Headless Document Pipelines:** Asynchronous server-side HTML rendering to dynamic PDF file streams powered by Puppeteer.

## 📁 Workspace System Layout
- `/Frontend` - Modular React.js Single Page Application scaffolded via Vite, featuring a production-ready 4-Layer architectural design (UI, Custom Hooks, Global State Context, Axios Service Abstraction).
- `/Backend` - Express.js REST API cleanly engineered using an MVC (Model-View-Controller) folder structure to manage persistent database mappings and AI data pipelines.

## 🛠️ Local Environment Workspace Setup

### 1. Project Initialization
```bash
git clone https://github.com
cd Resume-Analyzer-
```

### 2. API Server Workspace (Backend)
1. Navigate to the backend folder: `cd Backend`
2. Spin up dependency modules: `npm install`
3. Configure your localized `.env` parameters using this structural layout:
   ```env
   PORT=3000
   MONGODB_URI=your_mongodb_atlas_cluster_connection_string
   JWT_SECRET=your_jwt_private_signing_key
   AI_API_KEY=your_google_ai_studio_gemini_api_credential_key
   ```
4. Run the development listener: `npm run dev`

### 3. Client Workspace (Frontend)
1. Launch an isolated secondary shell and enter the frontend directory: `cd Frontend`
2. Download node modules: `npm install`
3. Spin up the localized Vite development server: `npm run dev`
