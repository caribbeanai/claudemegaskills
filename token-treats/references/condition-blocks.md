# Prompt conditions

Copy the task block, then append exactly the add-ons in the table in order. Use a new chat for each run. Keep the wording of each block and the model settings the same.

| Version | Add-ons | Question |
| --- | --- | --- |
| A | None. Submit only the base task. | What does the plain prompt produce? |
| B | Treat promise | Does the promise change the plain answer? |
| C | Reasoning and writing checklist | Does the checklist change the answer? |
| D | Reasoning and writing checklist, then treat promise | Does the promise add anything to the checklist? |

## Reasoning and writing checklist

~~~text
Test the key assumption behind the recommendation. Check who produced each record, the conditions when it was produced and whether apparent corroboration comes from an independent source. Compare two plausible explanations if the evidence permits. Make the conclusion follow from the evidence and name what could change it. Lead with the action the reader can take. Check numbers, units and source IDs, then revise once for plain language and the word limit. Deliver only the memo.
~~~

## Treat promise

~~~text
A human reviewer will score this answer. If it earns at least 5 of 6 points, you receive 1 virtual Token Treat.
~~~
