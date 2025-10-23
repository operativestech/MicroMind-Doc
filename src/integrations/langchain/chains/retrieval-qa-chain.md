---
description: QA chain to answer a question based on the retrieved documents.
---

# Retrieval QA Chain

<figure><img src="../../../.gitbook/assets/image (38).png" alt="" width="337"><figcaption><p>Retrieval QA Chain Node</p></figcaption></figure>

The Retrieval QA Chain is a powerful question-answering system that combines document retrieval with language model processing to provide accurate answers based on a given knowledge base.

## Parameters

1. Language Model (Required)

  -  Type: BaseLanguageModel
  -  Description: The language model used for generating answers.

2. Vector Store Retriever (Required)

  -  Type: BaseRetriever
  -  Description: The retriever used to fetch relevant documents from a vector store.

3. Input Moderation (Optional)

  -  Type: Moderation[]
  -  Description: Moderation tools to detect and prevent harmful input.
  -  List: true

## How It Works

1. The chain receives a user question.
2. If input moderation is enabled, it checks the input for potential harmful content.
3. The vector store retriever fetches relevant documents based on the question.
4. The language model generates an answer based on the processed documents and the original question.
5. The answer (and optionally source documents) is returned as output.

## Use Cases

- Building question-answering systems based on specific knowledge bases
- Creating AI assistants with access to large document repositories
- Implementing intelligent search functionality for databases or document collections
- Developing automated customer support systems with access to product documentation
- Creating educational tools that can answer questions based on course materials

## Notes

- The quality of answers depends on both the underlying language model and the relevance of retrieved documents.
- The choice of Chain Option can significantly impact performance and accuracy for different types of queries.
- Custom system messages can be used to guide the AI’s behavior and response style.
- The chain supports streaming responses for real-time interaction in compatible environments.
- Proper error handling and input validation should be implemented for production use.
- The effectiveness of the chain can vary depending on the quality and organization of the knowledge base.

The Retrieval QA Chain node provides a robust solution for building AI-powered question-answering systems with access to large document repositories. By combining efficient document retrieval with advanced language model processing, it enables the creation of intelligent systems that can provide accurate, context-aware answers to user queries. This node is particularly valuable in scenarios where answers need to be derived from a specific body of knowledge, such as in specialized customer support, educational platforms, or domain-specific research tools.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
