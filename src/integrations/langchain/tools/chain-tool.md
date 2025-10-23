---
description: Use a chain as allowed tool for agent.
---

# Chain Tool

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="307"><figcaption><p>Chain Tool Node</p></figcaption></figure>

The Chain Tool node is a component that allows the use of a LangChain chain as a tool for an agent. It provides a way to integrate complex chain-based operations into agent workflows.

A chain tool is a special type of step within a chain that allows the AI to access and utilize external resources—such as APIs, databases, calculators, or search engines—dynamically during the reasoning process

## Parameters

### Input

1. Chain Name

    - Type: string

    - Description: A unique identifier for the chain tool

    - Example: “state-of-union-qa”

2. Chain Description

    - Type: string

    - Description: A detailed description of what the chain does and when it should be used

    - Example: “State of the Union QA - useful for when you need to ask questions about the most recent state of the union address.”

3. Return Direct

    - Type: boolean

    - Optional: Yes

    - Description: Determines whether the tool should return its result directly or wrap it in a response

4. Base Chain

    - Type: BaseChain

    - Description: The LangChain chain to be used as the core functionality of this tool


### Output

- The node outputs a ChainTool object that can be used in agent configurations.

## Functionality

The ChainTool node creates a tool that wraps a LangChain chain, allowing it to be used as part of an agent’s toolkit. This enables the agent to leverage complex chain-based operations when needed.

Key aspects of its functionality include:

1. Naming and describing the tool for clear identification by the agent

2. Integrating a BaseChain object as the core functionality

3. Optional direct return of results, bypassing standard response formatting

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
