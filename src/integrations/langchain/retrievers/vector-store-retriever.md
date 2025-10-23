---
description: Store vector store as retriever to be later queried by MultiRetrievalQAChain.
---

# Vector Store Retriever

<figure><img src="../../../.gitbook/assets/image (148).png" alt="" width="301"><figcaption><p>Vector Store Retriever Node</p></figcaption></figure>

The Vector Store Retriever node is a component used in retrieval-based systems, particularly for storing and querying vector representations of data. It's designed to be used with MultiRetrievalQAChain, making it useful for question-answering tasks that require retrieval from multiple sources.

## Input Parameters

1. Vector Store

    - Label: Vector Store

    - Name: vectorStore

    - Type: VectorStore

    - Description: The vector store to be used as the basis for the retriever.

2. Retriever Name

    - Label: Retriever Name

    - Name: name

    - Type: string

    - Placeholder: “netflix movies”

    - Description: A unique identifier for the retriever.

3. Retriever Description

    - Label: Retriever Description

    - Name: description

    - Type: string

    - Rows: 3

    - Description: A brief explanation of when to use this specific vector store retriever.

    - Placeholder: "Good for answering questions about netflix movies"

## Output

The node initializes and returns a VectorStoreRetriever object, which encapsulates:

- The provided vector store

- The specified name

- The given description


## Usage

This node is typically used in workflows where:

1. You have pre-processed data stored in a vector format.

2. You need to retrieve this data efficiently based on similarity searches.

3. You want to integrate this retrieval mechanism into a larger question-answering or information retrieval system.


## Integration

The Vector Store Retriever is designed to work seamlessly with other components in a langchain-based system, particularly with MultiRetrievalQAChain for complex question-answering tasks that require querying multiple data sources.


## Implementation Notes

- The node uses the VectorStore class from ‘@langchain/core/vectorstores’.

- It implements the INode interface, ensuring compatibility with the broader node-based architecture.

- The init method is responsible for creating and returning the VectorStoreRetriever object based on the provided inputs.


## Best Practices

- Provide clear and descriptive names for your retrievers to easily identify them in complex workflows.

- Use the description field to specify the domain or type of questions this retriever is best suited for.

- Ensure that the vector store provided is properly initialized and contains relevant, high-quality data for optimal retrieval performance.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
