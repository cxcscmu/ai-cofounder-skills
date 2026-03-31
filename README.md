# AI Cofounder Skills

A Claude Code plugin containing all prompts from [CMU 11-787: AI as a Cofounder](https://www.cs.cmu.edu/~11787-AI-Cofounder/), packaged as reusable skills.

## Table of Contents

- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Skills Reference](#skills-reference)
- [License](#license)
- [Contact](#contact)

## Requirements

- [Claude Code](https://claude.ai/code) CLI

## Installation

Clone this repo, then load it as a plugin when starting Claude Code:

```bash
claude --plugin-dir /path/to/cofounder-skills
```

## Usage

Once loaded, invoke any skill with the `/cofounder-skills:<skill-name>` command. For example:

```
/cofounder-skills:five-whys
/cofounder-skills:icp
/cofounder-skills:budget-builder
```

Each skill will prompt you for the required inputs (company name, product description, etc.) and then generate a structured output.

## Skills Reference

### Module 1: Founder Advantage Analysis

| Skill | Description |
|-------|-------------|
| `prompt-example-full` | Interviews you across 6 dimensions (lived experience, conviction, mission, expertise, greed, luck) with 5 questions each to identify your real asymmetric advantages as a founder. |
| `prompt-example-short` | Short version — asks one key question per dimension for a quicker founder advantage assessment. |

### Module 2: Competitive Research

| Skill | Description |
|-------|-------------|
| `comp-research` | Maps competitive terrain across direct, indirect, and analogue competitors with evidence-backed dossiers, threat-vs-noise matrix, and strategic watch-list. |
| `comp-research-multi-step` | Advanced multi-step competitive intelligence covering 14 competitor types, critical strategic artifacts, deep research pass, and scenario playbooks. |
| `comp-research-build-advantage` | Extracts technical advantage vectors from prior competitive intelligence with citations, scoring, and composable open-source stacks. |

### Module 3: Customer Discovery

| Skill | Description |
|-------|-------------|
| `five-whys` | Guided 5 Whys root cause analysis with evidence-backed reasoning. Reframes your problem, conducts deep causal analysis, and recommends actions. |
| `icp` | Generates a detailed, evidence-backed Ideal Customer Profile with demographics, psychographics, personas, decision journey, and scoring rubric. |
| `anti-icp` | Generates an Anti-Ideal Customer Profile to help avoid marketing and product investments in poor-fit audiences that seem attractive. |

### Module 4: Landing Pages

| Skill | Description |
|-------|-------------|
| `landing-page-guru` | Creates a complete landing page strategy with page structure, CTAs, visual design direction, trust signals, and a ready-to-paste generator prompt. |

### Module 5: AI Tool Stack

| Skill | Description |
|-------|-------------|
| `ai-recruiter` | Assembles your AI cofounder tool stack — diagnoses founder gaps, recommends tools, builds a 14-day execution plan and weekly operating system. |

### Module 6: Finance & Pricing

| Skill | Description |
|-------|-------------|
| `budget-builder` | Generates a realistic, investor-credible operating budget from 5 inputs — with hiring plans, revenue projections, sensitivity analysis, and fundraising recommendations. |
| `consumption-based-pricing` | Single-input consumption pricing CFO that infers cost drivers, estimates COGS using current model pricing, runs scenario comparisons, and recommends pricing. |

### Module 7: Market Sizing & Differentiation

| Skill | Description |
|-------|-------------|
| `market-size-tam` | Calculates Total Addressable Market based on existing spending (not hypothetical demand) with stress testing and classification. |
| `differentiators` | Pressure tests whether a company has clear, defensible, evidence-backed differentiation against competitors. |

### Module 8: Demand Generation

| Skill | Description |
|-------|-------------|
| `example-data-sources` | Reference list of 100 data sources organized by category (financial, demographic, competitive, economic, behavioral, risk, regulatory, disruptions). |
| `example-media-artifacts` | Reference library of 180+ media artifact formats for demand generation (interactive, video, audio, static, written, social, emerging). |
| `demand-gen-creative-matrix` | Combines How Might We statements with data sources and media artifacts to produce actionable demand generation concepts with a prioritized execution roadmap. |

### Module 9: Legal & Term Sheets

| Skill | Description |
|-------|-------------|
| `legal-b2b` | Generates B2B software legal document outlines (MSA, NDA, DPA, SLA, etc.), precision drafting prompts, and cross-document risk checks. Not legal advice. |
| `legal-b2c` | Generates B2C consumer-facing legal document outlines with privacy compliance, trust optimization, and risk checks. Not legal advice. |
| `term-sheet-eval` | Deconstructs term sheets clause-by-clause, scores founder-friendliness, and provides tactical negotiation playbooks. Not legal advice. |
| `term-sheet-example` | Example term sheet (Eraser Robotics pre-seed convertible note) for practice with the `term-sheet-eval` skill. |

### Module 10: Storytelling & Presentation

| Skill | Description |
|-------|-------------|
| `poster-generator` | Generates demo day poster concepts, layouts, visual direction, headlines, and image generation prompts for a 2x3ft startup poster. |
| `ten-minute-stories` | Generates 10 different 10-minute story arc outlines across styles (Hero's Journey, Origin Story, David vs Goliath, and more) with scoring and recommendations. |

## License

For use by CMU 11-787 students and staff.

## Contact
Cathy Jiao: cljiao@cs.cmu.edu