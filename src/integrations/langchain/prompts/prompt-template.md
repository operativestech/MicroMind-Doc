---
description: Schema to represent a basic prompt for an LLM.
---

# Prompt Template

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="243"><figcaption><p>Prompt Template Node</p></figcaption></figure>

The Prompt Template node enables the creation of structured prompts with dynamic placeholders, allowing for consistent and reusable prompt generation in Language Model interactions.

## Parameters

### Inputs

1. Template (Required)

  - Type: string

  - Rows: 4

  - Placeholder: "What is a good name for a company that makes {product}?"

  - Description: The prompt template with variables in curly braces { }, which will be replaced with actual values

2. Format Prompt Values (Optional)

  - Type: json

  - Accept Variable: true

  - List: true

  - Description: JSON object containing values for template variables

  - Example:

  ```code
    {
      "product": "eco-friendly water bottles"
    }```

## Functionality

1. Template Processing

    - Variable extraction

    - Placeholder validation

    - Format verification

    - Dynamic content insertion

2. Value Management

    - JSON parsing

    - Variable mapping

    - Type validation

    - Error checking


## Use Cases

1. Dynamic Content Generation

  - Customized prompts

  - Variable content

  - Consistent formatting

  - Template reuse

2. Standardization

  - Format consistency

  - Error reduction

  - Quality control

  - Pattern enforcement

## Integration Notes

- Supports variable injection

- Handles JSON formatting

- Validates template syntax

- Manages error states


## Best Practices

1. Template Design

- Clear variable naming

- Consistent formatting

- Descriptive placeholders

- Proper documentation

2. Value Management

- Valid JSON structure

- Complete variable sets

- Type consistency

- Error handling

3. Performance Optimization

- Efficient templates

- Minimal complexity

- Reusable patterns

- Clear structure

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
