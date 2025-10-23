---
description: >-
  Cache LLM response in Redis, useful for sharing cache across multiple
  processes or servers.
---

# Redis Cache

The Redis Cache node provides integration with Redis, a popular in-memory data structure store, for caching LLM (Large Language Model) responses. It offers efficient caching capabilities across multiple sessions and instances.

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="331"><figcaption><p>Redis Cache Node</p></figcaption></figure>

## Parameters

- Credential
  - Type: credential
  - Credential Names: momentoCacheApi
  - Description: The API credentials required to authenticate with the Momento cache service.

## Inputs

The node doesn’t require direct input from the user. It integrates into the embedding generation flow automatically.

## Output

- The node returns a ```Text LangchainRedisCache``` object, which can be used as a cache backend for LangChain operations.

## How It Works

1. The node initializes a connection to the Redis server using the provided credentials.
2. When a query is made to an LLM:
  - The cache checks if an identical query has been processed before.
  - If found, it returns the cached response immediately.
  - If not found, the query is processed by the LLM, and the response is stored in the Redis cache before being returned.
3. The cache uses a combination of the prompt and LLM key to create unique cache keys.
4. If a TTL is specified, cached items will expire after the set duration.

## Use Cases

- Improving response times for frequently asked questions across multiple application instances
- Reducing API costs by minimizing redundant LLM calls in distributed systems
- Enhancing user experience in scalable chatbots or AI assistants with quicker responses
- Optimizing performance in scenarios with repetitive queries across different user sessions
- Sharing cache across multiple processes or servers

## Special Features

- Distributed Caching: Utilizes Redis for cross-instance caching.
- Persistence: Cache can persist beyond individual application sessions.
- Configurable TTL: Supports setting Time-To-Live for cached items.
- Flexible Connection: Supports both direct Redis configuration and URL-based connection.
- SSL Support: Offers secure connections to Redis servers.

## Notes
- Requires access to a Redis server, either self-hosted or cloud-based.
- The cache persists across application restarts, ensuring continuity of cached responses.
- This caching mechanism is particularly useful for scenarios where the same or similar queries are likely to occur across different sessions or application instances.
- While improving performance, it’s important to consider that cached responses may not reflect real-time changes or updates to the underlying LLM.
- The effectiveness of the cache depends on the nature of the queries and the likelihood of repetition across different users or sessions.
- The node supports both standalone Redis setups and clustered environments.


The Redis Cache node provides a robust solution for optimizing LLM-based applications in distributed environments. By leveraging Redis’s fast in-memory data store, it offers efficient caching capabilities that can significantly enhance both the performance and cost-effectiveness of AI-driven systems at scale. This node is particularly valuable in applications where quick response times are crucial across multiple instances or where similar queries are likely to occur from different users or sessions, and where sharing cache across multiple processes or servers is beneficial.


{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
