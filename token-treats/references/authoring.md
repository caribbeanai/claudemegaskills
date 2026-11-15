# Skill and prompt authoring notes

## Keep the skill focused

The frontmatter states what the skill does and when to use it. The body gives a short review workflow. Read the case materials, experiment protocol or source notes only when the task needs them. The skill operates on the user's supplied records and requires no scripts, API keys or tools on its own. [Anthropic's skill authoring guide](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices) · [Agent Skills specification](https://agentskills.io/specification)

## Adapt prompts to the model

| Provider | Design choice | Official guidance |
| --- | --- | --- |
| Anthropic | Tag documents and task instructions. Put a long source packet before the query. | [Claude prompting best practices](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices) |
| Google | Set explicit inputs, constraints and response format. Add stable IDs when working across text and media. | [Gemini prompt design strategies](https://ai.google.dev/gemini-api/docs/prompting-strategies) |
| DeepSeek | Hold thinking settings fixed during tests and evaluate the API's final answer field. | [DeepSeek thinking mode](https://api-docs.deepseek.com/guides/thinking_mode/) |
| OpenAI | Give clear goals, delimit the records and state success criteria. Start without examples. | [OpenAI reasoning best practices](https://developers.openai.com/api/docs/guides/reasoning-best-practices) |

## Test changes on the same task

Write a rubric before comparing results. Use saved prompts, fixed settings and blind scoring. Compare the four canonical versions within each model. In a separate test, compare a provider-specific prompt with the canonical prompt on the same records. Log model, mode, prompt version and the score for each answer. Report ties, poorer answers and failed runs. The [experiment protocol](experiment.md) includes the procedure for a separate test of post-answer reward feedback.
