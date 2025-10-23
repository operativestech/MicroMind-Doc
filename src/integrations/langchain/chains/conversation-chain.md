---
description: Chat models specific conversational chain with memory.
---

# Conversation Chain

<figure><img src="../../../.gitbook/assets/image (30).png" alt="" width="332"><figcaption><p>Conversation Chain Node</p></figcaption></figure>

The Conversation Chain is a specialized chain designed for maintaining coherent, context-aware conversations using chat-based language models. It integrates memory components to retain conversation history, allowing for more natural and contextually relevant interactions.

## Parameters

  - Chat Model (Required)
    -  Type: BaseChatModel
    -  Description: The chat-based language model used for generating responses.

  - Memory (Required)
    -  Type: BaseMemory
    -  Description: The memory component used to store and retrieve conversation history.

  - Chat Prompt Template (Optional)
    -  Type: ChatPromptTemplate
    -  Description: Custom prompt template for the conversation. Must include variable in the human message.
    -  Additional Params: true

  - Input Moderation (Optional)
    -  Type: Moderation[]
    -  Description: Moderation tools to detect and prevent harmful input.
    -  Additional Params: true

  - System Message (Optional)
    -  Type: string
    -  Description: Custom system message to set the behavior of the AI assistant.
    -  Default: A predefined system message template.
    -  Rows: 4
    -  Additional Params: true

## How It Works

1. The chain receives a user input.
2. If input moderation is enabled, it checks the input for potential harmful content.
3. It retrieves the conversation history from the memory component.
4. The chat prompt template (or default if not provided) is populated with the conversation history and current input.
5. The populated prompt is sent to the chat model for processing.
6. The model generates a response based on the prompt and conversation context.
7. The response is returned as output.
8. The conversation history in the memory component is updated with the new interaction.

## Use Cases

- Building conversational AI assistants or chatbots
- Creating interactive storytelling or role-playing experiences
- Developing personalized tutoring or coaching systems
- Implementing customer support chatbots with context retention
- Designing conversational interfaces for complex applications

## Notes

- The quality and coherence of conversations heavily depend on the capabilities of the chosen chat model.
- Custom chat prompt templates can significantly influence the conversation style and flow.
- The system message can be used to set specific personality traits or knowledge domains for the AI.
- For multi-turn conversations, ensure that the memory component is properly configured to retain necessary context.
- The chain supports both text-only and multi-modal (text + image) inputs, depending on the chat model’s capabilities.
- Proper error handling should be implemented, especially for potential API failures or moderation issues.
- The effectiveness of the chain can vary based on the complexity of the conversation and the specific use case.

The Conversation Chain node provides a powerful foundation for building sophisticated, context-aware conversational AI systems. By combining advanced chat models with flexible memory components and customizable prompts, it enables the creation of natural, engaging, and persistent conversational experiences. This node is particularly valuable in scenarios where maintaining conversation context, personality consistency, and interactive responsiveness are crucial, such as in virtual assistants, interactive storytelling, or personalized customer engagement systems.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
