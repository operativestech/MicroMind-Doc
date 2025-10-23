---
description: Reciprocal Rank Fusion to re-rank search results by multiple query generation.
---

# Reciprocal Rank Fusion Retriever

<figure><img src="../../../.gitbook/assets/image (146).png" alt="" width="303"><figcaption><p>Reciprocal Rank Fusion Retriever Node</p></figcaption></figure>

The Reciprocal Rank Fusion (RRF) Retriever is a specialized retriever that uses the Reciprocal Rank Fusion algorithm to re-rank search results obtained from multiple query generations. This node enhances the retrieval process by generating synthetic queries and combining their results for improved relevance.

## Input Parameters

1. Vector Store Retriever (required)

    - Type: VectorStoreRetriever

    - Description: The base retriever used for initial document retrieval.

2. Language Model (required)

    - Type: BaseLanguageModel

    - Description: The language model used for generating synthetic queries.

3. Query (optional)

    - Type: string

    - Description: Custom query to retrieve documents. If not specified, the user’s question will be used.

4. Query Count (optional)

    - Type: number

    - Default: 4

    - Description: Number of synthetic queries to generate.

5. Top K (optional)

    - Type: number

    - Description: Number of top results to fetch. Defaults to the TopK of the Base Retriever.

6. Constant (optional)

    - Type: number

    - Default: 60

    - Description: A constant added to the rank, controlling the balance between high-ranked and lower-ranked items.


## Outputs

1. Reciprocal Rank Fusion Retriever

  - Type: RRFRetriever, BaseRetriever

  - Description: The initialized RRF retriever object.

2. Document

  - Type: Document, json

  - Description: Array of document objects containing metadata and pageContent.

3. Text

  - Type: string, json

  - Description: Concatenated string from pageContent of retrieved documents.


## How It Works

1. The node initializes a ReciprocalRankFusion object using the provided language model, base retriever, and configuration parameters.

2. It then wraps this object in a ContextualCompressionRetriever for additional processing.

3. Depending on the selected output, the node can return:

    - The retriever object itself

    - An array of relevant documents

    - A concatenated text of the retrieved documents' content


## Use Cases

- Improving search relevance in document retrieval systems

- Enhancing question-answering systems with more diverse and relevant context

- Boosting the performance of RAG (Retrieval-Augmented Generation) applications


## Notes

- The node uses escape character handling for text output to ensure proper formatting.

- The synthetic query generation and re-ranking process happens internally within the ReciprocalRankFusion class.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
