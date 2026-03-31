I am currently TA-ing this class: https://www.cs.cmu.edu/~11787-AI-Cofounder/. I have been instructed with: 
 
1. Auto convert our course prompts into skills.
2. Release them to the class in skill containers

I have never worked with skill container before. You can see in the "prompts" folder all the prompts used in the class so far. You do not need to read all the prompts yet. You can read one as an example.

Can you propose a plan to convert the prompts to skills and place them in skill containers? Can you write the plan below?

---

## Plan

### Overview

We have 22 `.docx` prompt files used in CMU 11-787 AI Cofounder. We will:
1. Convert each prompt into a Claude Code **skill** (a `SKILL.md` file with YAML frontmatter + markdown instructions)
2. Package all skills into a single **skill container** (plugin) that students can install

### Plugin Structure

```
cofounder-skills/
├── .claude-plugin/
│   └── plugin.json            # Plugin manifest (name, description, version, author)
├── skills/
│   ├── prompt-example-full/
│   │   └── SKILL.md
│   ├── prompt-example-short/
│   │   └── SKILL.md
│   ├── comp-research/
│   │   └── SKILL.md
│   ├── comp-research-multi-step/
│   │   └── SKILL.md
│   ├── comp-research-build-advantage/
│   │   └── SKILL.md
│   ├── five-whys/
│   │   └── SKILL.md
│   ├── icp/
│   │   └── SKILL.md
│   ├── anti-icp/
│   │   └── SKILL.md
│   ├── landing-page-guru/
│   │   └── SKILL.md
│   ├── ai-recruiter/
│   │   └── SKILL.md
│   ├── budget-builder/
│   │   └── SKILL.md
│   ├── consumption-based-pricing/
│   │   └── SKILL.md
│   ├── market-size-tam/
│   │   └── SKILL.md
│   ├── differentiators/
│   │   └── SKILL.md
│   ├── example-data-sources/
│   │   └── SKILL.md
│   ├── example-media-artifacts/
│   │   └── SKILL.md
│   ├── demand-gen-creative-matrix/
│   │   └── SKILL.md
│   ├── legal-b2b/
│   │   └── SKILL.md
│   ├── legal-b2c/
│   │   └── SKILL.md
│   ├── term-sheet-eval/
│   │   └── SKILL.md
│   ├── term-sheet-example/
│   │   └── SKILL.md
│   ├── poster-generator/
│   │   └── SKILL.md
│   └── ten-minute-stories/
│       └── SKILL.md
├── prompts/                   # Original .docx files (kept for reference)
│   └── ...
└── plan.md                    # This file
```

### Step-by-step Process

**Step 1: Create the plugin manifest**
- Create `.claude-plugin/plugin.json` with name `"cofounder-skills"`, description, version, and author info.

**Step 2: Convert each .docx prompt to a skill**
For each of the 22 prompts:
1. Read the `.docx` file using `pandoc`
2. Create a `skills/<skill-name>/SKILL.md` with:
   - **YAML frontmatter**: `name`, `description` (concise summary of what the skill does, max 250 chars)
   - **Markdown body**: The prompt content, cleaned up from docx formatting artifacts (e.g. `\[Insert...\]` placeholders kept as-is since they are part of the interactive prompt)
3. Key decisions per skill:
   - `disable-model-invocation: true` — students should invoke these manually via `/cofounder-skills:<skill-name>`
   - No special `allowed-tools` unless the prompt requires web search or file I/O

**Step 3: Test the plugin locally**
- Run `claude --plugin-dir ./` and verify skills appear with `/help`
- Test a few skills to confirm they work as expected

**Step 4: Distribute to the class**
- Push the plugin to a GitHub repo
- Students install via: `/plugin install` pointing to the repo, or by cloning and using `claude --plugin-dir`

### Naming Convention

| Prompt File | Skill Name |
|---|---|
| 1.1.1 Prompt Example (Full Length).docx | prompt-example-full |
| 1.1.2 Prompt Example (Short Class Demo).docx | prompt-example-short |
| 2.1 Comp Research.docx | comp-research |
| 2.2 Comp Research multi step.docx | comp-research-multi-step |
| 2.3 Comp Research Build Advantage.docx | comp-research-build-advantage |
| 3.1 5 Whys.docx | five-whys |
| 3.2 ICP.docx | icp |
| 3.3 Anti ICP.docx | anti-icp |
| 4.1 Landing Page Guru.docx | landing-page-guru |
| 5.1 AI Recruiter.docx | ai-recruiter |
| 6.1 Budget Builder.docx | budget-builder |
| 6.2 Consumption Based Pricing.docx | consumption-based-pricing |
| 7.1 Market Size - TAM.docx | market-size-tam |
| 7.2 Differentiators.docx | differentiators |
| 8.2 Example Data Sources to Ingest.docx | example-data-sources |
| 8.3 Example Media and Artifacts.docx | example-media-artifacts |
| 8.4 Demand Gen - Creative Matrix.docx | demand-gen-creative-matrix |
| 9.1 Legal AI B2B - Not a Lawyer.docx | legal-b2b |
| 9.2 B2C Legal - Not a Lawyer.docx | legal-b2c |
| 9.3 Term Sheet Eval.docx | term-sheet-eval |
| 9.4 Term Sheet Example.docx | term-sheet-example |
| 10.1 Poster Generator.docx | poster-generator |
| 10.2 10 Minute Stories.docx | ten-minute-stories |