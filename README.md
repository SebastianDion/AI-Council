# AI-Council 🏛️

A multi-agent decision support skill for Claude Code, Antigravity, and AI coding assistants. Inspired by PewDiePie's AI Council and the Diverse Multi-Agent Debate (DMAD) framework.

Instead of getting a single generic AI opinion or an unverified echo-chamber, **AI-Council** runs a rigorous deliberation pipeline: independent takes → blind peer review → evidence ledger & red-team challenge → Chairman synthesis.

---

## The Council Roster

| Seat | Member | Archetype | Core Focus |
|---|---|---|---|
| 1 | **🦇 Batman** | Chief Strategist & Devil's Advocate | Worst-case analysis, hidden risks, contingency planning |
| 2 | **📖 Kakashi Hatake** | Chief Learning Officer & Mentor | Sustainable growth, mental adaptability, long-term mastery |
| 3 | **⚡ Tony Stark** | CTO & Opportunity Hunter | Execution leverage, prototypes, speed, asymmetrical upside |
| 4 | **🎯 Domain Specialist** | Rotating Expert | Dynamically chosen based on topic (finance, systems, career, etc.) |
| 5 | **👀 The Outsider** | Deliberate Naive Observer | Asks simple/critical questions, cuts through jargon & groupthink |

---

## How It Works (Reliability Architecture)

```
┌─────────────────────────────────────────────┐
│  User asks question + trigger phrase         │
└──────────────────────┬──────────────────────┘
                       │
          ┌────────────▼────────────┐
          │  STEP 0: PRE-FLIGHT     │
          │  Check runtime support  │
          │  & clarify unknowns     │
          └────────────┬────────────┘
                       │
          ┌────────────▼────────────┐
          │  STEP 1: INDEPENDENT    │
          │  5 parallel subagents   │
          │  give takes + evidence  │
          │  + confidence (1-10)    │
          └────────────┬────────────┘
                       │
          ┌────────────▼────────────┐
          │  STEP 2: PEER REVIEW    │
          │  Advisors critique anon │
          │  takes; defend dissent  │
          └────────────┬────────────┘
                       │
          ┌────────────▼────────────┐
          │  STEP 3: RED-TEAM &     │
          │  EVIDENCE SYNTHESIS     │
          │  Chairman weighs facts, │
          │  red-teams the winner,  │
          │  sets next action       │
          └─────────────────────────┘
```

### Why This Avoids Typical AI Flaws:
- **No Echo-Chamber / False Consensus:** A 5/5 vote is not proof. Arguments are weighed by evidence quality, not popularity.
- **Evidence Ledger:** Clearly distinguishes *verified facts* from *unstated assumptions* and *unpredictables*.
- **Pre-Flight Clarification:** If a critical variable (e.g. runway, constraints) is missing, the council asks 1 concise question instead of burning tokens hallucinating answers.
- **Red-Team Challenge:** The leading recommendation is intentionally stress-tested with failure modes before final approval.
- **Anti-Overplanning (Execution Protocol):** The output always concludes with an immediate first action (next 24 hours), review milestones, and a kill/pivot condition.

---

## Triggers

Invoke the council in chat whenever you have a hard decision or need multi-angle stress-testing:

- `JARVIS, ASSEMBLE`
- `council this`
- `assemble`
- `convene`
- `debate this`
- `war room this`
- `run the council`

---

## Installation

### For Antigravity / Claude Code

Clone or copy this repository into your agent's skills directory:

```bash
# In your project root:
mkdir -p .agents/skills/council
cp path/to/AI-Council/SKILL.md .agents/skills/council/SKILL.md
```

Or clone it directly:
```bash
git clone https://github.com/SebastianDion/AI-Council.git .agents/skills/council
```

---

## How to Tweak & Customize

Everything is defined in [`SKILL.md`](./SKILL.md):

1. **User Context / Profile:**
   - Edit the `## User context` block in `SKILL.md` to tailor advice to your background, goals, tech stack, and tendencies.
2. **Fixed Council Members:**
   - Swap Batman, Kakashi, or Tony Stark with any characters or archetypes you prefer. Keep the format with `Personality`, `Signature`, and `Flaw`.
3. **Execution Mode:**
   - Uses `flash` subagents by default for high speed and minimal cost.
   - Automatically discloses simulated execution if running inside environments without subagent tools.
4. **Trigger Phrases:**
   - Add custom keywords or your own slash commands under `## When to activate`.

---

## License

MIT
