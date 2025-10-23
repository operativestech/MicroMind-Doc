# ReAct Agent Chat

Agent that uses the [ReAct](https://react-lm.github.io/) (Reasoning and Acting) logic to decide what action to take, optimized to be used with Chat Models.

<figure><img src="../../../.gitbook/assets/image (173).png" alt="" width="325"><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (6) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="336"><figcaption><p>ReAct Agent Chat Node</p></figcaption></figure>

## ReAct Agent Chat Functionality

The ReAct Agent (Chat) in FlowiseAI is an autonomous agent designed to interact through conversation while using external tools (like APIs or knowledge bases) to answer complex questions. "ReAct" stands for Reasoning and Acting — this agent combines step-by-step reasoning with the ability to take actions (like calling tools) to gather the information needed to respond accurately.

React Agent Chat extends ReactAgentLLM with conversational capabilities. It maintains chat history, tracks context, and enables multi-turn dialogue with the same ReAct logic underneath.

## Inputs

The ReAct Agent Chat requires the following inputs to function effectively:

### Required Parameters

* **Allowed Tools**: External capabilities the agent can use to complete tasks, such as web search, document reading, web scraping, file writing, API access, etc.
* **Chat Model**: language model that is specifically trained and optimized for multi-turn, conversational interactions (e.g., GPT-4 vs Claude 3).
* **Memory**: the memory input provides the agent with long-term context across multiple user interactions. It helps the agent remember previous messages, questions, and responses, allowing it to hold a coherent and natural multi-turn conversation.

### Optional Parameters

* **Input Moderation**: Optional input that enables content moderation. This helps ensure that queries are appropriate and do not contain offensive or harmful content.


## Special Features
- ReAct Framework: Implements the Reason + Act loop for sophisticated problem-solving.

- Chat Model Optimization: Specifically designed to work well with chat models for natural conversations.

- Tool Integration: Can use a variety of tools to enhance its capabilities and perform actions.

- Memory Management: Maintains conversation history for contextual understanding.

- Moderation: Can implement input moderation to ensure safe interactions.

- Vision Support: If the chat model supports vision capabilities, the agent can process and respond to image inputs.

- Streaming: Supports streaming responses for real-time interaction.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
