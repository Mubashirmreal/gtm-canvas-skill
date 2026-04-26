# GTM Canvas Agent Skill

An agent skill that transforms any AI assistant into an interactive **GTM Canvas facilitator** — walking users through all 8 components of the GTM Canvas framework and producing a complete, actionable go-to-market strategy.

---

## Directory Structure

```
gtm-canvas-sk/
├── SKILL.md                          ← Main skill entrypoint (load this into your agent)
├── knowledge/
│   ├── gtm-canvas-template.md        ← Official GTM Canvas v1.5 blank template
│   └── gtm-canvas-handbook.md        ← Official GTM Canvas Handbook (authoritative reference)
├── examples/
│   └── sample_session.md             ← Complete example facilitation session
└── resources/
    ├── gtm_channel_guide.md          ← Deep-dive on all channel types
    └── pre_launch_checklist.md       ← Expanded pre-launch checklist with tools
```

---

## Quick Start by Framework

### Claude (Anthropic Projects)
1. Create a new Project in [claude.ai](https://claude.ai)
2. Copy the full contents of `SKILL.md` into **Project Instructions**
3. Upload `knowledge/gtm-canvas-template.md` and `knowledge/gtm-canvas-handbook.md` as **Project Knowledge** files
4. Start a conversation — Claude will immediately be in GTM facilitator mode

### OpenAI Custom GPT
1. Go to [chat.openai.com/gpts](https://chat.openai.com/gpts) → Create
2. Paste `SKILL.md` contents into the **Instructions** field
3. Upload all files from `knowledge/` and `examples/` as **Knowledge** files
4. Set the name to "GTM Canvas Facilitator"

### Cursor / Windsurf / Continue.dev
```
# Option A — project-level (affects this repo only)
cp -r gtm-canvas-sk/ .agent/skills/gtm-canvas/

# Option B — global (affects all projects)
cp -r gtm-canvas-sk/ ~/.continues/skills/gtm-canvas/   # Continue.dev
```
Then reference it in your agent config or rules file.

### Raw API (OpenAI-compatible)
```python
import openai, pathlib

skill = pathlib.Path("SKILL.md").read_text()
handbook = pathlib.Path("knowledge/gtm-canvas-handbook.md").read_text()

response = openai.chat.completions.create(
    model="gpt-4o",
    messages=[
        {"role": "system", "content": f"{skill}\n\n---\n\n{handbook}"},
        {"role": "user",   "content": "I want to build a GTM strategy for my product."}
    ]
)
```

### LangChain / LlamaIndex
- Load `SKILL.md` as the system prompt
- Load `knowledge/` files into a `VectorStoreIndex` for retrieval
- Use `trigger_phrases` from `SKILL.md` frontmatter for intent routing

### Dify / Flowise / n8n
- Import `knowledge/gtm-canvas-handbook.md` as a Knowledge Base document
- Paste `SKILL.md` content into the Agent's System Prompt node

---

## The 8 GTM Canvas Components

| # | Component | Core Question |
|---|-----------|---------------|
| 1 | Primary Feature | What do users come for and would miss most? |
| 2 | Primary Sellable Feature | What do they actually pay for? |
| 3 | Differentiator | How do you win the comparison war? |
| 4 | Alpha (Unfair Advantage) | What can competitors never replicate? |
| 5 | Handpick Users | Who are the first 100 real humans you'll onboard? |
| 6 | Profiling | What does a typical user look like? |
| 7 | Source | Where do they live online and offline? |
| 8 | Medium / Channel | How will you reach them? |

---
