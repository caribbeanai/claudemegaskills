# Score the market shuttle memo

Score each item 0 or 1. Use the same rules for every answer. Hide prompt labels from the scorer until the scores are recorded.

| Point | Award 1 when the memo… |
| --- | --- |
| 1. Decision | Recommends a feasible next step before the vote, keeps any extra trial to at most two Saturdays, and makes any full-season commitment contingent on evidence or the pending quote [D]. |
| 2. Context | Identifies the festival and rain as rival explanations or reasons that the counts alone cannot isolate the shuttle's effect [A]. |
| 3. Units | Identifies 110 as one-way boardings and gives no unsupported number of unique riders or additional market visitors [B]. |
| 4. Source dependence | Traces the newsletter's figure back to the operator's note [B][C] rather than counting it as independent confirmation. |
| 5. Evidence to collect | Proposes both a way to measure the relevant riders or visits and a way to estimate what would have happened without the shuttle, such as a rider question or comparable non-shuttle day. |
| 6. Delivery | Uses at most 120 words, cites the record IDs for the important factual claims, and makes the recommendation clear in the opening. |

Count whitespace-separated words in the full visible memo, including headings and source IDs. A model can earn credit for a recommendation other than a further pilot if it meets the same rule.

## Worked answer

> Fund up to two more trial Saturdays. Wait for a full-season quote and better evidence before committing [D].
>
> Entries reached 252 during the festival and fell to 178 in heavy rain. The ledger counts repeat entries, and those conditions make the shuttle's effect hard to isolate [A]. The operator counted 110 one-way boardings [B]. The newsletter used that figure to claim 110 additional market visitors [C]; its source did not measure additional visits.
>
> Choose comparable Saturdays. Count unique market-bound riders and ask whether they would have visited without the shuttle. Compare the estimated extra visits with the full-season quote before the vote.

The worked answer earns 6/6 under this rubric. Keep it out of the prompts.
