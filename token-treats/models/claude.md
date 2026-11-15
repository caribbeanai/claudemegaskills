# Claude AI Vitamins

Use the [skill folder](../README.md) in a client that supports Agent Skills, or paste the prompt into a normal chat. Use one `<document>` per source. For long packets, put the documents before the task. Where an exact phrase decides the issue, ask for a brief quotation with its source ID. [Anthropic's prompting guidance](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices)

~~~text
<documents>
  <document>
    <source>[Document ID and date]</source>
    <content>[Paste the relevant document text.]</content>
  </document>
</documents>

<task>[Deliverable, audience and decision.]</task>
<constraints>[Format, length and whether external sources are allowed.]</constraints>

Test the key assumption and a plausible alternative. Trace repeated claims to their original document. For each claim the decision depends on, give the source ID and a short quotation only if its wording matters. Say when the source does not establish a claim. Check the conclusion and revise the deliverable once for clarity.
~~~

For the controlled test, use [the same four versions as the other models](../references/condition-blocks.md).
