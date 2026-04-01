<p align="center">
  <img src="https://coachleo.ai/icon.png" alt="Coach Leo" width="120" />
</p>

<h1 align="center">Coach Leo — AI Running Coach</h1>

<p align="center">
  <strong>An AI running coach that connects to your Strava, builds training plans from your real data, and adapts daily based on how you actually feel.</strong><br/>
  Available as a web app, on Telegram, and as an MCP server for ChatGPT, Claude, and Mistral. Every recommendation draws from 65+ peer-reviewed sports science papers.
</p>

<p align="center">
  <a href="https://coachleo.ai">Try it free</a> ·
  <a href="https://coachleo.ai/en/about">About</a> ·
  <a href="https://coachleo.ai/en/docs">MCP Documentation</a> ·
  <a href="https://smithery.ai/servers/coachleo/running-coach">Smithery</a>
</p>

---

## What is Coach Leo?

Coach Leo is a full AI running coach application at [coachleo.ai](https://coachleo.ai). It connects to your Strava account, reads your real training history (pace, heart rate, elevation, cadence), and uses 12 specialized coaching tools to make decisions — like a real coach with access to your training diary.

Leo is not a chatbot that generates generic plans from what you type. He deduces your training patterns from Strava, derives your actual paces from 8 weeks of data, and adapts your plan daily through conversation.

### How to get started

1. Create an account at [coachleo.ai](https://coachleo.ai) (7-day free trial)
2. Connect your Strava account (read-only)
3. Start chatting — Leo already knows your training

---

## What makes Leo different

### Strava-first coaching
Leo never asks "what's your weekly mileage?" — he already knows. Strava syncs every 30 minutes. When you open a conversation, Leo has already analyzed your last 10 activities, your training load, your acute-to-chronic workload ratio (ACWR), and your weekly patterns.

### Plans built from YOUR actual paces
Leo derives your easy, tempo, interval, and long-run paces from 8 weeks of real Strava data. No generic templates. Your Zone 2 pace comes from YOUR heart rate and pace distributions.

### Plans that fit your life
Hard constraints are enforced, not just preferences. "I can only run Tuesday, Thursday, and Sunday", "maximum 40km per week", "no intervals" — Leo respects these in every plan. When your schedule changes, Leo restructures through conversation while keeping it coherent with your race goal.

### Multi-indicator overtraining prevention
Leo never relies on a single metric. He cross-references ACWR trends, volume increase speed, rest days, subjective fatigue, recurring body signal patterns, and plan adherence. Response is graduated: observation, session modification, week restructuring, professional referral.

### Biomechanical shoe wear analysis
Not just mileage tracking. Leo inspects 6 wear zones (outsole, lateral midsole, medial midsole, upper, heel, insole) with visual scoring. Wear patterns reveal biomechanical signals — pronounced medial wear suggests overpronation, which feeds back into body signal tracking.

### Race preparation with web search
Say "I'm doing the UTMB CCC" and Leo searches the web for real race data: date, distance, elevation, terrain, participants, GPX file. No manual entry. Leo then analyzes the GPX profile and predicts your finish time using 4 models (VDOT, Riegel, Cameron, Tanda).

### Sports nutrition guidance
Evidence-based race fueling adapted to your weight, duration, elevation, and gut tolerance. IOC/ISSN guidelines. Recovery nutrition timing and carb periodization. Per-session nutrition plans included.

### Scientific knowledge base
65+ peer-reviewed papers with hybrid semantic search (BM25 + pgvector). Covers training methodology, overtraining prevention, trail-specific training, biomechanics, nutrition, psychology, and cross-training.

### Persistent coaching memory
Leo searches past history before advising. He references specific conversations: "Last week you reported calf tightness and your ACWR was 1.4 — volume is up 30%, let's be cautious." After 3 months, Leo has a coaching dossier no new app can replicate.

### VO2max and race time predictions
VO2max from 3 methods (ACSM, Jack Daniels VDOT, HR-Pace regression) cross-validated with confidence intervals. Race time predictions using 4 models with personal Riegel exponent. Trail-adjusted estimates that account for elevation.

### Running character system
9 animal archetypes (Wolf, Mountain Goat, Turtle, Phoenix, Hawk, Bear, Fox, Cheetah, Otter) computed from 9 real training dimensions — not a personality quiz. Calculated from your Strava data. Evolves through 3 stages. Your character shapes how Leo coaches you.

### Cross-training as strategic lever
Cycling, swimming, hiking, skiing — each session gets a specific role: recovery, aerobic development, muscular reinforcement, or injury prevention. Integrated into weekly training load.

---

## Available everywhere

| Channel | Description |
|---------|-------------|
| **Web app** | Full chat interface with training dashboard, character visualization, race countdown, and performance metrics at [coachleo.ai](https://coachleo.ai) |
| **Telegram** | Message Leo directly for quick coaching on the go. Same memory, same tools, same coach. |
| **ChatGPT, Claude, Mistral** | Connect Leo as an MCP server. Your favorite AI assistant becomes your running coach with full access to your data. |

---

## Community (coming soon)

- **Packs** — Your character determines your pack. Join runners worldwide who share your training DNA.
- **Solo quests** — Personal challenges tied to your training dimensions.
- **Pack battles** — Weekly and seasonal competitions between packs.
- **Expeditions** — Run together across iconic routes worldwide. Every kilometer counts.

---

## Activity tracking

Coach Leo syncs **all your Strava activities** — running is the primary coaching focus (road, trail, track), but every other sport you log (cycling, swimming, CrossFit, hiking, skiing, etc.) is tracked with a specific role to give the coach a complete picture of your training load and recovery needs.

---

## Pricing

- **Founding member**: $9.99/month (limited spots, locked for life)
- **Regular**: $12.99/month
- **7-day free trial** included — no charge if you cancel before it ends
- All features included. No tiers, no feature gates.

---

## MCP Server (for developers)

Coach Leo also works as a **hosted remote MCP server** — no installation required. Connect it to any MCP-compatible client (ChatGPT, Claude Desktop, Cursor, Windsurf, and more).

### Quick setup

1. Open your MCP client's settings
2. Add a new remote server: `https://mcp.coachleo.ai/mcp`
3. Authenticate with your Coach Leo account
4. Start chatting — 12 coaching tools are ready

### JSON config

```json
{
  "mcpServers": {
    "coach-leo": {
      "url": "https://mcp.coachleo.ai/mcp"
    }
  }
}
```

### 12 coaching tools

| Tool | Description |
|------|-------------|
| `get_coaching_briefing` | Complete coaching context: profile, recent activities, training load, alerts, readiness, character status. |
| `manage_athlete` | Runner profile and running character management. Body metrics, preferences, character recalculation. |
| `manage_activities` | Query and annotate Strava-synced activities. Filter by date, sport, impact. Record feedback. |
| `manage_training` | Create and manage personalized training plans. Modify sessions, track adherence. |
| `track_body_signals` | Log body observations, record physical setbacks, daily readiness check-ins. |
| `manage_shoes` | Track shoe collection, wear inspections across 6 zones, mileage stats, and retirement. |
| `manage_races` | Full race lifecycle: discovery via web search, registration, preparation, results, post-race analysis. |
| `search_knowledge` | Hybrid semantic + full-text search across 65+ peer-reviewed papers. |
| `coaching_memory` | Persistent memory across sessions. Logs decisions, prevents contradictory advice. |
| `estimate_vo2max` | VO2max estimation using 3 scientific methods with cross-validation. |
| `calculate_training_zones` | Pace and HR zones (Z1-Z5) from race performance or physiological data. |
| `analyze_gpx` | GPX file analysis: elevation profiles, terrain segmentation, diversity scoring. |

### 11 coaching workflows

Predefined workflows that chain tools together for complex scenarios:

- **Onboarding** — Strava-first setup: Leo deduces your patterns before asking anything
- **Post-activity analysis** — Automated debrief with shoe deduction and sensation logging
- **Body signal analysis** — Injury risk assessment backed by knowledge base citations
- **Overtraining monitoring** — Multi-indicator load analysis with graduated alerts
- **Weekly review** — Training summary with character recalculation and plan adjustments
- **Adaptive plan creation** — Plans from real paces with constraint validation
- **Race planning** — Web search for race data, GPX analysis, taper protocol
- **Deep research** — Knowledge base enrichment from web search
- **GPX pattern analysis** — Terrain and elevation profiling for race preparation
- **Shoe wear assessment** — 6-zone inspection with biomechanical pattern detection
- **Character reveal** — Running character assignment ceremony

### Authentication

Full OAuth 2.1 implementation:

- Discovery: `/.well-known/oauth-authorization-server`
- Dynamic Client Registration (DCR)
- PKCE with S256
- Token refresh and revocation

---

## Privacy & data

- Hosted in **Finland** (Hetzner, EU)
- HTTPS/TLS encryption
- Strava data is **read-only**
- Strict user data isolation
- GDPR compliant — export and deletion on request
- No data used for AI model training

---

## Links

- [Website](https://coachleo.ai)
- [About](https://coachleo.ai/en/about)
- [MCP Documentation](https://coachleo.ai/en/docs)
- [Smithery](https://smithery.ai/servers/coachleo/running-coach)
- Contact: contact@coachleo.ai

---

<p align="center">Made in the Alps.</p>
