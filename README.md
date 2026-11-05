# PMF Strategy

A Codex skill for turning product ideas, customer research, and usage data into a coherent product-market fit strategy and a clear next decision.

Use it to write PMF narratives, assess whether a specific customer segment shows evidence of PMF, identify risky assumptions, design validation experiments, and plan early traction or a first growth loop.

## What it does

| Workflow | What you get |
|---|---|
| PMF narrative | A connected strategy covering problem, target audience, value proposition, competitive advantage, growth strategy, and business model. |
| PMF assessment | A segment-level verdict grounded in retention, engagement, acquisition, and economics, with evidence gaps made explicit. |
| Risk validation | Prioritized assumptions and a practical experiment with success, failure, and inconclusive criteria. |
| Customer interviews | Recruiting guidance, interview questions, or a synthesis of findings across segments. |
| Traction and growth | A stage-appropriate acquisition plan or a specific growth loop with its economics, prerequisites, and bottleneck. |

It supports both new products and expansion into new customer segments. It separates observed evidence from hypotheses and treats benchmarks as heuristics rather than automatic proof of PMF.

## Install in Codex

This repository is private. Your GitHub account needs read access to `Starttech-Labs/pmf-strategy`.

### Ask Codex to install it

Use this prompt in Codex, with GitHub credentials available in its environment:

```text
$skill-installer Install the skill from https://github.com/Starttech-Labs/pmf-strategy.
The skill is at the repository root (path .); install it with the name pmf-strategy.
```

### Manual installation

For macOS/Linux with Git and GitHub CLI installed, authenticate with an account that has repository access:

```sh
gh auth login
```

Skip login if you are already authenticated with the correct account. Install for your user:

```sh
mkdir -p "$HOME/.agents/skills"
gh repo clone Starttech-Labs/pmf-strategy "$HOME/.agents/skills/pmf-strategy"
```

Alternatively, install only for a project by running this from its root:

```sh
mkdir -p .agents/skills
gh repo clone Starttech-Labs/pmf-strategy .agents/skills/pmf-strategy
```

Choose one scope. If the destination already contains an installation, update that installation instead of cloning over it. The project option creates a nested Git checkout; it does not automatically commit the skill into the parent repository.

Codex discovers local skills automatically. In the CLI or IDE extension, use `/skills` or type `$pmf-strategy` to select it. If it does not appear, restart Codex. See the [official skills documentation](https://learn.chatgpt.com/docs/build-skills) for discovery paths and invocation details.

Keep the entire folder: `SKILL.md` relies on the bundled references. No package installation, API key, or original course document is required by the skill itself.

## Usage examples

Paste a prompt into Codex and provide the referenced product context or files.

**Draft a narrative from an idea**

```text
$pmf-strategy Write a PMF narrative for a scheduling product for independent
physiotherapy clinics. We are pre-launch. Separate hypotheses from evidence,
choose a Now audience, and identify the assumption we should validate first.
```

**Review an existing strategy**

```text
$pmf-strategy Review our attached PMF narrative. Find contradictions across
our audience, pricing, value proposition, and growth strategy. Suggest concrete
revisions and explain what evidence would justify them.
```

**Assess PMF from evidence**

```text
$pmf-strategy Assess PMF using these cohort-retention exports, monthly new-user
counts, acquisition costs, and interview notes. Compare customer segments,
state data limitations, and recommend whether to improve retention or scale.
```

**Design the next experiment**

```text
$pmf-strategy Our biggest uncertainty is whether clinic owners will pay
€99/month. Design the smallest credible test, including recruitment,
observable commitment, success/failure criteria, and what each outcome changes.
```

**Prepare interviews**

```text
$pmf-strategy Create a PMF interview guide for clinic owners and receptionists.
Test our audience assumptions and all six narrative dimensions. Start with
unaided questions before introducing our proposed benefits.
```

**Choose a growth loop**

```text
$pmf-strategy We have promising retention among small clinics but rely on
founder outreach. Evaluate model-channel and product-channel fit, then propose
one growth loop and a test of its weakest assumption. Label missing inputs.
```

## What to provide

Start with your product, stage, intended audience, business model, and the decision you need to make. Add research notes, competing alternatives, pricing hypotheses, or metrics where available. For metrics, include definitions, cohort sizes, dates, and segment labels.

Sparse input is fine for a hypothesis draft. A confident PMF assessment requires actual evidence; interviews, positive feedback, and signup spikes alone do not establish PMF. The skill does not automatically connect to your analytics or run external experiments.

## Updating

For the manual user installation above:

```sh
git -C "$HOME/.agents/skills/pmf-strategy" pull --ff-only
```

For a project installation, use `.agents/skills/pmf-strategy` instead. If you installed through `$skill-installer`, ask Codex to update the existing installation from this repository while preserving any local edits; it may be a downloaded copy rather than a Git checkout.

## Contents and approach

- [SKILL.md](SKILL.md): workflow selection and shared evidence rules.
- [Narrative](references/narrative.md): six strategy dimensions and coherence checks.
- [Assessment](references/assessment.md): retention, growth, engagement, economics, and verdicts.
- [Validation](references/validation.md): risk prioritization, interviews, and experiments.
- [Growth](references/growth.md): early traction and repeatable growth loops.
- [Codex metadata](agents/openai.yaml): display name and default prompt.

Synthesized from a supplied Reforge / Sachin Rekhi Finding Product/Market Fit course document, using the Deliberate Startup approach: define, validate, measure, and develop traction in parallel. The original document is not included. The references add practical evidence labels, experiment briefs, and measurement safeguards; they are not verbatim course templates.
