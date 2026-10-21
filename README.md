# Cadence — Editorial Prose Humanizer & Revision Studio

Cadence is a content-preserving AI writing humanizer and editorial revision studio engineered to enhance sentence rhythm, natural cadence, and syntactic burstiness while strictly preserving 100% of facts, proper nouns, citations, and numbers.

---

## Deploying to Vercel

Cadence is a zero-dependency, client-side web application. It requires no backend server, no database, and no serverless function quotas. It deploys on Vercel's **Hobby / Free Plan ($0/month)** with instant global CDN distribution, automatic HTTPS, and zero maintenance.

### Method 1: Deploy in 60 Seconds via Vercel CLI (Recommended)

1. Open your terminal in this directory:
   ```bash
   cd cadence-vercel
   ```
2. If you don't have the Vercel CLI installed yet, install it globally:
   ```bash
   npm install -g vercel
   ```
3. Run the deploy command:
   ```bash
   vercel
   ```
   - Log in or authenticate if prompted.
   - Accept the default project settings (`Set up and deploy? [Y/n]` -> **Y**).
   - Vercel will instantly upload and give you a preview URL (e.g., `https://cadence-editorial-humanizer.vercel.app`).
4. To deploy directly to your production domain:
   ```bash
   vercel --prod
   ```

---

### Method 2: Deploy via GitHub / GitLab / Bitbucket (Automatic CI/CD)

1. Initialize a git repository and commit the project files:
   ```bash
   git init
   git add .
   git commit -m "Initial Cadence v4.1 deployment"
   git branch -M main
   ```
2. Create a new repository on GitHub (e.g. `cadence-humanizer`) and push your code:
   ```bash
   git remote add origin https://github.com/YOUR_USERNAME/cadence-humanizer.git
   git push -u origin main
   ```
3. Go to [vercel.com/new](https://vercel.com/new).
4. Select your `cadence-humanizer` repository and click **Import**.
5. In the configuration screen:
   - **Framework Preset**: `Other`
   - **Root Directory**: `./` (leave default)
   - **Build and Output Settings**: Leave defaults (no build step needed for static HTML).
6. Click **Deploy**. Vercel will build and assign you a free `*.vercel.app` domain. Any future `git push` to `main` will automatically trigger a zero-downtime production deployment!

---

### Method 3: Deploy via Vercel Web Dashboard (Drag & Drop)

1. Log in to [vercel.com/dashboard](https://vercel.com/dashboard).
2. Click **Add New...** -> **Project**.
3. If using the Vercel Web UI drag-and-drop feature, drag this unzipped `cadence-vercel` folder directly into the browser window.
4. Click **Deploy**.

---

## Custom Domains

Once deployed, you can assign any custom domain (e.g. `humanizer.yourdomain.com` or `yourdomain.com`):
1. In the Vercel Project Dashboard, navigate to **Settings** -> **Domains**.
2. Enter your custom domain and follow Vercel's DNS instructions (pointing an `A` record or `CNAME` record to Vercel's edge network).
3. Vercel provisions and renews SSL/TLS certificates automatically.

---

## Features & Privacy Guarantee

- **100% In-Browser Execution (Layer A Default)**: Text revision, entity locking, sentence alternatives, and LCS diffing run locally in the browser's JavaScript engine. No user prose is stored on any server.
- **Optional Hybrid AI (Layer C)**: Users can optionally provide their own OpenAI, Google Gemini, or Ollama endpoint. API keys are stored strictly in volatile session memory.
