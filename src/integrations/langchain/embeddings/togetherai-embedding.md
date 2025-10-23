---
description: TogetherAI Embedding models to generate embeddings for a given text.
---

# TogetherAI Embedding

<figure><img src="../../../.gitbook/assets/image (2) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="301"><figcaption><p>TogetherAI Embedding Node</p></figcaption></figure>

The TogetherAIEmbedding node is used to generate embeddings for given text using TogetherAI’s embedding models. It’s part of the Embeddings category in the system.

## Parameters

### Credential (Required)

  - Label: Connect Credential
  - Name: credential
  - Type: credential
  - Credential Names: togetherAIApi

### Inputs

1. Cache (Optional)

    - Label: Cache
    - Name: cache
    - Type: BaseCache

2. Model Name (Required)

    - Label: Model Name
    - Name: modelName
    - Type: string
    - Placeholder: sentence-transformers/msmarco-bert-base-dot-v5
    - Description: Refers to the specific embedding model to use. Users can find available models on the TogetherAI embedding models page.

## Functionality

  1. The node initializes by retrieving the necessary credentials and input parameters.
  2. It sets up a TogetherAIEmbeddings object with the provided model name and API key.
  3. The initialized model can then be used to generate embeddings for text inputs.

## Usage

This node is particularly useful in natural language processing pipelines where text needs to be converted into numerical vectors (embeddings). These embeddings can be used for various downstream tasks such as semantic search, text classification, or clustering.


## Integration

The TogetherAIEmbedding node is designed to work seamlessly within a larger system, likely a node-based workflow environment for AI and machine learning tasks. It can be connected to other nodes that require text embeddings as input or to nodes that process the resulting embeddings further.


## Note

Users need to have valid TogetherAI API credentials to use this node. The API key is securely handled through the credential system of the parent application.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
