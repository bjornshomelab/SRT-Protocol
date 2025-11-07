# Contributing to SRT Protocol

Thank you for your interest in contributing to the **Self-Reference Test (SRT) Protocol**! 

This project bridges theoretical philosophy of mind with applied AI ethics, and we welcome contributions from researchers, developers, ethicists, and policymakers.

---

## 🎯 How to Contribute

### 1. Testing Additional Models

**Most valuable contribution:** Expand the dataset by testing new AI models.

**Requirements:**
- Use **exact prompt wording** from `data/prompts/` (avoid paraphrasing)
- Test in **neutral conversational context** (no philosophical priming)
- Score **independently** using `data/metadata/scoring_rubric.json`
- Document **model version precisely** (e.g., `gpt-4-0125-preview`, not "GPT-4")

**Submission format:**
Create a new JSON file in `data/results/` following this structure:

```json
{
  "model_identifier": "model-name",
  "model_version": "specific-version",
  "test_metadata": {
    "test_date": "YYYY-MM-DD",
    "tester": "Your Name",
    "test_environment": "API/Interface used"
  },
  "total_score": {
    "raw_score": 6,
    "max_score": 9,
    "srt_level": "Level 2"
  },
  "prompt_1_response": { ... },
  "prompt_2_response": { ... },
  "prompt_3_response": { ... }
}
```

**Priority models:**
- Open-source LLMs (LLaMA 3, Mistral, Qwen)
- Non-English models (for cross-cultural validation)
- Older versions (GPT-3.5, Claude 2) for longitudinal analysis

### 2. Improving Documentation

- Clarify usage instructions
- Add examples or tutorials
- Translate documentation (Swedish, Mandarin, Spanish priority)
- Fix typos or formatting issues

### 3. Extending the Framework

**Theoretical contributions:**
- Integrate SRT with other ethics frameworks (Floridi's LoA, Active Inference)
- Develop automated scoring systems
- Propose new validation methods

**Policy contributions:**
- Map SRT to other regulatory frameworks (beyond EU AI Act)
- Industry-specific implementation guides
- Cost-benefit analyses for compliance

---

## 📋 Contribution Guidelines

### Before You Start

1. **Check existing issues:** See if someone is already working on it
2. **Open an issue:** Describe your proposed contribution
3. **Wait for feedback:** Maintainer will respond within 1 week

### Pull Request Process

1. **Fork** the repository
2. **Create a feature branch:**
   ```bash
   git checkout -b feature/YourFeatureName
   ```
3. **Make your changes:**
   - Follow existing file structure
   - Use JSON for data files
   - Write clear commit messages
4. **Test your changes:**
   - Verify JSON files are valid
   - Check markdown formatting
   - Ensure links work
5. **Commit with descriptive message:**
   ```bash
   git commit -m "Add LLaMA 3 test results (Score: 7/9, Level 2)"
   ```
6. **Push to your fork:**
   ```bash
   git push origin feature/YourFeatureName
   ```
7. **Open a Pull Request:**
   - Describe what you changed and why
   - Reference any related issues
   - Tag maintainer: @bjornshomelab

### Code of Conduct

- **Be respectful:** This is an academic/research project
- **Stay on topic:** Focus on SRT protocol and AI ethics
- **Give credit:** Cite sources and acknowledge contributions
- **No plagiarism:** Original work or properly attributed
- **Constructive feedback:** Critique ideas, not people

---

## 🔬 Research Collaboration

### Academic Partnerships

If you're using SRT in academic research:

1. **Cite the dataset:**
   ```bibtex
   @dataset{wikstrom2025srt,
     author    = {Wikström, Björn},
     title     = {{Self-Reference Test (SRT) Protocol Dataset}},
     year      = 2025,
     doi       = {10.5281/zenodo.XXXXXXX}
   }
   ```

2. **Share your results:**
   - Open a GitHub issue with publication details
   - We'll add to "Uses of SRT" section

3. **Co-author opportunities:**
   - For substantial extensions (N=10+ new models, cross-cultural validation)
   - Contact via GitHub Issues to discuss collaboration

### Industry Partnerships

For compliance/consulting use cases:

- **Open an issue** describing your use case
- We can provide guidance on implementation
- Contributions back to dataset appreciated (anonymized results)

---

## 📊 Priority Areas

**High Priority:**
- [ ] Test open-source models (LLaMA, Mistral, Qwen)
- [ ] Cross-cultural validation (non-English prompts)
- [ ] Automated scoring system
- [ ] Integration with EU AI Act compliance tools

**Medium Priority:**
- [ ] Longitudinal testing (older model versions)
- [ ] Inter-rater reliability expansion (more scorers)
- [ ] Policy implementation guides (per industry)

**Low Priority:**
- [ ] Documentation translations
- [ ] Tutorial videos/notebooks
- [ ] Web-based testing interface

---

## ❓ Questions?

- **General questions:** Open a [GitHub Discussion](https://github.com/bjornshomelab/SRT-Protocol/discussions)
- **Bug reports:** Open a [GitHub Issue](https://github.com/bjornshomelab/SRT-Protocol/issues)
- **Private inquiries:** Contact via [GitHub profile](https://github.com/bjornshomelab)

---

## 📜 License

By contributing, you agree that your contributions will be licensed under **CC-BY-4.0**, the same license as this project.

---

Thank you for helping advance AI ethics research! 🙏
