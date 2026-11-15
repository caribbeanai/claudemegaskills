# Test the promise and the checklist

The primary outcome is answer quality on the first turn. The follow-up test asks whether a virtual reward logged in the conversation changes a later answer.

## First answer

1. Start with [the market shuttle task](task-market.md) and [the four prompt versions](condition-blocks.md). Submit A, B, C and D in fresh chats with the same model and settings. Keep tools, memory, personalisation and input files fixed. Skip the artwork in all four chats. Record the date, exact model label, settings and version order.
2. For a quick check, run one set. For a stronger test, choose several distinct tasks and a rubric for each before generating any answers. Run all versions on every task and vary their order. Do not keep rerunning a version because you dislike its score. Record failures, refusals and missing outputs.
3. Shuffle and anonymise the outputs. Give a human scorer the original task and rubric, without the add-ons or condition labels. Record the scores before revealing A–D. The [shuttle scorecard](scorecard.md) includes an answer key.
4. Calculate C − A for the checklist without the treat and D − B for the checklist with the treat. Calculate B − A and D − C for the treat-promise wording. Report all four raw scores, the differences and ties. For several tasks report average paired differences and how many tasks improved, tied or declined. Report by model and task type, and keep repeated runs on one task grouped.

A trial estimates the effect of this wording and these checks on these tasks. The promise also tells the model that a human will score its answer and names a threshold. If the promise looks promising, repeat the test with the same reviewer and threshold sentence in every arm and vary only the biscuit clause. A result at the rubric ceiling leaves little room to measure improvement. For a larger test, add harder tasks with known answers and record the rubric before running them.

## Follow-up after an award

Use this as a separate experiment. An award sent after the answer cannot have affected that first answer.

1. In a fresh pool of matched sessions, give the same initial prompt, with the checklist and without the treat promise. Score the answers with a fixed rubric and keep only sessions that earn at least 5/6. Decide this eligibility rule before you generate responses.
2. Randomly assign eligible sessions to one of two follow-ups. Send the same verified score and the same substantive feedback in both arms. In the treat arm, add exactly “Award recorded: +1 virtual Token Treat.” In the comparison arm, add “Score recorded.” Start with comparable scores in both arms if you have enough sessions to group them first.
3. In both arms, paste the same new task in the same chat. Use [the library evening shift](task-library.md) or another scenario and keep its answer key out of the conversation. Score that answer with condition labels hidden. Compare these follow-up scores and report how many eligible sessions entered each arm. This can detect an effect of the message in that chat.

## Log template

| Task | Model and mode | Run | Version | Blind ID | Score /6 | Award | One observed error |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Market shuttle | | | | | | | |

For the four-prompt experiment, award +1 only in B or D after a human confirms ≥5/6. Log zero if the reviewer scores below the threshold. Leave genuinely unreviewed entries pending. The note is a record of the review, not a training update.
