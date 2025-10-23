---
description: >-
  Iterate over the initially returned documents and extract, from each, only the
  content that is relevant to the query.
---

# LLM Filter Retriever

<figure><img src="../../../.gitbook/assets/image (144).png" alt="" width="297"><figcaption><p>LLM Filter Retriever Node</p></figcaption></figure>

The LLM Filter Retriever is a specialized retriever that enhances the document retrieval process by using a language model to filter and extract relevant content from initially retrieved documents.

## Input Parameters

1. Vector Store Retriever

  - Name: baseRetriever

  - Type: VectorStoreRetriever

  - Description: The underlying retriever used to fetch initial documents.

2. Language Model

  - Name: model

  - Type: BaseLanguageModel

  - Description: The language model used for filtering and extracting relevant content.

3. Query (Optional)

  - Name: query

  - Type: string

  - Description: Query to retrieve documents from the retriever. If not specified, the user’s question will be used.

  - Accepts variables: Yes


## Outputs

1. LLM Filter Retriever

  - Name: retriever

  - Type: LLMFilterRetriever, BaseRetriever

  - Description: The configured LLM Filter Retriever object.

2. Document

  - Name: document

  - Type: Document, json

  - Description: Array of document objects containing metadata and pageContent.

3. Text

  - Name: text

  - Type: string, json

  - Description: Concatenated string from pageContent of filtered documents.


## Functionality

The LLM Filter Retriever uses a ContextualCompressionRetriever with an LLMChainExtractor. It works as follows:

1. The base retriever (e.g., a vector store retriever) fetches initial documents.

2. The language model (LLM) is used to create an LLMChainExtractor, which serves as the base compressor.

3. The ContextualCompressionRetriever combines the base retriever and the LLM-based compressor.

4. When retrieving documents, the compressor filters and extracts only the relevant content from each document based on the query.

This approach helps to reduce noise and improve the relevance of the retrieved information, especially useful in scenarios where documents might contain a mix of relevant and irrelevant content.


## Usage

This node is particularly useful in workflows where:

- The initial document retrieval might return lengthy or partially relevant documents.

- You need to extract specific, query-relevant information from a larger context.

- You want to improve the quality and relevance of retrieved information before passing it to subsequent processing steps or presenting it to the user.


## Note

Ensure that a suitable language model is connected to this node, as it's crucial for the filtering and extraction process.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
