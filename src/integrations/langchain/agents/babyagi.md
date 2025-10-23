---
description: >-
  Task Driven Autonomous Agent which creates new task and reprioritizes task
  list based on objective
---

# BabyAGI

<figure><img src="../../../.gitbook/assets/image (14) (1) (1) (1).png" alt="" width="275"><figcaption><p>BabyAGI Node</p></figcaption></figure>

## BabyAGI Agent Functionality

The BabyAGI node in the AI MicroMind platform represents an autonomous task manager designed to take a single high-level objective and break it down into a sequence of subtasks it can create, prioritize, and execute on its own, continuously refining its task list as it progresses.

## Inputs

The BabyAGI Agent requires the following inputs to function effectively:

### Required Parameters

* **Chat Model**: language model that is specifically trained and optimized for multi-turn, conversational interactions (e.g., GPT-4 vs Claude 3).
* **Vector Store**: A vector store or vector database refers to a type of database system that specializes in storing and retrieving high-dimensional numerical vectors.
* **Task Loop**: refers to the core autonomous cycle that the agent follows to accomplish a high-level objective

### Optional Parameters
* **Input Moderation**: Optional input that enables content moderation. This helps ensure that queries are appropriate and do not contain offensive or harmful content.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
