---
description: Cohere API to generate embeddings for a given text
---

# Cohere Embeddings

<figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="306"><figcaption><p>Cohere Embeddings Node</p></figcaption></figure>

The Cohere Embeddings node is used to generate embeddings for given text using the Cohere API. Embeddings are vector representations of text that capture semantic meaning, which can be used for various natural language processing tasks such as search, classification, and clustering.

## Parameters

### Credential (Required)

- Type: cohereApi
- Required Fields: cohereApiKey

### Inputs

1. Model Name

- Type: asyncOptions
- Default: “embed-english-v2.0”
- Description: The name of the Cohere embedding model to use.
- Note: Available models are loaded dynamically.

2. Input Type

- Type: options
- Default: “search_query”
- Options:
    - search_document: For encoding documents to store in a vector database for search use-cases.
    - search_query: For querying a vector database to find relevant documents.
    - classification: For using embeddings as input to a text classifier.
    - clustering: For clustering embeddings.
- Description: Specifies the type of input passed to the model. Required for embedding models v3 and    higher.

## Functionality

1. The node first retrieves the necessary credentials (Cohere API key) and input parameters.
2. It then initializes a CohereEmbeddings instance with the provided configuration.
3. The resulting model can be used to generate embeddings for given text inputs.

## Use Cases

1. Semantic Search: Generate embeddings for documents and queries to perform semantic search operations.
2. Text Classification: Create embeddings as input features for text classification tasks.
3. Document Clustering: Generate embeddings to group similar documents together.
4. Information Retrieval: Enhance document retrieval systems by using semantic embeddings.
​
## Notes

- The node dynamically loads available embedding models specific to Cohere.
- It supports different input types, allowing for optimization based on the specific use case (search, classification, clustering).
- The Cohere API key is required and should be securely stored and accessed.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
