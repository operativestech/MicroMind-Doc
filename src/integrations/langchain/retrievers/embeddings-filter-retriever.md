---
description: >-
  A document compressor that uses embeddings to drop documents unrelated to the
  query.
---

# Embeddings Filter Retriever

<figure><img src="../../../.gitbook/assets/image (131).png" alt="" width="299"><figcaption><p>Embeddings Filter Retriever Node</p></figcaption></figure>

The Embeddings Filter Retriever is a specialized retriever that uses embeddings to filter out documents unrelated to a given query. It’s designed to improve the relevance of retrieved documents by comparing their embeddings to the query embedding.

## Description

This node implements a document compressor that uses embeddings to drop documents unrelated to the query. It combines a base retriever (typically a vector store retriever) with an embeddings filter to refine the retrieval process.

## Input Parameters

1. Vector Store Retriever (baseRetriever)

    - Type: VectorStoreRetriever

    - Description: The base retriever to use for initial document retrieval.

2. Embeddings (embeddings)

    - Type: Embeddings

    - Description: The embeddings model to use for encoding queries and documents.

3. Query (query)

    - Type: string

    - Optional: Yes

    - Description: Specific query to retrieve documents. If not provided, the user's question will be used.

4. Similarity Threshold (similarityThreshold)

    - Type: number

    - Default: 0.8

    - Optional: Yes

    - Description: Threshold for determining when two documents are similar enough to be considered redundant.

5. K (k)

    - Type: number

    - Default: 20

    - Optional: Yes

    - Description: The number of relevant documents to return. Can be set to undefined, in which case similarity_threshold must be specified.

## Outputs

1. Embeddings Filter Retriever (retriever)

    - Type: EmbeddingsFilterRetriever, BaseRetriever

    - Description: The configured retriever object.

2. Document (document)

    - Type: Document, json

    - Description: Array of document objects containing metadata and pageContent.

3. Text (text)

    - Type: string, json

    - Description: Concatenated string from pageContent of retrieved documents.

## Functionality

The Embeddings Filter Retriever works by:

1. Using the base retriever to fetch an initial set of documents.

2. Applying an embeddings filter to refine the results based on similarity to the query.

3. Returning either the retriever object, the filtered documents, or the concatenated text of the documents based on the specified output.


## Use Cases

- Improving relevance in document retrieval tasks.

- Reducing noise in retrieved documents for more focused language model inputs.

- Enhancing question-answering systems by providing more relevant context.


## Notes

- Either 'k' or 'similarity_threshold' must be specified for proper functioning.

- The node uses the ContextualCompressionRetriever and EmbeddingsFilter from the LangChain library.

- It handles escape characters in the output text when returning concatenated document content.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
