---
description: Parse the output of an LLM call as a comma-separated list of values.
---

# CSV Output Parser

<figure><img src="../../../.gitbook/assets/image (115).png" alt="" width="304"><figcaption><p>CSV Output Parser Node</p></figcaption></figure>

A specialized parser that converts Language Model outputs into comma-separated lists, enabling easy extraction and processing of list-based responses.

**Remember**: Output Parser nodes are responsible for taking the output of a model and transforming it to a more suitable format for downstream tasks. Useful when you are using LLMs to generate structured data, or to normalize output from chat models and LLMs.


## Parameters

### Inputs

1. Autofix (Optional)

    - Type: boolean

    - Description: Enables automatic error correction by making additional model calls when parsing fails

    - Default: false

## Functionality

1. Parsing Operations

    - List extraction

    - Comma separation

    - Value normalization

    - Format validation

2. Error Handling

    - Automatic fixing (optional)

    - Format validation

    - Error reporting

    - Recovery options

## Use Cases

1. List Processing

    - Item enumeration

    - Data extraction

    - Value separation

    - Batch processing

2. Data Transformation

    - Format conversion

    - Structure normalization

    - List standardization

    - Output formatting

## Integration Notes

- Integrates with LangChain base classes

- Supports automatic error correction

- Handles various list formats

- Produces standardized arrays


## Best Practices

1. Input Formatting

    - Clear list structure

    - Proper comma usage

    - Value consistency

    - Format validation

2. Error Management

    - Enable autofix for reliability

    - Handle parsing failures

    - Validate input format

    - Monitor error patterns

3. Performance Optimization

    - Efficient list processing

    - Minimal format complexity

    - Optimal autofix usage

    - Clean data handling

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
