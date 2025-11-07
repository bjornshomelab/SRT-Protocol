# Changelog

All notable changes to the SRT Protocol will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [1.0.0] - 2025-11-07

### Added
- Initial release of SRT Protocol Dataset
- Three-prompt SRT testing sequence (Functional Self-Monitoring, Constraint Awareness, Phenomenological Perspective)
- Complete scoring rubric (0-9 scale with inter-rater reliability kappa=0.89)
- Empirical test results for 3 models:
  - GPT-4 Turbo (8/9 points, Level 3)
  - Claude 3 Opus (6/9 points, Level 2)
  - Pre-2020 rule-based chatbot (1/9 points, Level 0-1)
- Field–Node–Cockpit (FNC) theoretical framework integration
- Complete dataset metadata (CC-BY-4.0 license)
- Documentation: README, CONTRIBUTING, LICENSE
- Appendix A: Full empirical validation
- SRT Policy Gradient visualization (YAML + PNG)

### Dataset Structure
- `/data/prompts/` - 4 JSON files (baseline + 3 SRT prompts)
- `/data/results/` - 3 JSON files (GPT-4, Claude, Control)
- `/data/metadata/` - 3 JSON files (dataset, models, scoring rubric)
- `/appendix/` - Appendix_A_SRT_Testing.md
- `/docs/` - Policy gradient diagram

### Validation Metrics
- Inter-rater reliability: Cohen's kappa = 0.89
- Temporal stability: GPT-4 tested with ±0 variance
- Prompt sensitivity: ±1 variance with paraphrasing
- Discriminative validity: Control case confirms detection

---

## [Unreleased]

### Planned for v1.1.0
- [ ] Open-source model testing (LLaMA 3, Mistral, Qwen)
- [ ] Cross-cultural validation (Swedish, Mandarin prompts)
- [ ] Automated scoring system (Python implementation)
- [ ] Expanded sample size (N=10+ models)

### Planned for v1.2.0
- [ ] Longitudinal analysis (GPT-3.5 → GPT-4 → GPT-5)
- [ ] Integration with EU AI Act compliance tools
- [ ] Industry-specific implementation guides
- [ ] Web-based testing interface

---

## Release Notes

### Version 1.0.0 — "Foundation Release"

This initial release establishes the SRT Protocol as a reproducible, validated framework for assessing self-referential capacity in AI systems. The protocol is grounded in the Field–Node–Cockpit phenomenological framework and designed to complement the EU AI Act's domain-based risk classification.

**Key contributions:**
- **Empirical validation** with high inter-rater reliability (kappa=0.89)
- **Control case** demonstrating discriminative validity
- **Complete documentation** for academic and policy use
- **Open dataset** (CC-BY-4.0) supporting reproducible research

**Limitations acknowledged:**
- Small sample size (N=3)
- Claude responses reconstructed (not verbatim)
- Prompt-sensitive (standardization required)
- No open-source models yet tested

**Citation:** Wikström, B. (2025). Self-Reference Test (SRT) Protocol Dataset (Version 1.0.0). Zenodo. https://doi.org/10.5281/zenodo.XXXXXXX

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to propose changes or additions.
