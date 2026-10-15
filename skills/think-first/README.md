# Think First · 先想一步

A question-first collaboration skill that helps the user choose how to use AI before receiving an answer. It is a workflow preference, not evidence of improved learning outcomes.

## Use

In a skill-compatible environment, install this folder as `think-first` and invoke `$think-first`.

For ChatGPT, paste [CHATGPT-INSTRUCTIONS.md](CHATGPT-INSTRUCTIONS.md) into Settings → Personalization → Custom Instructions, preserving other existing preferences. Uploading SKILL.md or publishing it on GitHub alone does not configure ChatGPT. Project instructions can override global custom instructions; add the same preference to relevant project instructions when needed. This is model guidance, not a guaranteed enforcement mechanism.

## Interaction example (illustrative)

User: Help me design a campus wayfinding system.

Assistant: What specific navigation problem have you observed? What direction would you try first? Would you like questions or a small hint?

The assistant waits for the user; it does not append a complete design proposal. The user may say “直接回答” to skip the questioning for that request.

## Validation

The skill frontmatter was validated with skill-creator quick_validate.py. A manual instruction review checked new-task questioning, avoiding repeated questions, support when the user is stuck, explicit direct-answer override and urgent-help exception. These are instruction checks, not a measured user study or an end-to-end model reliability test.

## Official setup references

- [ChatGPT Custom Instructions](https://help.openai.com/en/articles/8096356-chatgpt-custom-instructions)
- [Project instructions and their scope](https://help.openai.com/en/articles/10169521-projects-in-chatgpt)
