# Token Treats

![A turquoise Token Treats bag with a cartoon robot eating a biscuit and a cutaway showing a chip inside](assets/token-treats.webp)

**Vitamins for your prompt.** Give your AI a checklist that asks it to question an assumption, check where its evidence came from and edit its work. Add a virtual biscuit if you want to test whether the promise changes the answer.

## Try it

1. Open [the market shuttle task](references/task-market.md) and [the four prompt versions](references/condition-blocks.md).
2. Run each version in a fresh chat with the same model and settings. Shuffle the answers and hide their labels.
3. Score the memos with [the answer key](references/scorecard.md), then compare B with A and D with C. Those pairs measure the effect of adding the exact treat promise used here. Compare C with A for the checklist on its own.

[Full experiment and feedback protocol](references/experiment.md) · [Second task](references/task-library.md) · [Research and its limits](references/research.md) · [First pilot](references/pilot.md)

## Use it on your own work

In a client that loads [Agent Skills](https://agentskills.io/specification), add the `token-treats` folder using the client's skill import process. In a regular chat, open the guide for your model and copy its prompt. Use the same canonical prompt blocks across models when you want to compare results.

| Model | Paste-ready guide |
| --- | --- |
| ChatGPT | [ChatGPT](models/chatgpt.md) |
| Claude | [Claude](models/claude.md) |
| Gemini | [Gemini](models/gemini.md) |
| DeepSeek | [DeepSeek](models/deepseek.md) |
| Copilot, Mistral or Llama | [Other models](models/other-models.md) |

The virtual treat is a scorekeeper's label. A human can enter it as feedback in the current chat and record it in their own log. The skill only supplies instructions and does not run scripts, change model settings or store a balance itself.

## Artwork

The pouch is a parody product concept styled as a phone photo. Use this alt text when you post the image: “A turquoise Token Treats bag with a cartoon robot eating a biscuit and a cutaway showing a glowing microchip inside.”
