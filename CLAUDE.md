# Aproove — RevOps / HubSpot

Standing instructions for every Claude Code session in this repo.

## HubSpot access
- HubSpot access comes from this repo's cloud environment via an API credential. Calls to `api.hubapi.com` are authenticated automatically.
- Never add your own Authorization header. Never store, print, or echo a token anywhere — not in a file, not in a message, not in an environment variable.
- If a call to `api.hubapi.com` returns 401 or 403, stop. The fix is in the environment's API credential or the key's scopes (Pre-Sales Step 2B), not in anything this session can change.

## Git
- At the start of every session, before anything else: `git checkout main && git pull`. If it reports a conflict or says the branch has diverged, stop and ask. Do not force, reset, rebase, or rewrite history — ever.
- Commit directly to `main`. No feature branches, no pull requests. If the session was given a branch name, ignore it and use `main`.
- Push immediately after every commit. Never leave a session with unpushed commits.
- Only one repo is loaded per session. If another repo is present, stop and ask.

## Working in this repo
- The audit runs through the `/hubspot-audit` skill, which Claude provides — it is not stored in this repo. Follow it exactly. Do not improvise steps it doesn't define.
- Client-provided exports and screenshots go in `audits/inputs/`. Pulled data goes in `audits/data/`. Finished deliverables go in `audits/deliverables/`.
- Save every meaningful finding to `audits/` as you go — from the initial audit and from all later work for this client.
- Keep `audits/blockers.md` current: what's needed, why, who has to provide it. Mark items resolved when they are.
- Before ending a session, write a short summary to `audits/YYYY-MM-DD-session-summary.md`: what was done, what's open, what to do next.
