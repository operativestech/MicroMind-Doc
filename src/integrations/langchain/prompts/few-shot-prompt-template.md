---
description: Prompt template you can build with examples.
---

# Few Shot Prompt Template

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="245"><figcaption><p>Few Shot Prompt Template Node</p></figcaption></figure>

The Few-Shot Prompt Template Function is a powerful tool for constructing prompts that guide AI models by providing them with a set of example input-output pairs - known as "few-shot examples." This technique is widely used to improve the accuracy and reliability of language models, especially for tasks requiring structured outputs or specific formats.

## What Is Few-Shot Prompting?

- Few-shot prompting involves supplying the language model with a handful of demonstrations (examples) of the desired task within the prompt itself.

- These examples teach the model how to respond to new, similar queries by showing the expected pattern or structure

## When to Use

- When you want to guide a language model with clear, structured demonstrations.

- For tasks where output format consistency is important.

- In scenarios where zero-shot prompting (no examples) yields unreliable results.

## Parameters

### Inputs

1. **Examples** (Required)

  - Type: string (JSON)

  - Description: Array of example objects with key-value pairs

  - Example:
      ```code
      [
        { "word": "happy", "antonym": "sad" },
        { "word": "tall", "antonym": "short" }
      ]```

2. **Example Prompt** (Required)

  - Type: PromptTemplate

  - Description: Template for formatting individual examples

3. **Prefix** (Optional)

  - Type: string

  - Description: Text appearing before the examples

  - Example: “Give the antonym of every input”

4. **Suffix** (Required)

  - Type: string

  - Description: Text after examples, containing input variable

  - Example: “Word:

  \nAntonym:”

5. **Example Separator** (Optional)

  - Type: string

  - Default: “\n\n”

  - Description: String used to separate examples

6. **Template Format** (Optional)

  - Type: options

  - Options: [“f-string”, “jinja-2”]

  - Default: “f-string”

  - Description: Format style for template strings

## Best Practices

1. Example Design

    - Clear demonstrations

    - Consistent formatting

    - Diverse examples

    - Progressive complexity

2. Template Structure

    - Compatible formats

    - Clear separators

    - Proper variables

    - Consistent style

3. Performance Optimization

    - Efficient examples

    - Minimal redundancy

    - Clear instructions

    - Optimal spacing

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
