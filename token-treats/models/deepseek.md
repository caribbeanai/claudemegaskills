# DeepSeek AI Vitamins

Choose a model and thinking mode before testing. Keep the model, mode, reasoning effort when available and output budget fixed across versions. In API evaluations, score the final `content` field. Follow the provider's separate rules for `reasoning_content` if your integration uses tool calls. [DeepSeek's thinking-mode guide](https://api-docs.deepseek.com/guides/thinking_mode/)

~~~text
Task: [Deliverable, reader and decision.]
Source packet: [Numbered records and source rules.]
Output requirements: [Format, length and decision constraints.]

Return the recommendation, its strongest source support and the uncertainty that could change it. Verify consequential numbers, units and denominators. Identify any claim repeated from the same underlying record. Edit once for clarity and give only the requested deliverable.
~~~

For the controlled test, use [the same four versions as the other models](../references/condition-blocks.md).
