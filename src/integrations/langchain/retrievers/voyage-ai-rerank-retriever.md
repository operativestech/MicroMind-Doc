---
description: >-
  Voyage AI Rerank indexes the documents from most to least semantically
  relevant to the query.
---

# Voyage AI Rerank Retriever

<figure><img src="../../../.gitbook/assets/image (149).png" alt="" width="302"><figcaption><p>Voyage AI Rerank Retriever Node</p></figcaption></figure>

The Voyage AI Rerank Retriever is a specialized retriever node that enhances document retrieval by reranking results based on semantic relevance to the query. It uses Voyage AI’s reranking models to improve the quality of retrieved documents.

## Input Parameters

1. Vector Store Retriever (required)

    - Type: VectorStoreRetriever

    - Description: The base retriever to enhance with reranking

2. Model Name (optional)

    - Type: options

    - Options:

        - rerank-lite-1

        - rerank-1

    - Default: rerank-lite-1

3. Query (optional)

    - Type: string

    - Description: Specific query to use for retrieval. If not provided, the user's question will be used.

4. Top K (optional)

    - Type: number

    - Description: Number of top results to fetch. Defaults to the TopK of the Base Retriever or 4 if not specified.


## Outputs

1. Voyage AI Rerank Retriever

    - Type: VoyageAIRerankRetriever, BaseRetriever

    - Description: The configured retriever object

2. Document

    - Type: Document, json

    - Description: Array of document objects containing metadata and pageContent

3. Text

    - Type: string, json

    - Description: Concatenated string from pageContent of retrieved documents

## Functionality

The node works by wrapping a base vector store retriever with a ContextualCompressionRetriever. This compression retriever uses a VoyageAIRerank compressor to reorder the documents retrieved by the base retriever according to their semantic relevance to the query.

The process involves:

1. Retrieving documents from the base vector store

2. Applying the Voyage AI reranking model to these documents

3. Returning the reordered results

This approach can significantly improve the quality of retrieved documents, especially for complex or nuanced queries where semantic understanding is crucial.


## Use Cases

- Enhancing search results in document repositories

- Improving question-answering systems by providing more relevant context

- Refining information retrieval in research and analysis tasks


## Note

The effectiveness of this node depends on the quality of the base retriever and the appropriateness of the chosen Voyage AI model for the specific use case.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
