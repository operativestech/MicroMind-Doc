---
description: Search documents with scores from vector store.
---

# VectorStore To Document

<figure><img src="../../../.gitbook/assets/image (106).png" alt="" width="324"><figcaption><p>VectorStore To Document Node</p></figcaption></figure>

The VectorStore To Document node is a component in the Document Loaders category that allows you to search and retrieve documents with scores from a vector store. It converts the retrieved documents into either a document object array or a concatenated text string.

## Inputs

### Required Parameters

- **Vector Store**: The vector store to search documents from

### Optional Parameters

- **Query**: 
  - Query to retrieve documents from the vector database. If not specified, the user question will be used
  - Accepts variables
- **Minimum Score (%)**: Minimum score for embedding documents to be included

## Outputs

- **Document**: Array of document objects containing:
  - metadata: File metadata and custom fields
  - pageContent: Extracted text content
- **Text**: Concatenated string of all extracted content


{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
