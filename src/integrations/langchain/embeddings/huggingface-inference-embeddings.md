---
description: HuggingFace Inference API to generate embeddings for a given text.
---

# HuggingFace Inference Embeddings

<figure><img src="../../../.gitbook/assets/image (9) (1) (1) (1) (1) (1).png" alt="" width="297"><figcaption><p>HuggingFace Inference Embeddings Node</p></figcaption></figure>

The HuggingFace Inference Embeddings node is a component used to generate embeddings for given text using the HuggingFace Inference API. This node is part of the Embeddings category and leverages HuggingFace’s powerful language models to create vector representations of text.

## Parameters

### Credential
- Label: Connect Credential
- Name: credential
- Type: credential
- Credential Names: huggingFaceApi

### Inputs

1. Model

    - Label: Model
    - Name: modelName
    - Type: string
    - Description: The name of the HuggingFace model to use for embeddings. Leave blank if using a custom inference endpoint.
    - Placeholder: sentence-transformers/distilbert-base-nli-mean-tokens
    - Optional: Yes

2. Endpoint

    - Label: Endpoint
    - Name: endpoint
    - Type: string
    - Description: The URL of your custom inference endpoint, if using one.
    - Placeholder: https://xyz.eu-west-1.aws.endpoints.huggingface.cloud/sentence-transformers/all-MiniLM-L6-v2
    - Optional: Yes
    
## Initialization
The node initializes by creating an instance of ```text HuggingFaceInferenceEmbeddings``` with the following steps:

1. Retrieves the HuggingFace API key from the provided credentials.
2. Sets up the configuration object with the API key.
3. If a model name is provided, it’s added to the configuration.
4. If a custom endpoint is provided, it’s added to the configuration.
5. Creates and returns a new HuggingFaceInferenceEmbeddings instance with the configured parameters.

## Usage
This node is typically used in workflows where text needs to be converted into numerical vector representations. Common use cases include:

- Text similarity comparisons
- Document clustering
- Input preparation for machine learning models
- Semantic search implementations

By leveraging HuggingFace’s pre-trained models or custom-deployed endpoints, users can easily generate high-quality embeddings for a wide range of natural language processing tasks.


{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
