---
description: >-
  Cohere Rerank indexes the documents from most to least semantically relevant
  to the query.
---

# Cohere Rerank Retriever

<figure><img src="../../../.gitbook/assets/image (130).png" alt="" width="299"><figcaption><p>Cohere Rerank Retriever Node</p></figcaption></figure>

The Cohere Rerank Retriever is a specialized retriever that uses Cohere’s reranking capabilities to improve the relevance of retrieved documents. It works by first retrieving documents from a base vector store retriever, then reranking these documents based on their semantic relevance to the query using Cohere's AI models.

## Input Parameters

1. **Vector Store Retriever** (required)

    - Type: VectorStoreRetriever

    - Description: The base retriever to fetch initial documents from a vector store.

2. **Model Name** (optional)

    - Type: Options

    - Default: “rerank-english-v2.0”

    - Options:

        - rerank-english-v2.0

        - rerank-multilingual-v2.0

    - Description: The Cohere model to use for reranking.

3. **Query** (optional)

    - Type: string

    - Description: Specific query to retrieve documents. If not provided, the user's question will be used.

4. **Top K** (optional)

    - Type: number

    - Default: Inherits from base retriever, or 4 if not specified

    - Description: Number of top results to fetch after reranking.

5. **Max Chunks Per Doc** (optional)

    - Type: number

    - Default: 10

    - Description: Maximum number of chunks to produce internally from a document.

## Outputs

1. Cohere Rerank Retriever

  - Type: BaseRetriever

  - Description: The configured Cohere Rerank Retriever object.

2. Document

  - Type: Document[]

  - Description: Array of retrieved and reranked document objects, containing metadata and page content.

3. Text

  - Type: string

  - Description: Concatenated string of page content from all retrieved and reranked documents.

## How It Works

1. The node first initializes a base retriever (usually a vector store retriever).

2. It then creates a CohereRerank compressor using the provided API key, model, and parameters.

3. A ContextualCompressionRetriever is created, combining the base retriever and the Cohere reranker.

4. When queried, it retrieves documents from the base retriever and reranks them using Cohere’s AI.

5. The output can be the retriever itself, the reranked documents, or the concatenated text of the documents.

## Use Cases

- Improving relevance of document retrieval in question-answering systems.

- Enhancing search results by considering semantic similarity.

- Creating more accurate document summaries by focusing on the most relevant parts.


## Notes

- This node requires a Cohere API key to function.

- The effectiveness of the reranking depends on the quality of the initial retrieval and the chosen Cohere model.

- Consider the trade-off between retrieval speed and accuracy when adjusting the Top K and Max Chunks Per Doc parameters.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
