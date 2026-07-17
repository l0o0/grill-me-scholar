English | [简体中文](docs/README.zh-CN.md)

# Grill Me Scholar

An adaptive academic interview skill that helps researchers turn an unclear interest into one focused, feasible, and evidence-aware research topic.

Many research projects begin before the researcher has a precise question. A broad interest is not yet a research topic, and a topic is not ready merely because it sounds novel. Grill Me Scholar narrows the problem through a one-question-at-a-time interview while keeping consequential choices with the researcher.

## Why It Exists

Generic topic-generation prompts often produce a list of polished titles too early. They may silently choose a population or method, overlook access and ethics constraints, or repeat an unverified claim as a "research gap."

Grill Me Scholar is designed to slow that moment down. It keeps uncertainty visible and works toward shared understanding before confirming a direction.

## Core Features

- **One decision at a time:** active interview turns ask one non-compound question.
- **Adaptive entry:** starts differently for no direction, a broad field, or an existing candidate topic.
- **Researcher-owned choices:** offers frameworks and recommendations without silently choosing scope, method, or values.
- **Evidence discipline:** labels claims as `verified`, `user-provided`, or `needs verification`.
- **Academic viability checks:** examines concepts, evidence, methods, resources, access, ethics, contribution, and counterarguments.
- **Cross-disciplinary lenses:** adapts its checks for humanities, social sciences, science and engineering, health, and design or practice research.
- **Explicit completion gate:** produces a final Research Topic Card only after the topic is coherent, feasible, qualified, and confirmed by the researcher.

## Installation

### Install with `npx skills`

```bash
npx skills add l0o0/grill-me-scholar --skill=grill-me-scholar
```

### Manual project installation

```bash
git clone git@github.com:l0o0/grill-me-scholar.git
mkdir -p /path/to/project/.agents/skills
cp -R grill-me-scholar/.agents/skills/grill-me-scholar /path/to/project/.agents/skills/
```

### Manual personal installation for Codex

```bash
mkdir -p ~/.agents/skills
cp -R grill-me-scholar/.agents/skills/grill-me-scholar ~/.agents/skills/
```

Skill discovery paths can vary across Agent Skills-compatible tools. Use the path expected by your client when it differs from the examples above.

## Quick Start

English:

```text
Use $grill-me-scholar to help me narrow and validate my research topic.
```

中文：

```text
使用 $grill-me-scholar 帮我收窄并验证研究主题。
```

You can begin with no topic, a broad area, or a candidate question. You can also ask the skill to pause, go back, explain why a question matters, or produce a provisional result.

## Example Interview

> **Researcher:** I want to study how social media affects university students.
>
> **Grill Me Scholar:** "Affects" could refer to several different outcomes. Which single outcome matters most to you?
>
> **Researcher:** Student anxiety.
>
> **Grill Me Scholar:** Anxiety is now the tentative outcome, but the research aim is still ambiguous. Do you want to examine an association or understand students' experiences?
>
> **Researcher:** I think nobody has studied short-form video and anxiety, so that is my gap.
>
> **Grill Me Scholar:** That is a `user-provided` claim and remains `needs verification`; it is not yet a defensible gap. What literature-search evidence currently supports it?

The interview continues until the object, scope, evidence, method, constraints, ethics, and contribution are sufficiently clear. It does not force every session through a fixed number of questions.

## Research Topic Card

After final confirmation, the skill produces a structured card containing:

```text
Working title
One-sentence topic
Primary research question and necessary subquestions
Research object, scope, and key concepts
Motivation and potential contribution
Tentative relationship to prior work
Suggested methodological path
Required materials, data, and conditions
Feasibility and ethical risks
Verified evidence and sources
Assumptions needing verification
Smallest next action
Alternative directions and reasons not selected
```

If the topic cannot yet converge, the skill reports the best current candidate, the blocking uncertainty, and the smallest validation task instead of inventing certainty.

## Disciplinary Lenses

The core interview is shared, but the checks adapt to the field:

- **Humanities:** sources, context, interpretive framework, and corpus boundaries.
- **Social sciences:** concepts, mechanisms, cases, variables, data access, inference, and participant ethics.
- **Science and engineering:** systems, hypotheses, measurement, controls, uncertainty, safety, and reproducibility.
- **Medicine and health:** population, exposure or intervention, outcomes, bias, privacy, access, and ethics review.
- **Design and practice research:** setting, stakeholders, artifact or intervention, participation, and evaluation criteria.
- **Interdisciplinary research:** each field's theoretical, methodological, evidential, or contextual role, including conflicting assumptions about evidence.

## How It Works

The skill tracks the developing topic across interest, phenomenon, object, scope, evidence, method, resources, ethics, contribution, and commitment. Each dimension can remain unknown, become tentative or confirmed, require verification, or conflict with another decision.

The next question targets the uncertainty most likely to change or invalidate the topic. If a later constraint breaks an earlier plan—for example, inaccessible data or an ethics timeline—the interview goes back and redesigns the path while preserving the motivating question where possible.

A claim is `verified` only when an inspected reliable source directly supports that specific claim and a traceable locator is recorded. A resolving DOI by itself is not enough.

## Scope and Limitations

Grill Me Scholar helps form and stress-test a research topic. It does not:

- write a complete research proposal;
- guarantee that a topic or gap is novel;
- replace a systematic literature review;
- replace a supervisor, domain expert, statistician, or methodologist;
- grant data access, participant consent, or ethics approval;
- make the researcher's interests, values, or resource commitments for them.

Its output is only as reliable as the information and evidence available during the interview. Important factual claims should still be checked against appropriate scholarly sources and institutional requirements.

## Acknowledgements

Grill Me Scholar is inspired by Matt Pocock's [`grill-me`](https://github.com/mattpocock/skills/tree/main/skills/productivity/grill-me) and [`grilling`](https://github.com/mattpocock/skills/tree/main/skills/productivity/grilling) skills, especially their one-question-at-a-time interview pattern. This project adapts that pattern for academic topic formation and is not an official or endorsed derivative.
