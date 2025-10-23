---
description: Parse the output of an LLM call into a given (JSON) structure.
---

# Structured Output Parser

<figure><img src="../../../.gitbook/assets/image (127).png" alt="" width="301"><figcaption><p>Structured Output Parser Node</p></figcaption></figure>

The Structured Output Parser is a node used to parse the output of a Language Model (LLM) call into a predefined JSON structure. This node is particularly useful when you need to extract structured information from the LLM's response in a consistent format.

It is ideal for scenarios where the output structure is relatively flat and simple.

## Key Features

- **Basic Schema Support**: Allows users to define expected output fields and their types, usually via JSON schema or example-based schema generation.

- **Simple Validation**: Checks if the output matches the expected structure, but with less sophistication than advanced parsers.

- **Ease of Use**: Quick to set up for common use cases where outputs are not deeply nested or highly complex.

- **Intended for Final Output**: Best used for structuring the last step in a workflow, not for intermediary formatting.

## Parameters

### Inputs

1. Autofix (Optional)

    - Type: boolean

    - Description: Enables automatic error correction by making additional model calls when parsing fails

    - Default: false

2. JSON Structure (Required)

    - Type: datagrid

    - Description: Defines the expected JSON structure for model outputs

    - Schema:

        - Property: JSON property name

        - Type: Data type (string, number, boolean)

        - Description: Property description

    - Default:
    ```code
        [
          {
            "property": "answer",
            "type": "string",
            "description": "answer to the user's question"
          },
          {
            "property": "source",
            "type": "string",
            "description": "sources used to answer the question, should be websites"
          }
        ]
    
    ```

## Input

The node takes the following inputs:

- Configuration for autofix (boolean)

- JSON structure definition (datagrid)

## Output

The node outputs a StructuredOutputParser instance that can be used to parse LLM responses according to the defined JSON structure.

## Flow of the Structured Output Parser Node

1. Schema Definition

    - The user defines the expected output schema, usually as a JSON Schema or using libraries like Zod (TypeScript) or Pydantic (Python).

    - The schema specifies required fields, types, and descriptions for each output property.

2. LLM Call

    - The language model generates a response, typically as unstructured text or loosely structured JSON.

3. Parsing Step

    - The Structured Output Parser node receives the LLM output.

    - It attempts to parse the output according to the defined schema.

    - If the output matches the schema, it is transformed into a structured object.

    - If not, the parser may raise an error or attempt to fix the output (depending on configuration).

4. Output Delivery

    - The parsed, structured data is passed on to the next node in the workflow or consumed by downstream systems.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
