---
description: Voyage AI API to generate embeddings for a given text.
---

# VoyageAI Embeddings

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="307"><figcaption><p>VoyageAI Embeddings Node</p></figcaption></figure>

The VoyageAI Embeddings node is a component that integrates the Voyage AI API for generating embeddings from text. It’s part of a larger system for natural language processing and machine learning tasks.

## Parameters

### Credential (Required)

- Type: voyageAIApi
- Required Parameters:
    - ```text apiKey```: The API key for accessing the Voyage AI service
    - ```text endpoint```: The API endpoint for the Voyage AI service (optional)

### Inputs

- Model Name:
    - Type: Asynchronous dropdown
    - Default: ‘voyage-2’
    - Available options are dynamically loaded using the ```text listModels`` method

## Initialization

The node initializes a VoyageEmbeddings instance with the following:

1. Retrieves the selected model name
2. Fetches credential data (API key and optional endpoint)
3. Creates a VoyageEmbeddings object with the API key and model name
4. Sets a custom API URL if provided in the credentials

## Usage

This node is typically used in a pipeline where text needs to be converted into numerical vector representations. These embeddings can then be used for:

- Semantic search
- Text classification
- Clustering similar texts
- Measuring text similarity
- Input for other machine learning models

## Integration

The node is designed to work within a larger system, likely a graphical interface for building NLP pipelines. It can be connected to other nodes for data input and further processing of the generated embeddings.


## Dependencies

@langchain/community/embeddings/voyage: Provides the VoyageEmbeddings class
Various utility functions from the parent project for credential management, model loading, and base class retrieval

## Note

This node is part of a modular system and is expected to be used alongside other components for building comprehensive NLP workflows.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
