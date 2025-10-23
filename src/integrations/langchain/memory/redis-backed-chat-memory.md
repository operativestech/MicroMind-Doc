---
description: Summarizes the conversation and stores the memory in Redis server.
---

# Redis-Backed Chat Memory

<figure><img src="../../../.gitbook/assets/image (109).png" alt="" width="302"><figcaption><p>Redis-Backed Chat Memory Node</p></figcaption></figure>

The Redis-Backed Chat Memory node is a component that provides long-term memory storage for chat conversations using Redis as the backend. It summarizes and stores conversation history, allowing for persistent and scalable chat memory across sessions.

## Parameters
​
### Credential
  -  Type: credential
  -  Credential Names: redisCacheApi, redisCacheUrlApi
  -  Description: Redis connection credentials

​
### Inputs

1. Session Id (optional)

    - Type: string
    - Default: Empty string
    - Description: Unique identifier for the chat session. If not specified, a random id will be used

2. Session Timeouts (optional)

    - Type: number
    - Description: Time-to-live (TTL) for the session in seconds. Omit this parameter to make sessions never expire

3. Memory Key

    - Type: string
    - Default: “chat_history”
    - Description: Key used to store and retrieve the chat history in Redis

4. Window Size (optional)

    - Type: number
    - Description: Number of recent back-and-forth interactions to use as memory context


## Functionality

1. Initialization:

- Connects to Redis using provided credentials (either URL or individual connection parameters).
- Sets up a RedisChatMessageHistory instance for managing chat history.
- Creates a BufferMemoryExtended instance for handling memory operations.

2. Memory Operations:

- getChatMessages: Retrieves chat messages from Redis, with options for windowing and prepending messages.
- addChatMessages: Adds new messages (both user and AI) to the Redis store.
- clearChatMessages: Deletes all messages for a given session from Redis.

3. Session Management:

- Supports session-based storage using session IDs.
- Optional session timeout (TTL) for automatic expiration of old sessions.

## Use Cases

- Long-running chatbots that need to maintain context across multiple interactions.
- Multi-user chat systems where each user’s history needs to be stored separately.
- Applications requiring scalable and persistent chat memory storage.

## Integration

This node can be used in a AI solution to provide long-term memory capabilities to language models or other AI components that benefit from conversation history.


## Notes

- Ensure that a Redis server is properly set up and accessible for this node to function correctly.
- When using in production, consider security implications and ensure proper authentication and encryption for Redis connections.
- The window size parameter can be used to limit the amount of history provided to AI models, which can be useful for managing token limits or focusing on recent context.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
