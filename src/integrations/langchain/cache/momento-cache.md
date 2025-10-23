---
description: Cache LLM response using Momento, a distributed, serverless cache.
---

# Momento Cache

The Momento Cache node provides integration with Momento, a distributed, serverless cache service. It allows for efficient caching of LLM (Large Language Model) responses across multiple sessions and instances.

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="331"><figcaption><p>Momento Cache Node</p></figcaption></figure>

## Description

This node implements a caching mechanism using Momento’s serverless cache service. It stores LLM responses in a distributed cache, allowing for quick retrieval of previously computed results across different sessions and application instances. This can significantly reduce response times and API calls for repeated queries.

## Parameters
- Credential
  - Type: credential
  - Credential Names: momentoCacheApi
  - Description: The API credentials required to authenticate with the Momento cache service.

## Inputs

The node doesn’t require direct input from the user. It integrates into the embedding generation flow automatically.

## Output

- The node returns a ```Text LangchainMomentoCache``` object, which can be used as a cache backend for LangChain operations.

## How It Works
1. The node initializes a connection to the Momento cache service using the provided credentials.
2. When a query is made to an LLM:
  - The cache checks if an identical query has been processed before.
  - If found, it returns the cached response immediately.
  - If not found, the query is processed by the LLM, and the response is stored in the Momento cache before being returned.
3. The cache uses a combination of the prompt and LLM key to create unique cache keys.
4. The cached data is stored in Momento’s distributed cache, making it accessible across multiple sessions and instances.

## Use Cases
- Improving response times for frequently asked questions across multiple application instances
- Reducing API costs by minimizing redundant LLM calls in distributed systems
- Enhancing user experience in scalable chatbots or AI assistants with quicker responses
- Optimizing performance in scenarios with repetitive queries across different user sessions

## Special Features
- Distributed Caching: Utilizes Momento’s serverless cache for cross-instance caching.
- Scalability: Easily scales with application growth without managing cache infrastructure.
- Persistence: Cache persists beyond individual application sessions.
- Automatic Integration: Works seamlessly within the LLM query flow.
- Configurable TTL: Supports setting Time-To-Live for cached items.

## Notes
- Requires a Momento account and API credentials to function.
- The cache persists across application restarts, ensuring continuity of cached responses.
- This caching mechanism is particularly useful for scenarios where the same or similar queries are likely to occur across different sessions or application instances.
- While improving performance, it’s important to consider that cached responses may not reflect real-time changes or updates to the underlying LLM.
- The effectiveness of the cache depends on the nature of the queries and the likelihood of repetition across different users or sessions.

The Momento Cache node provides a powerful solution for optimizing LLM-based applications in distributed or serverless environments. By leveraging Momento’s serverless cache, it offers efficient caching capabilities that can significantly enhance both the performance and cost-effectiveness of AI-driven systems at scale. This node is particularly valuable in applications where quick response times are crucial across multiple instances or where similar queries are likely to occur from different users or sessions.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
