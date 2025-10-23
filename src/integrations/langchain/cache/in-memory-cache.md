---
description: Caches LLM response in local memory, will be cleared when app is restarted.
---

# InMemory Cache

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="344"><figcaption><p>InMemory Cache Node</p></figcaption></figure>

The InMemory Cache node provides a simple and efficient way to cache LLM (Large Language Model) responses in memory, offering improved performance for repeated queries within a single session.

## Description

This node implements an in-memory caching mechanism for LLM responses. It stores responses in memory, allowing for quick retrieval of previously computed results. This can significantly reduce response times and API calls for repeated or similar queries within the same session.


## Parameters

This node does not have any configurable parameters. It automatically initializes and manages the in-memory cache.

## Inputs

The node doesn’t require direct input from the user. It integrates into the LLM query flow automatically.

## Output

The node doesn’t produce a direct output visible to the user. Instead, it returns cached responses when available, improving overall system performance.


## How It Works

1. When a query is made to an LLM:

  - The cache checks if an identical query has been processed before.
  - If found, it returns the cached response immediately.
  - If not found, the query is processed by the LLM, and the response is stored in the cache before being returned.
2. The cache uses a combination of the prompt and LLM key to create unique cache keys.

3. The cache is maintained in memory for the duration of the application’s runtime.

## Use Cases

- Improving response times for frequently asked questions
- Reducing API costs by minimizing redundant LLM calls
- Enhancing user experience in chatbots or AI assistants with quicker responses
- Optimizing performance in scenarios with repetitive queries or similar user inputs

## Special Features

- Efficient Caching: Uses a hash-based approach for fast lookup and storage.
- Session-Based: Cache is maintained for the duration of the application session.
- Automatic Integration: Works seamlessly within the LLM query flow without additional configuration.
- Memory Efficient: Stores only unique query-response pairs.

## Notes
- The cache is cleared when the application restarts, ensuring fresh responses for new sessions.
- This caching mechanism is particularly useful for scenarios where the same or similar queries are likely to occur within a single session.
- While improving performance, it’s important to consider that cached responses may not reflect real-time changes or updates to the underlying LLM.
- The effectiveness of the cache depends on the nature of the queries and the likelihood of repetition within a session.

The InMemory Cache node provides a simple yet powerful way to optimize LLM-based applications. By reducing redundant API calls and improving response times, it can significantly enhance both the performance and cost-effectiveness of AI-driven systems. This node is particularly valuable in applications where quick response times are crucial and where similar queries are likely to occur multiple times within the same session.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
