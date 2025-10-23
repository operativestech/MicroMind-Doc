---
description: Schema to represent a chat prompt.
---

# Chat Prompt Template

<figure><img src="../../../.gitbook/assets/image (14) (1) (1).png" alt="" width="239"><figcaption><p>Chat Prompt Template Node</p></figcaption></figure>

A Chat Prompt Template allows you to define a sequence of chat messages—such as system, human, and AI messages—using templates with placeholders for variables. These templates can be filled in at runtime with user inputs or contextual data, making it easy to generate consistent and context-aware prompts for language models

## Parameters

### Inputs

1. System Message (Required)

    - Type: string

    - Description: Initial system message that sets the context or role for the AI

    - Example: "You are a helpful assistant that translates {input_language} to {output_language}."

2. Human Message (Required)

    - Type: string

    - Description: Human message prompt added at the end of the message sequence

    - Example: "{text}"

3. Format Prompt Values (Optional)

    - Type: JSON

    - Description: Variables specification for use in prompts

    - Example:
    ``` code
      {
      "input_language": "English",
      "output_language": "Spanish"
      }
    ```
4. Messages History (Optional)

    - Type: Tabs

    - Default: messageHistoryCode

    - Description: Additional messages after System Message for few-shot examples

    - Tabs:

        - Add Messages (Code)

            - Type: code

            - Description: Custom message history using JavaScript code

## Best Practices

1. System Message Design

    - Clear instructions

    - Specific role definition

    - Consistent context

    - Appropriate constraints

2. Message History

    - Relevant examples

    - Progressive complexity

    - Clear structure

    - Safe code execution

3. Variable Management

    - Clear naming

    - Type consistency

    - Error handling

    - Default values

## Input/Output

### Input

- The node takes in the defined parameters (system message, human message, prompt values, and optional message history).

- If message history code is provided, it is executed in a sandboxed environment.


### Output

- The node outputs a ChatPromptTemplate object that includes:

    - A system message

    - Optional message history (if provided and valid)

    - A human message

## Usage

This node is used to create structured chat prompts for language models. It’s particularly useful for:

1. Setting up consistent system instructions across multiple interactions.

2. Defining a standard format for human inputs.

3. Incorporating few-shot examples or specific conversation context through the message history feature.

4. Allowing for dynamic prompt creation by using variables in the system and human messages.

The Chat Prompt Template Function is a foundational tool for anyone developing advanced conversational AI workflows, enabling structured, maintainable, and highly customizable prompts for chat models

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
