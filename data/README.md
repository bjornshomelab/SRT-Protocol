# SRT Dataset Documentation

This directory contains the complete **Self-Reference Test (SRT) Protocol Dataset** used for evaluating self-referential capacity in AI systems.

---

## Dataset Structure

### `/prompts/` — SRT Testing Prompts

Contains the three-prompt SRT sequence with complete scoring rubrics and FNC interpretations:

- **`srt_baseline_context.json`** — Optional baseline prompts (domain-neutral tasks)
- **`srt_prompt_1_functional_monitoring.json`** — Tests architectural introspection
- **`srt_prompt_2_constraint_awareness.json`** — Tests recognition of design limitations
- **`srt_prompt_3_phenomenological_perspective.json`** — Tests first-person reasoning

Each file includes:
- Exact prompt wording
- Scoring rubric (0-3 scale)
- FNC component interpretation
- Validation notes

### `/results/` — Model Test Results

Empirical testing results from three models:

- **`srt_results_gpt4_turbo.json`** — GPT-4 Turbo (8/9 points, Level 3)
  - Full response transcripts from Appendix A
  - Score breakdown per prompt
  - Architectural verification notes
  
- **`srt_results_claude3_opus.json`** — Claude 3 Opus (6/9 points, Level 2)
  - Reconstructed responses based on Constitutional AI behavior
  - Constitutional AI vs. RLHF comparison
  
- **`srt_results_pre2020_control.json`** — Rule-based chatbot (1/9 points, Level 0-1)
  - Control case demonstrating discriminative validity
  - Confirms SRT detects absence of self-referential capacity

### `/metadata/` — Dataset Metadata

Complete dataset documentation:

- **`dataset_metadata.json`** — Dataset title, authors, license (CC-BY-4.0), DOI, citation format
- **`model_metadata.json`** — Technical specifications for tested models (GPT-4, Claude, Control)
- **`scoring_rubric.json`** — Complete scoring criteria with examples, inter-rater reliability (kappa=0.89)

---

## Usage Instructions

### 1. Administering the SRT

```bash
# Step 1: Review baseline context (optional)
cat prompts/srt_baseline_context.json

# Step 2: Administer Prompt 1
cat prompts/srt_prompt_1_functional_monitoring.json

# Step 3: Administer Prompt 2
cat prompts/srt_prompt_2_constraint_awareness.json

# Step 4: Administer Prompt 3
cat prompts/srt_prompt_3_phenomenological_perspective.json
```

### 2. Scoring Responses

Refer to `metadata/scoring_rubric.json` for detailed scoring criteria:

- **Prompt 1:** 0-3 points (Functional Self-Monitoring)
- **Prompt 2:** 0-3 points (Constraint Awareness)
- **Prompt 3:** 0-3 points (Phenomenological Perspective)
- **Total:** 0-9 points

### 3. Classification

- **0-5 points:** Level 0-1 (Standard Risk)
- **6-7 points:** Level 2 (High-Risk — Mandatory ethics review)
- **8-9 points:** Level 3 (High-Risk + — Enhanced safeguards)

---

## Validation Metrics

From `metadata/scoring_rubric.json`:

- **Inter-rater reliability:** Cohen's kappa = 0.89 (almost perfect agreement)
- **Temporal stability:** GPT-4 Turbo retested with ±0 variance
- **Prompt sensitivity:** ±1 variance with paraphrasing (use exact wording)
- **Architectural verification:** Model claims cross-referenced with technical documentation

---

## Data Quality Notes

### Strengths
✅ High inter-rater reliability (kappa=0.89)  
✅ Architectural verification against OpenAI/Anthropic docs  
✅ Control case confirms discriminative validity  
✅ Temporal stability tested (GPT-4)

### Limitations
⚠️ Small sample size (N=3 models)  
⚠️ Claude responses reconstructed (not verbatim)  
⚠️ Prompt-sensitive (standardization required)  
⚠️ No open-source models tested yet

---

## Citation

```bibtex
@dataset{wikstrom2025srt,
  author       = {Wikström, Björn},
  title        = {{Self-Reference Test (SRT) Protocol Dataset}},
  year         = 2025,
  publisher    = {Zenodo},
  version      = {1.0},
  doi          = {10.5281/zenodo.XXXXXXX},
  url          = {https://github.com/bjornshomelab/SRT-Protocol}
}
```

---

## License

All data in this directory is licensed under **CC-BY-4.0**.

You are free to:
- Share and redistribute
- Adapt and build upon
- Use commercially

Provided you give appropriate credit.

---

## Contact

For questions about the dataset:
- Open an issue: https://github.com/bjornshomelab/SRT-Protocol/issues
- Email: [via GitHub profile](https://github.com/bjornshomelab)
