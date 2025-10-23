---
description: Stores the conversation in MongoDB Atlas.
---

# MongoDB Atlas Chat Memory

<figure><img src="../../../.gitbook/assets/image (108).png" alt="" width="299"><figcaption><p>MongoDB Atlas Chat Memory Node</p></figcaption></figure>

The MongoDB Atlas Chat Memory node is a component designed to store conversation history in MongoDB Atlas. It extends the functionality of BufferMemory to provide persistent storage of chat messages using MongoDB as the backend.

## Parameters
​
### Credential

Label: Connect Credential
Name: credential
Type: credential
Credential Names: mongoDBUrlApi
Description: MongoDB Atlas connection credentials
Description: MongoDB Atlas connection credentials
​
### Inputs

  - Database

    -  Label: Database
    -  Name: databaseName
    -  Type: string
    -  Placeholder: “mongodb+srv://username:password@cluster.mongodb.net/DB_NAME”
    -  Description: MongoDB Atlas database name

  - Collection Name

    -  Label: Collection Name
    -  Name: collectionName
    -  Type: string
    -  Placeholder: <COLLECTION_NAME>
    -  Description: Name of the collection to store chat messages

  - Session Id (Optional)

    -  Label: Session Id
    -  Name: sessionId
    -  Type: string
    -  Default: ” (empty string)
    -  Description: Unique identifier for the chat session. If not specified, a random id will be used

  - Memory Key (Additional Parameter)

    -  Label: Memory Key
    -  Name: memoryKey
    -  Type: string
    -  Default: ‘chat_history’
    -  Description: Key used to store the chat history in memory
​
## Functionality

1. Initialization:

- Connects to MongoDB Atlas using the provided credential.
- Creates a MongoDBChatMessageHistory instance.
- Initializes a BufferMemoryExtended instance.

2. Message Storage:

- Stores messages as documents in the specified MongoDB collection.
- Each document represents a chat session, identified by a sessionId.

3. Message Retrieval:

- Retrieves messages for a specific session from MongoDB.
- Converts stored messages to BaseMessage objects.

4. Memory Management:

- Supports adding new messages to the chat history.
- Allows clearing of chat history for a specific session.

5. Extended Functionality:

- Implements MemoryMethods interface for advanced memory operations.
- Supports overriding sessionId for flexible message management.

## Use Cases

- Long-term storage of conversation history.
- Maintaining separate chat histories for different users or contexts.
- Integrating persistent memory in chatbots or conversational AI systems.
​
## Notes
- This node uses a singleton pattern for MongoDB client management to optimize connections.
- It extends the base BufferMemory class to provide MongoDB-specific functionality.
- The node supports both adding individual messages and bulk message operations.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
