---
description: Stores the conversation in dynamo db table.
---

# DynamoDB Chat Memory

<figure><img src="../../../.gitbook/assets/image (107).png" alt="" width="301"><figcaption><p>DynamoDB Chat Memory Node</p></figcaption></figure>

The DynamoDB Chat Memory node is a component that stores conversation history in an Amazon DynamoDB table. It extends the functionality of the BufferMemory class to provide persistent storage of chat messages using AWS DynamoDB as the backend.

## Parameters
​
- ### Credential

    Type: credential
    Credential Names: dynamodbMemoryApi
    Description: AWS credentials for DynamoDB access
​
## Inputs

1. Table Name

    Type: string
    Description: The name of the DynamoDB table to store chat 
    
2. Partition Key

    Type: string
    Description: The primary key for the DynamoDB table

3. Region

    Type: string
    Description: The AWS region where the DynamoDB table is located
    Placeholder: us-east-1


4. Session ID (optional)

    Type: string
    Default: ” (empty string)
    Description: Unique identifier for the chat session. If not specified, a random ID will be used


5. Memory Key

    Type: string
    Default: ‘chat_history’
    Description: Key used to store the chat history in memory
​
## Functionality

The DynamoDB Chat Memory node provides the following key features:

1. Initialization: Sets up the DynamoDB client and creates a BufferMemoryExtended instance with the specified parameters.

2. Message Storage: Stores chat messages (both user inputs and AI responses) in the specified DynamoDB table.

3. Message Retrieval: Fetches stored chat messages from the DynamoDB table.

4. Message Clearing: Allows clearing of all stored messages for a given session.

5. Session Management: Supports multiple chat sessions using unique session IDs.


## Usage

This node is particularly useful for applications that require persistent storage of conversation history across sessions or need to scale chat memory storage using AWS DynamoDB. It’s ideal for chatbots, virtual assistants, or any AI application that benefits from maintaining context over time or across multiple interactions.


## Implementation Details

- Uses the ```text @aws-sdk/client-dynamodb``` for interacting with DynamoDB.
- Extends the ```text BufferMemory``` class from LangChain for compatibility with other LangChain components.
- Implements custom methods for adding, retrieving, and clearing messages in DynamoDB.
- Supports credential management for secure AWS authentication.

## Note
Ensure that the AWS credentials provided have the necessary permissions to read from and write to the specified DynamoDB table. Also, make sure that the table structure matches the expected format for storing chat messages.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
