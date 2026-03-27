<p align="center">
  <img src="https://coachleo.ai/logo.png" alt="Coach Leo" width="120" />
</p>

<h1 align="center">Coach Leo — AI Running Coach</h1>

<p align="center">
  <strong>A remote MCP server that turns any AI assistant into your personal running coach.</strong><br/>
  Syncs your real training data from Strava, builds personalized training plans, manages your race calendar, tracks body signals and shoes, and assigns you a running character. Every recommendation draws from 65+ peer-reviewed sports science papers.
</p>

<p align="center">
  <a href="https://coachleo.ai">Website</a> ·
  <a href="https://coachleo.ai/en/docs">Documentation</a> ·
  <a href="https://smithery.ai/servers/coachleo/running-coach">Smithery</a>
</p>

---

## Connect

Coach Leo is a **hosted remote MCP server** — no installation required. Works with any MCP-compatible client (Claude, Cursor, Windsurf, and more).

### Quick setup

1. Open your MCP client's settings
2. Add a new remote server
3. Enter: `https://mcp.coachleo.ai/mcp`
4. Authenticate with your Coach Leo account
5. Start chatting — your tools are ready

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

### Requirements

- Coach Leo account (7-day free trial)
- Connected Strava account

---

## Tools

| Tool | Description |
|------|-------------|
| `get_coaching_briefing` | Complete coaching context: profile, recent activities, training load, alerts, readiness, character status. Called at the start of every conversation. |
| `manage_athlete` | Runner profile and running character management. Update body metrics, preferences, and trigger character recalculation. |
| `manage_activities` | Query and annotate Strava-synced activities. Filter by date, sport, impact. Record post-workout feedback. |
| `manage_training` | Create and manage personalized training plans. Modify sessions, track adherence. |
| `track_body_signals` | Log body observations, record physical setbacks, daily readiness check-ins. Severity levels from info to alert. |
| `manage_shoes` | Track shoe collection, wear inspections, mileage stats, and retirement. |
| `manage_races` | Full race lifecycle: discovery, registration, preparation, results, post-race analysis. |
| `search_knowledge` | Hybrid semantic + full-text search across 65+ peer-reviewed papers on training methodology, injury prevention, nutrition, psychology, and more. |
| `coaching_memory` | Persistent memory across sessions. Logs decisions, searches history, prevents contradictory advice. |
| `estimate_vo2max` | VO2max estimation using ACSM, Jack Daniels VDOT, and HR-Pace methods. |
| `calculate_training_zones` | Pace and HR zones (Z1-Z5) from race performance or physiological data. |
| `analyze_gpx` | GPX file analysis: elevation profiles, terrain segmentation, diversity scoring. |

---

## Coaching Workflows

11 predefined workflows that chain tools together for complex scenarios:

- **Onboarding** — New runner setup with Strava sync and character assignment
- **Post-activity analysis** — Automated debrief after each run
- **Body signal analysis** — Injury risk assessment and recovery guidance
- **Overtraining monitoring** — Load trend analysis with alert triggers
- **Weekly review** — Training week summary with plan adjustments
- **Adaptive plan creation** — Science-backed periodized plans
- **Race planning** — From goal race selection to taper strategy
- **Deep research** — Knowledge base deep dives on specific topics
- **GPX pattern analysis** — Terrain and elevation profiling
- **Shoe wear assessment** — Rotation and retirement recommendations
- **Character reveal** — Running character assignment ceremony

---

## Running Character

Every runner is assigned one of 9 animal characters based on their real training data:

**Wolf** · **Mountain Goat** · **Turtle** · **Phoenix** · **Hawk** · **Bear** · **Fox** · **Cheetah** · **Otter**

Your character evolves as your training evolves. It shapes how the coach talks to you and what it prioritizes in your coaching.

---

## Community (coming soon)

- **Packs** — Join your animal pack and contribute to collective goals
- **Expeditions** — Run together across iconic routes worldwide
- **Pack challenges** — Weekly and seasonal inter-pack competitions
- **Real-world impact** — Kilometers that matter beyond your training

---

## Activity Tracking

Coach Leo syncs **all your Strava activities** — running is the primary coaching focus (road, trail, track), but every other sport you log (cycling, swimming, CrossFit, hiking, football, etc.) is tracked to give the coach a complete picture of your training load and recovery needs.

---

## Authentication

Full OAuth 2.1 implementation:

- Discovery: `/.well-known/oauth-authorization-server`
- Dynamic Client Registration (DCR)
- PKCE with S256
- Token refresh and revocation

---

## Privacy & Data

- Hosted in **Germany** (Hetzner, EU)
- HTTPS/TLS encryption
- Strava data is **read-only**
- Strict user data isolation
- GDPR compliant — export and deletion on request
- No data used for AI model training

---

## Links

- [Website](https://coachleo.ai)
- [Documentation](https://coachleo.ai/en/docs)
- [Smithery](https://smithery.ai/servers/coachleo/running-coach)
- Contact: contact@coachleo.ai

---

<p align="center">Made in the Alps.</p>
