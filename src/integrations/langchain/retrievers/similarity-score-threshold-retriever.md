---
description: Return results based on the minimum similarity percentage.
---

# Similarity Score Threshold Retriever

<figure><img src="../../../.gitbook/assets/image (147).png" alt="" width="301"><figcaption><p>Similarity Score Threshold Retriever Node</p></figcaption></figure>

The Similarity Score Threshold Retriever is a specialized retriever that returns results based on a minimum similarity percentage. It's designed to filter and retrieve documents from a vector store that meet or exceed a specified similarity threshold.

## Input Parameters

1. Vector Store (required)

    - Type: VectorStore

    - Description: The vector store to retrieve documents from.

2. Query (optional)

    - Type: string

    - Description: The query to retrieve documents. If not specified, the user’s question will be used.

    - Accepts variables: Yes

3. Minimum Similarity Score (%) (required)

    - Type: number

    - Default: 80

    - Description: The minimum similarity score (as a percentage) for retrieved documents.

4. Max K (optional, additional parameter)

    - Type: number

    - Default: 20

    - Description: The maximum number of results to fetch.

5. K Increment (optional, additional parameter)

    - Type: number

    - Default: 2

    - Description: How much to increase K by each time. It’ll fetch N results, then N + kIncrement, then N + kIncrement * 2, etc.


## Outputs

1. Similarity Threshold Retriever

  - Type: SimilarityThresholdRetriever

  - Description: The configured retriever object.

2. Document

  - Type: Document[] (array of Document objects)

  - Description: Array of document objects containing metadata and pageContent.

3. Text

  - Type: string

  - Description: Concatenated string from pageContent of retrieved documents.


## Functionality

The node creates a ScoreThresholdRetriever from the provided vector store and configuration parameters. It can output either the retriever itself, the retrieved documents, or the concatenated text content of the retrieved documents, depending on the selected output.

When retrieving documents or text, it uses either the provided query or the input string to fetch relevant documents. For text output, it concatenates the page content of all retrieved documents and handles escape characters.


## Use Cases

- Retrieving highly relevant documents from a large corpus

- Filtering out less relevant information in information retrieval tasks

- Ensuring a minimum quality threshold for retrieved content in question-answering systems

- Fine-tuning document retrieval for specific similarity requirements in various NLP applications

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
