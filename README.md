# AI-Council 🏛️

A multi-agent decision support skill for Claude Code, Antigravity, and AI coding assistants. Inspired by PewDiePie's AI Council and the Diverse Multi-Agent Debate (DMAD) framework.

Instead of getting a single generic AI opinion, **AI-Council** convenes a panel of 5 independent advisors who debate, peer-review each other blind, and synthesize an actionable verdict.

---

## The Council Roster

| Seat | Member | Archetype | Core Focus |
|---|---|---|---|
| 1 | **🦇 Batman** | Chief Strategist & Devil's Advocate | Risk management, worst-case scenarios, contingency planning |
| 2 | **📖 Kakashi Hatake** | Chief Learning Officer & Mentor | Sustainable growth, mental adaptability, long-term mastery |
| 3 | **⚡ Tony Stark** | CTO & Opportunity Hunter | Execution, prototypes, leverage, bias-to-action |
| 4 | **🎯 Domain Specialist** | Rotating Expert | Dynamically chosen based on topic (finance, tech, career, etc.) |
| 5 | **👀 The Outsider** | Deliberate Naive Observer | Asks simple/critical questions, cuts through jargon & groupthink |

---

## How It Works

```
┌─────────────────────────────────────────────┐
│  User asks question + trigger phrase         │
└──────────────────────┬──────────────────────┘
                       │
          ┌────────────▼────────────┐
          │  PHASE 1: INDEPENDENT   │
          │  5 parallel subagents   │
          │  give uncontaminated    │
          │  perspectives           │
          └────────────┬────────────┘
                       │
          ┌────────────▼────────────┐
          │  PHASE 2: PEER REVIEW   │
          │  Each advisor critiques │
          │  the other 4 takes      │
          │  blindly/anonymously    │
          └────────────┬────────────┘
                       │
          ┌────────────▼────────────┐
          │  PHASE 3: CHAIRMAN      │
          │  Main agent synthesizes │
          │  verdict + vote tally   │
          └─────────────────────────┘
```

1. **Phase 1 (Independent Takes):** 5 parallel subagents analyze the question without seeing each other's responses.
2. **Phase 2 (Blind Peer Review):** Advisors inspect anonymized arguments from the other 4 seats and revise or defend their stances.
3. **Phase 3 (Chairman Synthesis):** The main agent reports the verdict, consensus/dissent vote tally, key tension points, and collapsed summaries.

---

## Triggers

Invoke the council in chat whenever you have a hard decision or want multiple angles:

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

Everything is defined in [`SKILL.md`](./SKILL.md). You can customize:

1. **User Context / Profile:**
   - Edit the `## User context` block in `SKILL.md` to tailor advice to your background, goals, tech stack, and tendencies.
2. **Fixed Council Members:**
   - Swap Batman, Kakashi, or Tony Stark with any characters or archetypes you prefer. Keep the format with `Personality`, `Signature`, and `Flaw to role-play`.
3. **Subagent Models:**
   - Defaults to `flash` for fast, lightweight advisor responses. Can be switched to `inherit` or `pro` for deeper analysis.
4. **Trigger Phrases:**
   - Add custom keywords or your own slash commands under `## When to activate`.

---

## License

MIT
