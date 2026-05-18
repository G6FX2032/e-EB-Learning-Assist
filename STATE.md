# STATE.md — education-agent-skills

**Last updated:** 2026-05-18 (Session 6)

## What was done

Added 2 orchestrator skills in original-frameworks:

1. **original-frameworks/assessment-design-orchestrator** — Routes teachers between five assessment design pathways: formative assessment, rubric/criteria design, authentic/performance assessment, peer and self-assessment, and diagnostic/pre-assessment. Enforces a pathway-first approach (present options before routing). Integrates Messick (1989) validity check at every pathway and a UDL-informed equity check for format barriers. Explicit do-not-proceed-if gates: no rubric without exemplars, no peer assessment without training students, no assessment before learning goals are clear. Evidence sources include Black & Wiliam (1998), Wiliam (2011), Wiggins (1998), Sadler (1989), Hattie & Timperley (2007), Messick (1989), Topping (2009), Zimmerman (2002), Manning (2023-2026). evidence_strength: emerging.

2. **original-frameworks/inclusive-design-orchestrator** — Coordinates UDL and differentiation tools through a three-tier universal-first hierarchy: universal design before targeted differentiation before individualised accommodation. Routes between four pathways: proactive barrier removal, existing plan audit, targeted differentiation, and assessment accessibility. Includes explicit specialist referral flags (for needs requiring educational psychology, speech-language therapy, occupational therapy), a tokenism check (modifications must address actual identified barriers), and an honest warning that inclusive design is necessary but not sufficient for genuine inclusion. Evidence sources: Rose & Meyer (2002), CAST (2018), Meyer Rose & Gordon (2014), Ok Rao Bryant & McDougall (2017), Tomlinson (2001), Gay (2010), Manning (2023-2026). evidence_strength: emerging.

Both orchestrators carry full composite-framework evidence governance: Evidence Space, Component Evidence, Synthesis Evidence, What This Skill Should Not Claim, Appropriate Use, and Dependency Maintenance sections.

Also:
- CI workflow updated: 145 → 147
- CLAUDE.md updated: 147 skills
- README badge and description updated: 147 skills

## What was verified

- Both description fields verified ≤250 characters via Python: 207 and 202 chars
- All chains_well_with targets confirmed to exist on disk before writing
- `python3 scripts/validate-skills.py`: 147 skills, 0 errors, 4 pre-existing warnings (line-length on unrelated skills)
- `python3 scripts/validate-registry.py`: 147 skills, 19 domains — valid
- `npx playwright test`: 20/20 pass
- `cd mcp-server && npm run build && npm test`: 16/16 pass
- Committed and pushed: b88d3b8

## Chain targets verified

Assessment Design Orchestrator:
- formative-assessment-technique-selector ✓
- assessment-validity-checker ✓
- gap-analysis-from-student-work ✓
- differentiation-adapter ✓
- self-regulation-scaffold-generator ✓
- inclusive-design-orchestrator ✓ (created this session)
- udl-barrier-anticipator ✓

Inclusive Design Orchestrator:
- udl-lesson-auditor ✓
- udl-options-designer ✓
- udl-barrier-anticipator ✓
- differentiation-adapter ✓
- assessment-design-orchestrator ✓ (created this session)
- language-demand-analyser ✓
- scaffolded-task-modifier ✓

## What's next

- Systems-thinking orchestrator: systems-thinking domain now has 7 skills (iceberg, aspirational iceberg, mental model mapper, ladder of inference, agency circles, leverage-response design, wellbeing impact mapper). A composite orchestrator linking these into a full inquiry arc is the logical next step (separate from the existing compassionate-systems-awareness-orchestrator which covers a subset).
- Perspective-taking designer (questioning-discussion) has natural cross-domain chains with historical-thinking — worth formalising.
- The assessment-design-orchestrator and inclusive-design-orchestrator now cross-chain with each other, making a combined "accessible assessment design" flow possible as a future composite skill.
