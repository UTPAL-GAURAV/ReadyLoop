# ReadyLoop — Agent Repo

This is the local agent repo for [ReadyLoop](https://ready-loop-ui.vercel.app) — an AI-powered interview preparation app.

All interview interaction happens here via Claude. The dashboard at the link above is display-only.

---

## Setup

**1. Clone this repo**

```bash
git clone https://github.com/UTPAL-GAURAV/ReadyLoop.git
cd ReadyLoop
```

**2. Get your auth token**

- Go to [ReadyLoop](https://ready-loop-ui.vercel.app)
- Sign in with Google
- Click **Copy token** in the header

**3. Add credentials to `.env`**

Open `.env` and fill in both values:

```
GOOGLE_AUTH_TOKEN=<paste token here>
BACKEND_BASE_URL=https://readyloop-backend.onrender.com
```

`BACKEND_BASE_URL` is the Render backend URL. Only change it if you are running the backend locally.

**4. Start a session**

Open this repo in Claude Code (CLI, VS Code extension, or desktop app) and paste a job description:

```
Paste a JD and say: "Prepare me for this role"
```

Claude reads `CLAUDE.md` automatically — no extra setup needed.

---

## How it works

- Claude reads your JD, identifies company, role, level, and geography
- Generates a structured interview plan with rounds and pre-evaluated questions
- Conducts mock interviews with adaptive follow-up questioning
- Saves all data to the backend — view results on the dashboard

---

## Related repos

- [ReadyLoop-UI](https://github.com/UTPAL-GAURAV/ReadyLoop-UI) — React dashboard
- [ReadyLoop-Backend](https://github.com/UTPAL-GAURAV/ReadyLoop-Backend) — Node.js REST API
