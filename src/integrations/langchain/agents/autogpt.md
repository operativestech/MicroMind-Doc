---
description: Autonomous agent with chain of thoughts for self-guided task completion.
---

# AutoGPT

<figure><img src="../../../.gitbook/assets/image (12) (2).png" alt="" width="277"><figcaption><p>AutoGPT Node</p></figcaption></figure>

## AutoGPT Agent Functionality

AutoGPT is an autonomous agent node designed for self-guided task completion. It uses a chain of thoughts approach to break down and solve complex tasks without constant human intervention.

The AutoGPT node implements an autonomous agent capable of breaking down complex tasks into smaller steps and executing them sequentially. It uses a language model, a set of tools, and a vector store for memory to guide its decision-making process.

The AutoGPT node implements an autonomous agent capable of breaking down complex tasks into smaller steps and executing them sequentially. It uses a language model, a set of tools, and a vector store for memory to guide its decision-making process.

## Inputs

### Required Parameters

* **Allowed Tools**:  External capabilities the agent can use to complete tasks, such as web search, document reading, web scraping, file writing, API access, etc.
* **Chat Model**: language model that is specifically trained and optimized for multi-turn, conversational interactions (e.g., GPT-4 vs Claude 3).
* **Vector Store Retriever**: Vector-based memory that allows the agent to remember past steps and avoid repetition. Useful for tasks that require reflection or long-term context.

### Optional Parameters

* **Input Moderation**: Optional input that enables content moderation. This helps ensure that queries are appropriate and do not contain offensive or harmful content.
* **AutoGPT Name**: The name given to the AutoGPT agent.
* **AutoGPT Role**: The role assigned to the AutoGPT agent.
* **Maxium Loop**: parameter controls how many iterations (or thought-action-observation cycles) the AutoGPT agent can run before automatically stopping.

## How It Works

1. The AutoGPT agent is initialized with the provided tools, language model, and vector store retriever.

2. The agent receives a task or goal as input.

3. It then enters a loop, where in each iteration it:

  - Determines the next action to take
  - Executes the action using the available tools
  - Updates its memory with the results
  - Decides whether to continue or finish the task

4. The agent continues this process until it completes the task, reaches the maximum number of iterations, or encounters an error.

5. Finally, it returns a detailed output including its thought process and results.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
