---
description: Use HyDE retriever to retrieve from a vector store.
---

# HyDE Retriever

<figure><img src="../../../.gitbook/assets/image (143).png" alt="" width="302"><figcaption><p>HyDE Retriever Node</p></figcaption></figure>

The HyDE (Hypothetical Document Embeddings) Retriever is a specialized retrieval component used to fetch relevant documents from a vector store. It leverages a language model to generate hypothetical answers or passages based on the input query, which are then used to retrieve similar documents from the vector store.

## Input Parameters

1. Language Model (required)

    - Type: BaseLanguageModel

    - Description: The language model used to generate hypothetical documents.

2. Vector Store (required)

    - Type: VectorStore

    - Description: The vector store to retrieve documents from.

3. Query (optional)

    - Type: string

    - Description: Specific query to retrieve documents. If not provided, the user's question will be used.

4. Select Defined Prompt (required)

    - Type: options

    - Description: Pre-defined prompt templates for different use cases.

    - Options: websearch, scifact, arguana, trec-covid, fiqa, dbpedia-entity, trec-news, mr-tydi

    - Default: websearch

5. Custom Prompt (optional)

    - Type: string

    - Description: A custom prompt template that overrides the defined prompt if provided.

6. Top K (optional)

    - Type: number

    - Description: Number of top results to fetch.

    - Default: 4


## Outputs

1. HyDE Retriever

    - Type: HydeRetriever

    - Description: The configured HyDE Retriever object.

2. Document

    - Type: Document[]

    - Description: An array of retrieved document objects containing metadata and page content.

3. Text

    - Type: string

    - Description: Concatenated string of page content from all retrieved documents.


## Usage

The HyDE Retriever is particularly useful in scenarios where traditional keyword-based retrieval might fall short. It's effective for:

  - Answering complex questions that require contextual understanding

  - Retrieving documents for topics with limited or ambiguous keywords

  - Improving retrieval performance in domain-specific applications

By generating a hypothetical answer or passage, the HyDE Retriever can capture the semantic intent of the query more effectively, leading to more relevant document retrieval.


## Note

The performance of the HyDE Retriever heavily depends on the quality of the language model and the appropriateness of the prompt template for the given task. Experimenting with different prompts and fine-tuning the language model for specific domains can significantly improve retrieval results.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
