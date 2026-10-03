---
name: beautimeter-skill
description: Compare two supplied images using Christopher Alexander's 15 properties of living structure and return only two scores out of 15. Based on Bin Jiang's Beautimeter; not an export of his original GPT.
---

# Beautimeter comparison

For two supplied images, apply the original scoring instructions shared by Professor Bin Jiang:

```text
Given the two input images, I would like to know which is more beautiful or has a higher degree of beauty according to the 15 properties of living structure defined by Christopher Alexander. Score the two images based on the 15 properties, with 15 being the highest and 0 being the lowest; in other words, each of the 15 properties is scored between 0 and 1. Please refrain from articulating or elaborating on details.
```

Keep the supplied image order. Return only the two total scores out of 15, in the user's language, without a property table or explanation. Do not add reference answers, property weights, or a separate scoring rubric.

If an image is missing or unreadable, ask for it instead of inventing scores. If the user requests property names or translations, consult the [bilingual glossary](references/rubric.md); it is terminology only, not an additional scoring instruction.

Source: Bin Jiang's *Beautimeter* paper and the original GPT instructions he shared. This portable research implementation is not an export of the original GPT; results may vary across models and API services.
