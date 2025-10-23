---
description: >-
  QA Chain that automatically picks an appropriate vector store from multiple
  retrievers.
---

# Multi Retrieval QA Chain

<figure><img src="../../../.gitbook/assets/image (34).png" alt="" width="333"><figcaption><p>Multi Retrieval QA Chain Node</p></figcaption></figure>

The Multi Retrieval QA Chain is an advanced question-answering system that automatically selects and utilizes the most appropriate vector store retriever from multiple options based on the input query. It’s designed to provide accurate answers by dynamically choosing the best-suited knowledge base for each specific question.


## Parameters

- Language Model (Required)

  -  Type: BaseLanguageModel
  -  Description: The language model used for generating responses and selecting retrievers.

- Vector Store Retriever (Required)

  -  Type: VectorStoreRetriever
  -  Description: An array of vector store retrievers, each containing a vector store, name, and description.
  -  List: true

- Return Source Documents (Optional)

  -  Type: boolean
  -  Description: Whether to return the source documents used to generate the answer.

- Input Moderation (Optional)

  -  Type: Moderation[]
  -  Description: Moderation tools to detect and prevent harmful input.
  -  List: true

## Input

A string containing the user’s question or query.

## Output

- If Return Source Documents is false:
  -  A string containing the answer to the user’s question.
- If Return Source Documents is true:
  -  An object containing:
    -   text: The answer to the user’s question.
    -   sourceDocuments: An array of documents used to generate the answer.

## How It Works

1. The chain receives a user question.
2. If input moderation is enabled, it checks the input for potential harmful content.
3. The language model analyzes the question to determine which vector store retriever is most appropriate.
4. The selected retriever fetches relevant documents from its associated vector store.
5. The language model generates an answer based on the retrieved documents and the original question.
6. The answer (and optionally source documents) is returned as output.

## Special Features

- Dynamic Retriever Selection: Automatically chooses the most appropriate vector store retriever for each query.
- Multiple Knowledge Base Support: Can handle questions across various topics or domains using specialized retrievers.
- Flexible Configuration: Allows for easy addition or modification of vector store retrievers.
- Input Moderation: Optional safeguards against inappropriate or harmful inputs.
- Source Attribution: Option to return source documents for transparency and verification.
- Improved Accuracy: By using specialized retrievers, it can provide more accurate and relevant answers.

## Notes

- The effectiveness of the chain depends on the quality and diversity of the provided vector store retrievers.
- Careful design of retriever descriptions is crucial for accurate selection.
- The chain may require more computation time compared to single-retriever chains due to the selection process.
- It’s important to ensure that the language model is capable of accurately selecting between retrievers.
- For best results, vector store retrievers should cover distinct knowledge domains or document types.
- Regular analysis of chain performance can help identify areas where new retrievers might be needed.
- The chain supports streaming responses for real-time interaction in compatible environments.

The Multi Retrieval QA Chain node provides a sophisticated solution for creating highly adaptable question-answering systems that can handle diverse queries across multiple knowledge domains. By dynamically selecting the most appropriate vector store retriever for each question, it combines the specificity of specialized knowledge bases with the flexibility of a general-purpose system.

This node is particularly valuable in scenarios where the input questions can vary widely in topic or require access to different types of information, such as in comprehensive customer support systems, multi-domain research tools, or versatile AI assistants. Its ability to adapt to different types of queries makes it a powerful component for building more intelligent and responsive information retrieval systems.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
