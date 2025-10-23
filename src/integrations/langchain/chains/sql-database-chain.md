---
description: Answer questions over a SQL database.
---

# Sql Database Chain

<figure><img src="../../../.gitbook/assets/image (40).png" alt="" width="332"><figcaption><p>Sql Database Chain Node</p></figcaption></figure>

The SQL Database node enables seamless integration with relational databases using SQL, allowing you to query, retrieve, and manipulate structured data within your workflows. This node is designed for flexible, intelligent interactions with SQL databases, supporting a wide range of data-driven tasks.

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

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
