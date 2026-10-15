# Think First · 先想一步

A question-first AI collaboration skill: form your own judgment, choose what help you need, then proceed one step at a time. No learning-outcome improvement has been measured.

## Use

In a skill-compatible environment, install this folder as `think-first` and invoke `$think-first`.

For ChatGPT, paste [CHATGPT-INSTRUCTIONS.md](CHATGPT-INSTRUCTIONS.md) into Settings → Personalization → Custom Instructions, preserving existing preferences. Publishing SKILL.md on GitHub does not automatically configure ChatGPT. Project instructions can override global instructions; add the same preference to relevant projects if needed. These are model instructions, not guaranteed enforcement.

## Example

See the illustrative exchange in [SKILL.md](SKILL.md). The assistant asks about the user's observation, initial idea and desired help, then waits. Say “直接回答” to bypass questioning for one request, or “恢复先问后答” to restore it.

## Validation

Validated frontmatter using skill-creator quick_validate.py. Manual instruction review covers new-task questions, continuation without repeated intake, scaffolding when stuck, direct-answer override, and urgent-help exception. This is not a live model reliability test or learning study.

## Official references

- [ChatGPT Custom Instructions](https://help.openai.com/en/articles/8096356-chatgpt-custom-instructions)
- [Project instruction scope](https://help.openai.com/en/articles/10169521-projects-in-chatgpt)
