# AGENTS — AI assistant instructions (focus: server)

Purpose
- Provide concise, actionable guidance to AI coding agents working on server-related tasks for this repository. Keep recommendations minimal and link to repo files when relevant.

Repository layout (quick links)
- [index.html](index.html)
- [about.html](about.html)
- [contact.html](contact.html)
- [products.html](products.html)
- [services.html](services.html)
- [css/style.css](css/style.css)
- [js/script.js](js/script.js)

Assumptions
- This is a static website with HTML/CSS/JS assets served from the project root. There is no build step or backend present by default.

Local development — quick servers
- Python 3 (quick, zero-deps):

```bash
python -m http.server 8000
# then open http://localhost:8000
```

- Node (npx `serve`):

```bash
npx serve .  # or `npm i -g serve` then `serve .`
```

When to add a server
- If a feature requires dynamic routes, APIs, or server-side logic, prefer adding a small, well-documented server under a `server/` directory. Suggested minimal stacks:
  - Node + Express for JavaScript familiarity
  - A small Python Flask app if Python is preferred

Suggested tasks for agents (server-focused)
- Add a minimal Express server to serve static files and provide simple API endoints (create `server/index.js`).
- Add `Dockerfile` and `.dockerignore` for containerized serving.
- Add a development script for live reload (`browser-sync` or `nodemon`).
- Add basic CORS and security headers for APIs when applicable.
- Document any new server commands in `AGENTS.md` and update README.md with run instructions.

Action conventions
- Keep pull requests small and focused: one PR per server feature (e.g., "Add Express dev server").
- Include a short README inside `server/` explaining run commands, ports, and environment variables.

Notes for reviewers
- Verify that any server added does not expose secrets. If environment variables are required, add a `.env.example` and document expectations.

If you want, I can:
- scaffold a minimal Express server and Dockerfile
- or add a one-line dev script for Python-based serving
