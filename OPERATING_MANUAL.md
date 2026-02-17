# OPERATING_MANUAL.md — System Operating Manual (Bob/Marshall)

## Purpose
This manual documents:
- How Bob & MarshallBot are set up
- Key workspace settings and structure
- Credential and automation setup locations
- Limits and manual steps (e.g. Vercel linking)
- How to troubleshoot, upgrade, or extend the system

## 1. Core Structure
- **Bob/MarshallBot Workspace:** `/Users/moltbot/.openclaw/workspace/bob` (all agent/system files)
- **Dashboard Project Repo:** https://github.com/marshall-moltbot/dashboard-marshall-bob
- **Live Dashboard URL:** https://dashboard-marshall-bob.vercel.app
- **Main Workspace:** `/Users/moltbot/.openclaw/workspace/` (shared by all agents)

## 2. Credentials & Config
- **GitHub PAT:** Saved in `/secure/github-pat-bob.txt`
- **Vercel Deploy:** Manual repo link required for each new project on the Free plan. Auto if upgraded to Pro.
- **Secrets/Env Vars:** Managed via Vercel dashboard (manual step, see project settings)

## 3. Automation/Manual Step Notes
- Bob creates/manages all repos, pushes, code automation, and journaling.
- **Current limitation:** On Free plan, after Bob creates a repo, you must log into Vercel, click “Add Project,” and manually select the new repo for deploy (takes 2 clicks, no code).
- **To unlock full hands-off automation:** Upgrade to Vercel Pro and add Bob’s GitHub/Email as a team member.

## 4. Troubleshooting
- See AGENTS.md and SOUL.md for Bob’s operating principles and escalation policy.
- GitHub CLI must be globally accessible and authenticated on host machine.
- If automation fails, Bob will alert you INSTANTLY and suggest a manual step.

## 5. Review & Ownership
- Changes to this manual should be surfaced on the dashboard in the “Manuals & Reviews Pending” widget for human sign-off.
- Anyone can add FAQs, onboarding tips, or upgrade notes here.
