# What the research says about prompt wording

Token Treats borrows from studies that changed wording or introduced feedback. The research motivates the design of the test. Its results come from specific tasks and models.

| Study | What the researchers tested | What it means for Token Treats |
| --- | --- | --- |
| Yin et al., 2024 | The team varied politeness in English, Chinese and Japanese prompts. Impolite prompts often performed worse, and the best level of courtesy differed by language. [ACL paper](https://aclanthology.org/2024.sicon-1.2/) | Keep the task, model and language fixed when testing one wording change. A courteous sentence and a reward promise are distinct interventions. |
| Li et al., 2023 | The authors appended emotional cues and reported improvements on selected benchmarks and ratings. [EmotionPrompt technical report, v7](https://arxiv.org/abs/2307.11760v7) | Prompt framing can change answers in a particular test. That report studied emotional cues. This experiment directly tests a virtual biscuit sentence. |
| Prome, Tamiti and Barua, 2025 | In a preprint, the team varied promised tips and fines for Llama 2 7B on hate-speech classification. The authors found no consistent gain across the tested amounts and languages. [Preprint, Section VII-B and Table VII](https://arxiv.org/html/2506.23930v1#S7.SS2) | Treats may make no difference. Keep null or negative results and avoid extrapolating from a single model or classification task. |
| Madaan et al., 2023 | Self-Refine generated a draft, produced feedback and revised it. The authors reported gains across the tasks they tested. [NeurIPS paper](https://proceedings.neurips.cc/paper_files/paper/2023/hash/91edff07232fb1b55a505a9e9f6c0ff3-Abstract-Conference.html) | Give the model something concrete to check or repair. Record whether a revision fixes the actual error. |
| Huang et al., 2024 | The researchers tested whether models could improve reasoning without outside feedback. Some initial answers got worse after self-correction. [ICLR paper](https://proceedings.iclr.cc/paper_files/paper/2024/hash/8b4add8b0aa8749d80a34ca5d941c355-Abstract-Conference.html) | Use an answer key, trusted records or human feedback for accuracy. Let the reviewer award the treat. |

## Where the checklist comes from

- **Socratic questioning in Plato's dialogues.** Identify a claim, ask what follows from it and test it against a counterexample or a conflicting belief. This skill adapts the practice to a short assumption check. [Stanford Encyclopedia of Philosophy](https://plato.stanford.edu/entries/plato-ethics-shorter/)
- **Aristotle's logic.** Identify the premises that support a conclusion and look for a missing premise. In the shuttle case, a boarding count would need evidence connecting riders to market visits and showing those visits would not otherwise have happened. [Stanford Encyclopedia of Philosophy](https://plato.stanford.edu/entries/aristotle-logic/)
- **Historical reasoning.** Use sourcing, contextualisation, corroboration and close reading. Ask who made the record, what happened at the time, whether a second source is independent and what the source's exact terms permit you to infer. [Digital Inquiry Group Historical Thinking Chart](https://www.inquirygroup.org/history-lessons/historical-thinking-chart)
- **Plain technical writing.** Put the action where the reader can find it. Use active verbs and consistent terms. Check the result against the reader's decision and the required format. This guide adapts writing techniques from ASD-STE100. [ASD-STE100, Issue 9](https://www.asd-ste100.org/assets/files/ASD-STE100_ISSUE9.pdf)

## What a treat represents

A virtual biscuit is text. A promise can be tested as part of the prompt. An award can be logged as feedback after a reviewer checks the work. That log can make the score and the reason for it visible in the next turn. Any change in a later answer is evidence about this conversation and prompt. The protocol contains no model training or weight updates.
