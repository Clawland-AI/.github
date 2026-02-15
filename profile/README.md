# Clawland

**Build the Edge AI Future. Get Paid for It.**

Clawland is an open-source ecosystem of AI Agents designed to run on hardware ranging from $2 microcontrollers to cloud servers — replacing human monitoring, maintenance, and service jobs at 1/100th the cost.

---

## The Claw Family

| Project | Language | RAM | Hardware Cost | Purpose |
|---------|----------|-----|---------------|---------|
| [**picclaw**](https://github.com/Clawland-AI/picclaw) | Go | <10MB | $10 board | Ultra-lightweight edge AI Agent |
| [**moltclaw**](https://github.com/Clawland-AI/moltclaw) | TypeScript | >1GB | Cloud / Mac Mini | Full-featured cloud AI Gateway with multi-Agent routing |
| [**nanoclaw**](https://github.com/Clawland-AI/nanoclaw) | Python | >100MB | $50 SBC | Mid-weight Agent / Regional gateway |
| [**microclaw**](https://github.com/Clawland-AI/microclaw) | C / Rust | <1MB | $2-5 MCU | Sensor-level micro Agent |

## Infrastructure

| Project | Purpose |
|---------|---------|
| [**clawland-fleet**](https://github.com/Clawland-AI/clawland-fleet) | Cloud-Edge orchestration — Fleet Manager, Edge API, Reporter, Event Hub |
| [**clawland-deploy**](https://github.com/Clawland-AI/clawland-deploy) | One-click deployment — Ansible, Docker Compose, pre-built images |
| [**clawland-dashboard**](https://github.com/Clawland-AI/clawland-dashboard) | Fleet visualization — real-time node map, alert timeline, sensor charts |

## Hardware & Skills Ecosystem

| Project | Purpose |
|---------|---------|
| [**clawland-kits**](https://github.com/Clawland-AI/clawland-kits) | Open hardware sensor kit designs — BOMs, wiring, drivers, pre-built images |
| [**clawland-skills**](https://github.com/Clawland-AI/clawland-skills) | Community skill marketplace — plug-and-play AI capabilities |
| [**clawland-drivers**](https://github.com/Clawland-AI/clawland-drivers) | Unified sensor driver library — GPIO/I2C/SPI/Serial Python drivers |

## Integrations & Tools

| Project | Purpose |
|---------|---------|
| [**clawland-homebridge**](https://github.com/Clawland-AI/clawland-homebridge) | Smart home bridge — HomeKit / Home Assistant integration |
| [**clawland-grafana**](https://github.com/Clawland-AI/clawland-grafana) | Grafana data source plugin — sensor metrics and fleet health |
| [**clawland-ai.github.io**](https://github.com/Clawland-AI/clawland-ai.github.io) | Documentation website — guides, API docs, scenario showcases |

## What Can You Build?

Deploy a **$10 board + $5 sensor + Picclaw** and replace:

- **$48,000/yr** data center night shift operator — with an $88 monitoring kit
- **$30,000/yr** fish pond patrol worker — with a $133 aquaculture guardian
- **$18,000/yr** greenhouse attendant — with a $95 smart farming kit
- **$900/yr** elderly care subscription — with a $30 safety guardian
- **$3,200/yr** predictive maintenance service — with a $32 equipment doctor

> Every scenario above is documented with full hardware BOM, wiring diagrams, implementation logic, and cost comparison. See [clawland-kits](https://github.com/Clawland-AI/clawland-kits).

## Build to Earn

Clawland is not donation-ware. **Core contributors share 20% of all product revenue** — hardware kit sales, SaaS subscriptions, and consulting income.

- Transparent quarterly payouts via [Open Collective](https://opencollective.com/Clawland-AI)
- Contribution-based scoring system (code, reviews, skills, hardware designs, docs)
- First 10 Core Maintainers get an additional 0.5% lifetime revenue share

Read the full terms: [CONTRIBUTOR-REVENUE-SHARE.md](https://github.com/Clawland-AI/.github/blob/main/CONTRIBUTOR-REVENUE-SHARE.md)

## Architecture

```
         ☁️ Cloud (moltclaw)
         ┌──────────────────────┐
         │  AI Gateway + Fleet  │
         │  Manager + Decision  │
         │  Engine + Dashboard  │
         └──────────┬───────────┘
                    │
         ═══ Internet / 4G / LoRa ═══
                    │
    ┌───────────────┼───────────────┐
    │               │               │
┌───┴───┐      ┌───┴───┐      ┌───┴───┐
│  L2   │      │  L2   │      │  L2   │  Regional
│nanoclaw│      │nanoclaw│      │nanoclaw│  Gateways
└───┬───┘      └───┬───┘      └───┬───┘  ($50 SBC)
    │               │               │
  ┌─┼─┐          ┌─┼─┐          ┌─┼─┐
  │ │ │          │ │ │          │ │ │    Edge Nodes
  ■ ■ ■          ■ ■ ■          ■ ■ ■    ($10 board)
 picclaw        picclaw        picclaw
 + sensors      + sensors      + sensors
```

## Get Involved

1. Pick a repo and look for [`good first issue`](https://github.com/search?q=org%3AClawland-AI+label%3A%22good+first+issue%22&type=issues) labels
2. Read our [Contributing Guide](https://github.com/Clawland-AI/.github/blob/main/CONTRIBUTING.md)
3. Join the conversation in [GitHub Discussions](https://github.com/orgs/Clawland-AI/discussions)
4. Check the [Bounty Board](https://github.com/orgs/Clawland-AI/projects/1) for paid tasks

## Governance

Clawland is governed by a Technical Steering Committee (TSC). Major decisions go through an RFC process. See [GOVERNANCE.md](https://github.com/Clawland-AI/.github/blob/main/GOVERNANCE.md).

## License

| Layer | License |
|-------|---------|
| Core agents (picclaw, moltclaw, nanoclaw, microclaw) | **Apache 2.0** |
| Cloud orchestration (clawland-fleet, clawland-dashboard) | **BSL 1.1** → Apache 2.0 after 4 years |
| Hardware designs (clawland-kits) | **CERN-OHL-S-2.0** |
| Skills & integrations (clawland-skills, clawland-homebridge) | **MIT** |
| Sensor drivers (clawland-drivers, clawland-grafana) | **Apache 2.0** |
| Documentation (clawland-ai.github.io) | **CC BY-SA 4.0** |

---

*"Let $10 hardware + AI Agents do the watching, so humans can do the thinking."*
