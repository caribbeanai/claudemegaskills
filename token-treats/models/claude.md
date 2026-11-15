# Claude

Paste the block into a fresh chat or import the [skill folder](../README.md) in a Claude client that supports Agent Skills. Use the tagged template to keep pasted records distinct from instructions. [Claude prompting guide](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/overview)

~~~text
<task>[Name the deliverable, reader and decision.]</task>
<records>[Paste source text with an ID for each record.]</records>
<requirements>[Set the format, word limit and whether outside sources are allowed.]</requirements>

Check the strongest assumption and one plausible alternative. Identify the author, date and source dependence where these affect the conclusion. Cite record IDs for material claims and state what evidence would change the recommendation. Revise for plain language and return the requested deliverable.
~~~

For the controlled test, use the [canonical task and experiment](../references/experiment.md).
