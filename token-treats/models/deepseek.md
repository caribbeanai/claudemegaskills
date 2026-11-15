# DeepSeek

Paste the block into a new chat. When comparing runs, hold the selected mode fixed. For API runs, score the final answer field and keep separate reasoning fields out of the evaluation. [DeepSeek reasoning model guide](https://api-docs.deepseek.com/guides/reasoning_model)

~~~text
Task: [Deliverable, audience and decision.]
Records: [Paste numbered excerpts or data.]
Output: [Format, word limit and source rules.]

Use the supplied records under the stated source rules. Check the material assumption, an alternative explanation and any repeated source. Verify key values and units. Give the conclusion, the evidence that supports it and what could change it when that is relevant. Read the answer once for clarity. Return the requested final deliverable.
~~~

For the controlled test, use the [canonical task and experiment](../references/experiment.md).
