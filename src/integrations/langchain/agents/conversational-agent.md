---
description: Conversational agent for a chat model. It will utilize chat specific prompts.
---

# Conversational Agent

<figure><img src="../../../.gitbook/assets/image (10) (1) (1) (1) (1) (1).png" alt="" width="271"><figcaption><p>Conversational Agent Node</p></figcaption></figure>

The Conversational Agent is an advanced AI agent designed for dynamic, multi-turn conversations. It leverages a chat model, memory, and a set of tools to engage in contextual dialogue and perform tasks based on user input.

## Description

The Conversational Agent node creates an AI assistant capable of maintaining context over multiple interactions, using tools to gather information or perform actions, and providing coherent responses. It’s particularly suited for chat-based applications where context retention and task execution are important.

## Inputs

The Conversational Agent requires the following inputs to function effectively:

### Required Parameters

* **Allowed Tools**: List the tools this agent is permitted to use.
* **Chat Model**: language model that is specifically trained and optimized for multi-turn, conversational interactions (e.g., GPT-4 vs Claude 3).
* **Memory**: the memory input provides the agent with long-term context across multiple user interactions. It helps the agent remember previous messages, questions, and responses, allowing it to hold a coherent and natural multi-turn conversation.

### Optional Parameters

* **Input Moderation**: Optional input that enables content moderation. This helps ensure that queries are appropriate and do not contain offensive or harmful content.

## How It Works
1. The agent is initialized with the provided tools, chat model, memory, and optional parameters.
2. It receives a user input, which is first checked by any specified moderation tools.
3. The agent then:
  - Retrieves relevant context from its memory
  - Analyzes the input and context to determine the next action
  - Uses tools if necessary to gather information or perform tasks
  - Generates a response using the chat model
4. The response and any used tools or source documents are returned.
5. The conversation history is updated in the memory for future context.

## Special Features
- Vision Support: If the chat model supports vision capabilities, the agent can process and respond to image inputs.
- Streaming: The agent supports streaming responses, allowing for real-time interaction.
- Tool Integration: Can use a variety of tools to enhance its capabilities and perform actions.
- Memory Management: Maintains conversation history for contextual understanding.
- Moderation: Can implement input moderation to ensure safe interactions.

## Notes
- The agent uses a sophisticated prompt structure to maintain consistent behavior.
- It can handle multi-modal inputs if the underlying chat model supports it (e.g., text and images).
- The system message can be customized to tailor the agent’s personality and capabilities.
- The max iterations parameter can be used to control the depth of the agent’s problem-solving attempts.

The Conversational Agent node provides a powerful, flexible foundation for building interactive AI systems. Its ability to maintain context, use tools, and engage in multi-turn dialogues makes it suitable for a wide range of applications where natural, intelligent conversation is required. The integration of memory, tools, and optional features like vision support and moderation makes it a comprehensive solution for complex conversational AI tasks.


{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
