---
description: MistralAI API to generate embeddings for a given text.
---

# MistralAI Embeddings

<figure><img src="../../../.gitbook/assets/image (10) (1) (1) (1).png" alt="" width="295"><figcaption><p>MistralAI Embeddings Node</p></figcaption></figure>

The MistralAI Embeddings node is a component that integrates the MistralAI API to generate embeddings for given text. Embeddings are vector representations of text that capture semantic meaning, useful for various natural language processing tasks.

## Parameters

### Credential
- Label: Connect Credential
- Name: credential
- Type: credential
- Credential Names: mistralAIApi

### Inputs

1. Model Name (Required)

  - Type: asyncOptions
  - Default: “mistral-embed”
  - Load Method: listModels

2. Batch Size (Optional)

  - Type: number
  - Default: 512
  - Step: 1

3. Strip New Lines (Optional)

  - Type: boolean
  - Default: true

4. Override Endpoint (Optional)

  - Type: string

## Functionality

1. The node initializes by loading the specified model and setting up the MistralAI Embeddings with the provided parameters.
2. It uses the MistralAI API key from the connected credential for authentication.
3. The node can handle batch processing of text for embedding generation.
4. It offers options to strip new lines from the input text and override the default API endpoint.
​
## Use Cases

- Text similarity comparison
- Semantic search
- Document classification
- Content-based recommendation systems

## Input/Output

- Input: Text data to be embedded
- Output: Vector representations (embeddings) of the input text

## Additional Notes

- The node dynamically loads available models using the listModels method.
- It supports customization of batch size for processing efficiency.
- The option to strip new lines can be useful for cleaning input text.
- Advanced users can override the default API endpoint if needed.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
