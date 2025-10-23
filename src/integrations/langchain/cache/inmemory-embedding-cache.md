---
description: Cache generated Embeddings in memory to avoid needing to recompute them.
---

# InMemory Embedding Cache

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="340"><figcaption><p>InMemory Embedding Cache Node</p></figcaption></figure>

The InMemory Embedding Cache node provides an efficient way to cache generated embeddings in memory, reducing the need to recompute them for repeated queries within a single session.

## Description

This node implements an in-memory caching mechanism for embeddings. It stores computed embeddings in memory, allowing for quick retrieval of previously generated results. This can significantly reduce computation time and API calls for repeated or similar embedding requests within the same session.

## Inputs

The node doesn’t require direct input from the user. It integrates into the embedding generation flow automatically.

* **Embedding**: The embedding model to be used for generating embeddings.

## Output

- The node returns a ```Text CacheBackedEmbeddings``` object, which wraps the original embedding model with caching functionality.


## How It Works

1. When an embedding request is made:

  - The cache checks if an identical request has been processed before.
  - If found, it returns the cached embedding immediately.
  - If not found, the embedding is generated using the provided embedding model, stored in the cache, and then returned.

2. The cache uses a combination of the input text and namespace (if provided) to create unique cache keys.

3. The cache is maintained in memory for the duration of the application’s runtime.

4. The caching mechanism is implemented using the ```text CacheBackedEmbeddings``` class from LangChain, which provides a robust framework for caching embeddings.


## Notes
- The cache is cleared when the application restarts, ensuring fresh embeddings for new sessions.
- This caching mechanism is particularly useful for scenarios where the same or similar texts are likely to be embedded multiple times within a single session.
- While improving performance, it’s important to consider memory usage, especially for large numbers of unique embeddings.
- The effectiveness of the cache depends on the nature of the embedding requests and the likelihood of repetition within a session.

The InMemory Embedding Cache node provides a powerful way to optimize embedding-based applications. By reducing redundant computation and improving response times, it can significantly enhance both the performance and cost-effectiveness of systems that rely heavily on embeddings. This node is particularly valuable in applications where quick embedding generation is crucial and where similar texts are likely to be processed multiple times within the same session.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
