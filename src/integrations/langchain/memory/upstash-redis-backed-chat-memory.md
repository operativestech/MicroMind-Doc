---
description: Summarizes the conversation and stores the memory in Upstash Redis server.
---

# Upstash Redis-Backed Chat Memory

<figure><img src="../../../.gitbook/assets/image (112).png" alt="" width="302"><figcaption><p>Upstash Redis-Backed Chat Memory Node</p></figcaption></figure>

The Upstash Redis-Backed Chat Memory node is a component that provides long-term memory storage for chat conversations using Upstash Redis. It summarizes and stores conversation history, allowing for persistent memory across chat sessions.

## Parameters
​
### Credential

- Type: credential
- Credential Names: upstashRedisMemoryApi
- Description: Configure password authentication for your Upstash Redis instance
​
### Inputs

1. Upstash Redis REST URL

- Type: string
- Description: The base URL for your Upstash Redis instance
- Placeholder: ```text https://<your-url>.upstash.io```

2. Session Id (optional)

- Type: string
- Description: Unique identifier for the chat session. If not specified, a random id will be used

3. Session Timeouts (optional)

- Type: number
- Description: Time-to-live for the session in seconds. Omit this parameter to make sessions never expire

4. Memory Key

- Type: string
- Default: ‘chat_history’
- Description: Key used to store and retrieve the chat history in Redis
​
## Functionality

1. Initialization:

- Creates a Redis client using the provided URL and authentication token.
- Sets up an UpstashRedisChatMessageHistory instance.
- Initializes a BufferMemoryExtended instance with the chat history.

2. Memory Operations:

- ```text getChatMessages```: Retrieves stored chat messages from Redis.
- ```text addChatMessages```: Adds new messages to the Redis storage.
- ```text clearChatMessages```: Clears all messages for a given session.

## Usage

This node is particularly useful in scenarios where you need to maintain conversation context over extended periods or across multiple sessions. It leverages Upstash Redis for efficient and scalable storage of chat history.


## Integration

The node can be easily integrated into a larger conversational AI system, providing a robust solution for managing chat memory. It’s designed to work seamlessly with other components and can be configured through the Ardor UI.


## Note

Ensure that you have proper credentials and access to an Upstash Redis instance before using this node. The Redis connection is managed as a singleton to optimize resource usage across multiple instances of the node.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
