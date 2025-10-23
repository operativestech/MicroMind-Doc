---
description: >-
  Agent that is designed for LLMs that are good for reasoning/writing XML (e.g:
  Anthropic Claude).
---

# XML Agent

<figure><img src="../../../.gitbook/assets/image (9) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="335"><figcaption><p>XML Agent Node</p></figcaption></figure>

## XML Agent Functionality

The XML Agent is a specialized LangChain-based agent in AI designed to interpret and execute instructions formatted as XML tags. This structure allows for clean, parseable tool invocation using a standardized markup format.

## Inputs

The XML Agent requires the following inputs to function effectively:

### Required Parameters

* **Tools**: External capabilities the agent can use to complete tasks, such as web search, document reading, web scraping, file writing, API access, etc.
* **Memory**: the memory input provides the agent with long-term context across multiple user interactions. It helps the agent remember previous messages, questions, and responses, allowing it to hold a coherent and natural multi-turn conversation.
* **Chat Model**: language model that is specifically trained and optimized for multi-turn, conversational interactions (e.g., GPT-4 vs Claude 3).

### Optional Parameters

* **Input Moderation**: Optional input that enables content moderation. This helps ensure that queries are appropriate and do not contain offensive or harmful content.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
