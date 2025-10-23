---
description: Google vertexAI API to generate embeddings for a given text.
---

# Google VertexAI Embeddings

<figure><img src="../../../.gitbook/assets/image (8) (1) (1) (1) (1) (1).png" alt="" width="301"><figcaption><p>Google VertexAI Embeddings Node</p></figcaption></figure>

The GoogleVertexAIEmbedding_Embeddings node is a component that integrates Google Vertex AI’s embedding capabilities into a larger system. It’s designed to generate embeddings for given text using Google’s Vertex AI API.

## Parameters

### Credential (Optional)

  - Type: googleVertexAuth
  - Description: Google Vertex AI credential. Not required if using a GCP service like Cloud Run or if default credentials are installed on the local machine.

### Inputs

- Model Name:
    - Type: Asynchronous options
    - Default: “textembedding-gecko@001”
    - Load Method: listModels (retrieves available embedding models)

## Initialization

The node initializes a GoogleVertexAIEmbeddings instance with the following potential configurations:

  - Google Application Credential File Path
  - Google Application Credential JSON
  - Project ID
  - Model Name

## Usage

This node is typically used in workflows that require text embeddings, such as:

  - Semantic search
  - Text classification
  - Clustering
  - Recommendation systems
​
## Implementation Details

1. The node first retrieves credential data and input parameters.
2. It then configures authentication options based on the provided credentials.
3. A GoogleVertexAIEmbeddings instance is created with the specified model and authentication options.
4. The initialized model is returned, ready to generate embeddings for input text.

## Error Handling

The node includes error checks for:

  - Missing Google Application Credential
  - Conflicting credential inputs
​
## Integration

This node is designed to work within a larger system, likely a workflow or pipeline for natural language processing tasks. It can be connected to other nodes that require text embeddings as input.

​
## Notes

- The node uses the @langchain/community library for the GoogleVertexAIEmbeddings implementation.
- It supports dynamic loading of available embedding models.
- The node is flexible in terms of authentication, supporting both file-based and JSON-based credentials.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
