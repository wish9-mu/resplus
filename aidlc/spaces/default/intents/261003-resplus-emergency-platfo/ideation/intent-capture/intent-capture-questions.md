## Sources

- [desc] Initial description: "Analyze this repository for the Res+ emergency coordination platform. Read TECH_STACK.md and FLOW.md as the source of truth. Do not implement features yet. First: 1. Inspect the existing repository. 2. Determine what is already implemented. 3. Identify missing dependencies and configuration. 4. Propose the folder structure. 5. Define the minimum viable hackathon architecture. 6. Identify the critical user journeys: Household, BHW, Ambulance, ER. 7. Identify external integrations that require API keys. 8. Create an implementation plan ordered by dependency. Do not change the core flow described in FLOW.md. Prioritize a working end-to-end demo over production-scale architecture."
- [scope] Workflow-selected scope: `mvp`.

---

## Q1. What is the core business problem Res+ solves?

In the Philippine emergency response context, what is the primary gap that Res+ addresses?

A. Slow emergency response due to lack of coordination between family, BHW, ambulance, and ER
B. Lack of patient medical data at the point of emergency care
C. Inability of BHWs to give first aid coaching during emergencies
D. No real-time traffic routing for ambulances
E. All of the above — end-to-end coordination gap from SOS to ER handoff

[Answer]:

---

## Q2. Who is the primary intended user for the hackathon demo?

A. Judges evaluating technical completeness and real-world viability
B. Actual BHWs and ER staff in a municipality
C. LGU officials and MHO administrators
D. General public households only

[Answer]:

---

## Q3. What does success look like for this hackathon submission?

A. A working end-to-end demo from SOS tap to ER arrival, covering all 4 roles
B. A deployed public URL with all API integrations live and real data flowing
C. A prototype showing the core SOS → BHW confirm → dispatch → ER accept flow (subset of full flow)
D. A fully production-ready system with Row Level Security, pg_cron escalations, and all fallbacks working

[Answer]:

---

## Q4. Which user journeys are absolutely required for the demo vs. nice-to-have?

The four roles defined in FLOW.md are: Household (SOS), BHW (confirm + coach), Ambulance (hospital pick + route), ER (accept/divert).

A. All four are required and must be fully functional end-to-end
B. Household + BHW are core; Ambulance + ER are nice-to-have
C. Household + BHW + Ambulance are core; ER accept/divert is nice-to-have
D. Only the Household SOS button needs to work for MVP demo
X. Other (please specify)

[Answer]:

---

## Q5. What is the target deployment environment for the demo?

A. Vercel (public URL, as specified in TECH_STACK.md)
B. Local development only (localhost demo)
C. Any cloud platform with a public URL
D. Not yet decided

[Answer]:

---

## Q6. Are all external API keys and accounts already provisioned?

The platform requires: Supabase, Agora (RTC + STT), AWS Bedrock (Claude), Google Maps + Routes API, and Vercel.

A. Yes, all keys are ready
B. Some are ready — specify which are missing in Other
C. None are ready yet
D. Only Supabase and Google Maps are ready
X. Other (please specify)

[Answer]:

---

## Q7. What is the team's primary frontend/backend experience?

This informs how much of the existing TECH_STACK.md choices (Next.js App Router, Supabase, TypeScript) are already familiar.

A. Experienced with Next.js App Router and TypeScript
B. Familiar with React but new to Next.js App Router
C. Backend-focused team, frontend is a challenge
D. Full-stack team comfortable with the entire stack
X. Other (please specify)

[Answer]:

---

## Q8. Is there a hard deadline for the hackathon submission?

A. Yes — within the next 24 hours
B. Yes — within the next 48–72 hours
C. Yes — within the week
D. Not specified / flexible

[Answer]:

---

## Assumptions & Open Questions

- [assumption] The repository at https://github.com/wish9-mu/resplus.git is the target repository where all code will be developed and submitted.
- [assumption] TECH_STACK.md and FLOW.md are the authoritative design documents and must not be changed.
- [assumption] The hackathon goal is a working demo, not a production system — some features (pg_cron escalations, Row Level Security, full PWA offline) may be deferred if they block the core flow demo.
- [assumption] The team wants to build the system from scratch (greenfield) since the repository was empty.
- [assumption] "Do not implement features yet" means this analysis stage should produce a plan, not code.
