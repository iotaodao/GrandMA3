# GrandMA3 Macro Agent

AI-powered assistant for fixing and generating GrandMA3 Macros and Lua scripts.

## Installation

### Prerequisites
- Node.js (v18 or higher)
- npm or yarn
- Google Gemini API Key

### Setup
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/ma3-agent.git
   cd ma3-agent
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Configure Environment:
   Create a `.env` file in the root directory:
   ```env
   API_KEY=your_google_gemini_api_key
   ```

### Development
To run the application locally:
```bash
npm run dev
```

### Production Deployment (PM2)
To run the application on a server using PM2:

1. **Install PM2 globally:**
   ```bash
   npm install -g pm2
   ```

2. **Build the application:**
   ```bash
   npm run build
   ```

3. **Start the application:**
   Serve the `dist` folder on port 3000 in SPA mode:
   ```bash
   pm2 serve dist 3000 --name "ma3-agent" --spa
   ```

4. **Setup Auto-restart:**
   Save the process list and generate startup script:
   ```bash
   pm2 save
   pm2 startup
   ```

### Management
- Restart: `pm2 restart ma3-agent`
- Stop: `pm2 stop ma3-agent`
- Logs: `pm2 logs ma3-agent`
