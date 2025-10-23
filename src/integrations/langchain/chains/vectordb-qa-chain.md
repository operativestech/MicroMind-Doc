---
description: QA chain for vector databases.
---

# VectorDB QA Chain

<figure><img src="../../../.gitbook/assets/image (41).png" alt="" width="339"><figcaption><p>VectorDB QA Chain Node</p></figcaption></figure>

The VectorDB QA Chain is a question-answering system that combines vector database retrieval with language model processing to provide accurate answers based on a given knowledge base stored in a vector database.

## Parameters

1. Language Model (Required)

  -  Type: BaseLanguageModel
  -  Description: The language model used for generating answers.

2. Vector Store Retriever (Required)

  -  Type: BaseRetriever
  -  Description: The vector store used for storing and retrieving document embeddings.

3. Input Moderation (Optional)

  -  Type: Moderation[]
  -  Description: Moderation tools to detect and prevent harmful input.
  -  List: true


## How It Works

1. The chain receives a user question.
2. If input moderation is enabled, it checks the input for potential harmful content.
3. The vector store retrieves relevant documents based on the similarity between the question and stored document embeddings.
4. The retrieved documents are combined with the original question to form a prompt for the language model.
5. The language model generates an answer based on the prompt and retrieved context.
6. The final answer is returned as output.

The VectorDB QA Chain node provides a powerful solution for building AI-powered question-answering systems that can efficiently process and retrieve information from large document collections. By leveraging vector databases for fast similarity search and combining it with advanced language model processing, it enables the creation of intelligent systems that can provide accurate, context-aware answers to user queries. 

This node is particularly valuable in scenarios where quick information retrieval from vast knowledge bases is crucial, such as in enterprise search systems, technical support platforms, or educational resources.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
