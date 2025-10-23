---
description: Agent that uses Function Calling to pick the tools and args to call.
---

# Tool Agent

<figure><img src="../../../.gitbook/assets/image (8) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="337"><figcaption><p>Tool Agent Node</p></figcaption></figure>

## Tool Agent Functionality

The Tool Agent node in AIMicroMind plays a central role in enabling LangChain-style agentic behavior, allowing an LLM to reason and decide when and how to call tools (functions) dynamically during a conversation or task.


## Inputs

The Tool Agent requires the following inputs to function effectively:

### Required Parameters

* **Tools**: External capabilities the agent can use to complete tasks, such as web search, document reading, web scraping, file writing, API access, etc.
* **Memory**: the memory input provides the agent with long-term context across multiple user interactions. It helps the agent remember previous messages, questions, and responses, allowing it to hold a coherent and natural multi-turn conversation.
* **Tool Calling Chat Model**: Only compatible with models that are capable of function calling: ChatOpenAI, ChatMistral, ChatAnthropic, ChatGoogleGenerativeAI, ChatVertexAI, GroqChat

### Optional Parameters

* **Input Moderation**: Optional input that enables content moderation. This helps ensure that queries are appropriate and do not contain offensive or harmful content.

## Special Features

- Function Calling: Utilizes advanced chat models’ function calling for precise tool selection and execution.

- Memory Management: Maintains conversation history for contextual understanding.

- Tool Integration: Can use a variety of tools to enhance its capabilities and perform actions.

- Moderation: Can implement input moderation to ensure safe interactions.

- Vision Support: If the chat model supports vision capabilities, the agent can process and respond to image inputs.

- Streaming: Supports streaming responses for real-time interaction.

- Customizable Prompts: Allows for custom chat prompt templates to tailor the agent’s behavior.

## Notes

- The agent uses a sophisticated prompt structure to maintain consistent behavior.

- It can handle multi-modal inputs if the underlying chat model supports it (e.g., text and images).

- The system message can be customized to tailor the agent’s personality and capabilities.

- The max iterations parameter can be used to control the depth of the agent’s problem-solving attempts.

- This agent is particularly useful for scenarios where maintaining conversation context, using specific tools, and leveraging function calling capabilities are important.

The Tool Agent node provides a powerful solution for building AI systems that can engage in informed, context-aware conversations while having the ability to use tools as needed. Its combination of conversational abilities, tool usage, and function calling makes it suitable for a wide range of applications requiring both knowledge access and task execution within a conversational framework.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
