---
description: >-
  Cache LLM response in Redis, useful for sharing cache across multiple
  processes or servers.
---

# Redis Embeddings Cache

The Redis Embeddings Cache node provides a mechanism to cache generated embeddings using Redis, a high-performance in-memory data store. This node is designed to improve efficiency and reduce computational costs when working with embedding models.

<figure><img src="../../../.gitbook/assets/up-001.png" alt="" width="280"><figcaption><p>Redis Embeddings Cache Node</p></figcaption></figure>

## Parameters

- Embeddings (Required)

  - Type: Embeddings
  - Description: The embedding model to be used for generating embeddings.

- Credential

  - Type: credential
  - Credential Names: momentoCacheApi
  - Description: The API credentials required to authenticate with the Momento cache service.

## Inputs

- The node doesn’t require direct input from the user. It integrates into the embedding generation flow automatically.

## Output

- The node returns a ```Text CacheBackedEmbeddings``` object, which wraps the original embedding model with Redis-based caching functionality.

## How It Works

1. The node initializes a connection to the Redis server using the provided credentials.
2. When a query is made to an LLM:
  - The cache checks if an identical query has been processed before.
  - If found, it returns the cached response immediately.
  - If not found, the query is processed by the LLM, and the response is stored in the Redis cache before being returned.
3. The cache uses a combination of the prompt and LLM key to create unique cache keys.
4. If a TTL is specified, cached items will expire after the set duration.

## Use Cases

- Improving response times for applications that frequently generate embeddings
- Reducing API costs by minimizing redundant embedding generation calls
- Enhancing performance in scenarios with repetitive text inputs or similar queries
- Optimizing vector search operations by caching frequently used embeddings
- Sharing cached embeddings across multiple processes or servers

## Special Features

- Distributed Caching: Utilizes Redis for cross-instance caching of embeddings.
- Configurable TTL: Supports setting Time-To-Live for cached embeddings.
- Namespace Support: Allows for organization of multiple caches within the same Redis instance.
- Flexible Connection: Supports both direct Redis configuration and URL-based connection.
- SSL Support: Offers secure connections to Redis servers.
- LangChain Integration: Built on top of LangChain’s CacheBackedEmbeddings for reliability and consistency.

## Notes

- Requires access to a Redis server, either self-hosted or cloud-based.
- The cache persists across application restarts, ensuring continuity of cached embeddings.
- This caching mechanism is particularly useful for scenarios where the same or similar texts are likely to be embedded multiple times across different sessions or application instances.
- While improving performance, it’s important to consider Redis memory usage, especially for large numbers of unique embeddings.
- The effectiveness of the cache depends on the nature of the embedding requests and the likelihood of repetition across different users or sessions.
- Supports both standalone Redis setups and clustered environments.

The Redis Embeddings Cache node provides a powerful solution for optimizing embedding-based applications in distributed environments. By leveraging Redis’s fast in-memory data store, it offers efficient caching capabilities that can significantly enhance both the performance and cost-effectiveness of systems that rely heavily on embeddings. This node is particularly valuable in applications where quick embedding generation is crucial across multiple instances or where similar texts are likely to be processed multiple times from different users or sessions.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
