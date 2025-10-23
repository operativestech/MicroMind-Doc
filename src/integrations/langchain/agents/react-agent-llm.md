# ReAct Agent LLM

Agent that uses the [ReAct](https://react-lm.github.io/) (Reasoning and Acting) logic to decide what action to take, optimized to be used with Non Chat Models.

<figure><img src="../../../.gitbook/assets/image (174).png" alt="" width="325"><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (7) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="335"><figcaption><p>ReAct Agent LLM Node</p></figcaption></figure>

## ReAct Agent LLM Functionality

This agent implements the ReAct (Reason + Act) framework, which allows it to alternate between reasoning about a problem and taking actions to solve it. It’s designed to work seamlessly with chat models, making it particularly effective for interactive, multi-turn conversations that involve complex problem-solving.

The ReactAgentLLM is the core agent that implements the ReAct paradigm, allowing LLMs to reason through problems and invoke tools/functions step-by-step based on intermediate observations.

## Inputs

The ReAct Agent LLM requires the following inputs to function effectively:

### Required Parameters

* **Allowed Tools**: External capabilities the agent can use to complete tasks, such as web search, document reading, web scraping, file writing, API access, etc.
* **Chat Model**: language model that is specifically trained and optimized for multi-turn, conversational interactions (e.g., GPT-4 vs Claude 3).
* **Memory**: the memory input provides the agent with long-term context across multiple user interactions. It helps the agent remember previous messages, questions, and responses, allowing it to hold a coherent and natural multi-turn conversation.

### Optional Parameters

* **Input Moderation**: Optional input that enables content moderation. This helps ensure that queries are appropriate and do not contain offensive or harmful content.


{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
