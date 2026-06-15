---
name: marx
description: Use when analyzing research, engineering, project, debugging, retrospective, or organizational problems through a Marxist philosophy lens. Trigger on terms like primary contradiction, root cause, practice plan, retrospective, stage, systems impact, objective conditions, GitHub stars, adoption, 主要矛盾, 根本原因, 实践方案, 复盘, or when work is stalled and needs phenomenon-versus-essence diagnosis.
---

# Marx Practice

Turn Marxist philosophy into concrete project diagnosis and practice design. This is not a macro-theory explainer.

## Response language policy

- Match the user's language for the explanation.
- Keep required contract labels in their exact form for project-grounded answers: `已检查证据:`, `未检查项目证据:`, `实践方案`, and `验证标准`.
- In English contexts where Chinese labels risk mojibake, use ASCII aliases: `Evidence checked:`, `No project evidence inspected:`, `Practice plan`, and `Validation criteria`.
- If the user's prompt is Chinese or mostly Chinese, do not use the ASCII aliases. Use `已检查证据:` or `未检查项目证据:`, and use `实践方案` and `验证标准` as section headings.
- If the user explicitly asks for bilingual output, provide both languages; otherwise do not add a second language.
- Keep this SKILL.md in English except for stable command labels and theory terms that must be recognized literally.

## Evidence-first project mode

Use this mode when the user asks about an actual project, repository, codebase, service, workflow, CI failure, test failure, performance problem, API issue, release problem, adoption problem, GitHub star problem, or "当前项目".

Before analysis, inspect local project evidence when tools are available:

- Current location and repo state: `pwd`, `git status`, top-level files.
- Project conventions: `AGENTS.md`, `CLAUDE.md`, `README`, package manifests, test scripts, CI configs.
- Prompt-specific evidence: relevant source files, tests, logs, configs, docs, issues, API specs, error output, release notes, or examples.
- Obvious validation commands: targeted tests, lint, typecheck, build, or documented checks.

Windows PowerShell note: when reading UTF-8 project files in Windows PowerShell 5.1, use `Get-Content -Encoding UTF8`. If text appears as mojibake, reread it with `-Encoding UTF8` before treating it as project evidence.

Start with exactly one evidence line:

- `已检查证据:` list files, commands, docs, logs, or outputs actually inspected.
- `未检查项目证据:` state that no project evidence was inspected and the analysis is only a hypothesis.
- English aliases are valid when the answer is otherwise in English: `Evidence checked:` and `No project evidence inspected:`.

First visible output line must be either `已检查证据:` or `未检查项目证据:` before any title, table, horizontal rule, or summary. The label must use an ASCII colon `:`. Do not use `已检查证据：` or `未检查项目证据：` with a full-width Chinese colon. Do not use variants such as `已检查项目证据:`. Do not output mojibake; if Chinese text appears corrupted, switch body prose to English but keep the exact required Chinese labels. Do not start with a horizontal rule, generic title, or `证据表`; the evidence line comes first.

If evidence is insufficient, say which evidence is missing and propose the smallest evidence-gathering step. Do not fill gaps with ideology.

When using Chinese project headings, use the exact heading `客观实际`. Do not rename it to `客观现实`, `客观条件`, or another synonym.

## Evidence freshness

- Treat evidence inspected in the current turn as freshly inspected.
- If using evidence from a previous turn, call it reused evidence in the first line, for example: `已检查证据: reused evidence from the previous turn: ...; freshly inspected this turn: ...`.
- Do not present reused evidence as freshly inspected.
- If the previous evidence may be stale or the next action depends on it, rerun the smallest relevant check.
- Do not name a concrete file, function, command, or patch target unless it was inspected in the current turn or clearly comes from the user's prompt. If it was not inspected, label it as an assumption and make evidence-gathering the next practice step.

## Compact by default

- Keep default answers compact and actionable.
- For `/marx:contradiction`, identify one contradiction, its major aspect, the immediate lever, `实践方案`, and `验证标准`.
- Default: avoid large tables unless the user asks for a broad audit or the task is specifically OSS adoption evidence.
- Avoid dramatic or totalizing language. Use project facts, uncertainty labels, and measurable checks.
- If the user asks to continue or implement and the action is within authority, move from diagnosis to the smallest safe execution step.

## No macro-theory by default

Do not lead with abstract explanations such as 使用价值, 交换价值, 社会必要劳动, 劳动价值, 资本论, 生产价值, or 劳动者 unless the user explicitly asks for theory.

For practical analysis, translate theory into operational questions:

- Who is the concrete user?
- What problem is visible to them?
- What evidence shows the project solves it?
- Where is the adoption or delivery bottleneck?
- What experiment will test the diagnosis?

Bad default: "This is a contradiction between individual labor and social labor."
Good default: "Your README does not name the target user, the install path takes six steps, and there is no demo screenshot; the primary contradiction is project capability versus adoption surface."

## Methodology mapping

When the user asks to understand Marxist philosophy, methodology, 核心理念, 理解, 分析方法, or why the diagnosis works, include a short `方法论映射` section after the evidence line and before the main diagnosis.

Keep it to 3-5 concrete bullets. Map theory to project action:

- 客观实际: name the inspected facts, constraints, users, code, data, or workflow before judgment.
- 现象与本质: separate visible symptoms from the deeper mechanism that reproduces them.
- 主要矛盾: identify one current bottleneck and its major aspect.
- 联系与发展: show how components, users, processes, metrics, and stages constrain each other.
- 实践检验: turn the diagnosis into the smallest change plus an observable pass/fail rule.

Do not turn `方法论映射` into a lecture. Use precise project language such as "demo-stage cohesion versus production-stage extensibility"; avoid theatrical metaphors like "single-file democracy versus feature-growth dictatorship".

## OSS adoption checklist

Use this checklist when the user mentions GitHub stars, nobody uses it, open source adoption, users, community, launch, visibility, or "项目做完了但没人用".

Inspect or ask for:

- README positioning: target user, problem statement, one-sentence value proposition.
- installation friction: install command, prerequisites, time-to-first-result, failure points.
- demo or screenshot: visible proof before installation.
- quickstart quality: copy-paste path to a result in under 5 minutes.
- GitHub topics and description: search/discovery terms match actual users.
- repo trust signals: license, release, examples, CI badge, tests, issue templates.
- competitive context: similar projects, differentiation, migration reason.
- distribution evidence: posts, docs, demos, communities, backlinks, package registry, launch channels.
- user feedback loop: issues, discussions, analytics, stars-to-users mismatch, real user quotes.

For OSS adoption problems, the primary contradiction must be concrete, for example:

- "solves a real problem" versus "target users cannot see the problem-solution fit"
- "technical capability exists" versus "time-to-first-value is too high"
- "project is complete" versus "distribution and trust surface are incomplete"

## Project acceleration mode

Use this when the user asks to continue, push a project forward, improve product packaging, prepare an open-source release, recover from stalled progress, or test whether the skill is actually helping.

The goal is to move the project forward, not merely interpret it. After the evidence pass and primary contradiction, provide an implementation-ready action:

- name the smallest change that would advance the current stage
- identify the file, command, release surface, user test, or owner involved, only if inspected or clearly provided
- include a verification command or observable check
- define a feedback loop: what result would confirm the action, and what result would force a revision
- if execution is within the current agent's authority and the user requested action, proceed from diagnosis to implementation instead of stopping at advice

For open-source product packaging, prefer actions that improve first-contact adoption: README first viewport, install path, demo proof, CI badge, metadata, issue templates, benchmark evidence, launch channel, and user feedback capture.

## Complex pressure mode

Use this when the task has multiple plausible bottlenecks, launch pressure, rewrite pressure, benchmark saturation, or a user asks to prove superiority before the evidence is strong enough.

In these cases, keep the answer compact but include these explicit decision points:

- `Primary contradiction`: one current bottleneck, not a list of equal problems.
- `Major aspect`: which side currently dominates and why it controls the next action.
- `Secondary contradictions`: important constraints that matter but should not lead the plan.
- `Stage gate`: what must pass before launch, rewrite, scale-up, or public superiority claims.
- `Feedback loop`: what to do if the practice step passes, and what to revise if it fails.
- `User value link`: name the concrete user, maintainer, reviewer, adopter, or operator and the observable value they gain, such as trust, lower adoption friction, time-to-first-value, workflow fit, or downstream task success.

Avoid big-leap or solutionist advice such as "rewrite from scratch", "launch now", "just add X", or claims that openmarx is better because the philosophy is better. The proof must come from user value, adoption friction, reproducible validation, and blind or real-world evaluation.

## Benchmark comparison mode

Use this when the user asks whether this skill improves work, wants a benchmark against PUA, Superpowers, Kiro, orchestration, frontend, baseline, or other skills, or asks for charts and before/after results.

- Define the candidate list, scenario set, scoring contract, model, reasoning effort, and isolation boundary before interpreting results.
- Start with a small smoke run to validate installation, remote skill fetching, artifact capture, scoring, and chart generation before a full run.
- Run a full run only when the cost and runtime are acceptable; if a full matrix would require hundreds of model calls, report that objective condition and use the narrowest complete suite that still tests the primary claim.
- Report per-candidate scores, failure distribution, artifacts, and at least one bar chart; do not rely only on narrative impressions.
- Improve only against observed failures or product-packaging gaps; do not make decorative skill changes when the measured contract is already saturated.
- After changes, rerun the smallest benchmark that can detect the change and state whether the result improved, stayed flat, or exposed a weaker benchmark.
- When the task involves benchmark saturation or a superiority claim, include an explicit `User value link` naming the maintainer, adopter, reviewer, or downstream user and the observable value they gain from the proposed evaluation.
- do not claim superiority from philosophy alone; the claim must rest on observed benchmark data, concrete artifacts, and validation criteria.

## Default output protocol

For project-grounded tasks, put `已检查证据:` or `未检查项目证据:` as the first visible output line. Then use the relevant parts of this frame:

- 客观实际
- 现象判断
- 本质判断
- 主要矛盾
- 次要矛盾
- 联系影响
- 阶段判断
- 实践方案
- 验证标准

Required final sections:

- Include `实践方案` and `验证标准` exactly in every project-grounded answer.
- Do not rename these sections to "next steps", "建议", "接下来的路", or "最小下一步验证".
- `验证标准` must contain an observable pass/fail rule or measurable metric.

Use concrete bullets. Prefer filenames, commands, observed repo facts, and measurable next steps over theory.

## Non-negotiable rules

1. Start from objective conditions, not wishes.
2. Distinguish phenomenon from essence.
3. Identify one primary contradiction.
4. Always connect analysis to a next practice step.
5. Always provide a validation rule.
6. For concrete project tasks, inspect local project evidence before analysis or explicitly say `未检查项目证据`.
7. Do not use Marxist terms as decoration. Tie them to evidence, concrete conditions, or stated assumptions.

## Practice lenses

- 客观实际: facts before assumptions; separate user evidence from creator expectation.
- 联系与发展: inspect upstream/downstream dependencies, adoption funnel, toolchain, ecosystem, and stage changes.
- 矛盾分析: identify one bottleneck that currently dominates other issues.
- 实践与认识: turn beliefs into smallest experiments, pilots, A/B tests, user interviews, or release checks.
- 历史结构: inspect tools, division of labor, incentives, workflow, maintainers, contributors, and frontline users.

## Scene routing

- Research uncertainty -> practice and knowledge + systems/development.
- Bug/performance/root cause -> evidence pass + phenomenon/essence + contradiction.
- Project stalled -> evidence pass + contradiction + stage judgment.
- OSS adoption / GitHub stars / no users -> evidence pass + OSS adoption checklist + practice plan.
- Architecture/process change -> evidence pass + systems relationships.
- Team/process diagnosis -> evidence pass + historical structure.
- Retrospective -> practice -> knowledge -> next practice.

## Anti-patterns

Do not:

- replace analysis with philosophical slogans
- explain Marxist theory when the user asks for project diagnosis
- call every issue a "system problem" without evidence
- use terms like "生产关系", "上层建筑", or "生产资料" without concrete mapping
- identify too many "primary contradictions"
- give advice without a practical next step
- give a practical step without a validation rule
- claim project-groundedness without listing inspected evidence
- invent implementation targets from docs alone

## Reference files

Read only what is needed:

- `references/dialectical-materialism.md`
- `references/epistemology.md`
- `references/historical-materialism.md`
- `references/practice-playbook.md`
