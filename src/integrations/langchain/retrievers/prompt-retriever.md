---
description: >-
  Store prompt template with name & description to be later queried by
  MultiPromptChain.
---

# Prompt Retriever

<figure><img src="../../../.gitbook/assets/image (145).png" alt="" width="301"><figcaption><p>Prompt Retriever Node</p></figcaption></figure>

The Prompt Retriever node is designed to store prompt templates with associated names and descriptions. These stored prompts can later be queried and used by a MultiPromptChain. This node is particularly useful for organizing and managing multiple prompts that can be dynamically selected based on the context or requirements of a conversation or task.

## Input Parameters

1. Prompt Name

    - Type: string

    - Description: A unique identifier for the prompt template

    - Example: "physics-qa"

2. Prompt Description

    - Type: string

    - Description: A brief explanation of what the prompt does and when it should be used

    - Example: "Good for answering questions about physics"

3. Prompt System Message

    - Type: string

    - Description: The actual prompt template or system message that guides the AI's behavior

    - Example: "You are a very smart physics professor. You are great at answering questions about physics in a concise and easy to understand manner. When you don't know the answer to a question you admit that you don't know."


## Output

The node initializes and returns a PromptRetriever object, which encapsulates the provided prompt information (name, description, and system message).


## Usage

This node is typically used as part of a larger system where multiple specialized prompts are needed. By storing prompts with metadata, it allows for:

1. **Organized Prompt Management**: Keeping track of multiple prompts for different purposes.

2. **Dynamic Prompt Selection**: Enabling systems to choose the most appropriate prompt based on the current context or user query.

3. **Improved Maintainability**: Centralizing prompt storage and making it easier to update or modify prompts without changing the underlying code.


## Integration

The Prompt Retriever is often used in conjunction with a MultiPromptChain, which can dynamically select and use the most appropriate prompt based on the input or context. This allows for creating more flexible and adaptive AI systems that can handle a wide range of queries or tasks by selecting the most suitable prompt template.


## Example Use Case

In a multi-purpose AI assistant, you might have several Prompt Retriever nodes set up:

  - One for physics questions

  - One for literature analysis

  - One for coding help

  - One for general conversation

The system could then use a MultiPromptChain to analyze the user's input and select the most appropriate prompt, allowing the AI to seamlessly switch between different areas of expertise or conversation styles.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
