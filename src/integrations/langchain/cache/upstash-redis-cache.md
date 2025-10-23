---
description: Cache LLM response in Upstash Redis, serverless data for Redis and Kafka.
---

# Upstash Redis Cache

The Upstash Redis Cache node provides integration with Upstash Redis, a serverless Redis service, for caching LLM (Large Language Model) responses. It offers efficient, scalable caching capabilities suitable for serverless and edge computing environments.

<figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="328"><figcaption><p>Upstash Redis Cache Node</p></figcaption></figure>

## Parameters

- Credential
  - Type: credential
  - Credential Names: upstashRedisApi
  - Description: The credentials required to connect to the Upstash Redis service.

## Input

- The node doesn’t require direct input from the user. It integrates into the LLM query flow automatically.

## Output

- The node initializes and returns an Upstash Redis Cache instance that can be used as a caching backend for LLM operations.

## How It Works

1. The node establishes a connection to the Upstash Redis service using the provided credentials.
2. When a query is made to an LLM:
  - The cache checks if an identical query has been processed before.
  - If found, it returns the cached response immediately.
  - If not found, the query is processed by the LLM, and the response is stored in the Upstash Redis cache before being returned.
3. The cache uses a combination of the prompt and LLM key to create unique cache keys.
4. Cached data is stored in Upstash’s serverless Redis, making it accessible across multiple serverless function invocations or edge locations.

## Use Cases

- Improving response times for LLM queries in serverless architectures
- Reducing API costs by minimizing redundant LLM calls in edge computing scenarios
- Enhancing user experience in globally distributed applications with quicker responses
- Optimizing performance in scenarios with repetitive queries across different serverless function invocations
- Implementing efficient caching for LLM-based chatbots or AI assistants deployed on edge networks

## Special Features

- Serverless Caching: Utilizes Upstash’s serverless Redis for scalable, managed caching.
- Global Distribution: Supports caching across multiple regions for low-latency access.
- Automatic Scaling: Scales automatically with application demand without managing infrastructure.
- Persistence: Cache persists beyond individual function invocations or application restarts.
- Compatibility: Works seamlessly with serverless platforms and edge computing environments.

## Notes

- Requires an Upstash account and API credentials to function.
- Ideal for serverless and edge computing scenarios where traditional Redis setups might be challenging.
- The cache persists across function invocations, ensuring continuity of cached responses in serverless environments.
- This caching mechanism is particularly useful for scenarios where the same or similar queries are likely to occur across different regions or function invocations.
- While improving performance, it’s important to consider that cached responses may not reflect real-time changes or updates to the underlying LLM.
- The effectiveness of the cache depends on the nature of the queries and the likelihood of repetition across different users or sessions.

The Upstash Redis Cache node provides a powerful solution for optimizing LLM-based applications in serverless and edge computing environments. By leveraging Upstash’s serverless Redis service, it offers efficient caching capabilities that can significantly enhance both the performance and cost-effectiveness of AI-driven systems at global scale. This node is particularly valuable in applications where quick response times are crucial across multiple regions or where similar queries are likely to occur from different serverless function invocations or edge locations.



{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
