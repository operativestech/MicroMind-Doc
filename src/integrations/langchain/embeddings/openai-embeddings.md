---
description: OpenAI API to generate embeddings for a given text.
---

# OpenAI Embeddings

<figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1) (1) (1) (1).png" alt="" width="305"><figcaption><p>OpenAI Embeddings Node</p></figcaption></figure>

The OpenAI Embeddings node is used to generate embeddings for given text using the OpenAI API. Embeddings are vector representations of text that capture semantic meaning, allowing for efficient comparison and analysis of textual data.

## Parameters

### Credential (Required)

  - Label: Connect Credential
  - Name: credential
  - Type: credential
  - Credential Names: openAIApi
​
### Inputs

1. Model Name

    - Type: asyncOptions
    - Default: ```code “text-embedding-ada-002”```
    - Description: The name of the OpenAI model to use for generating embeddings.

2. Strip New Lines (Optional)

    - Type: boolean
    - Description: Whether to remove new line characters from the input text.

3. Batch Size (Optional)

    - Type: number
    - Description: The number of texts to process in a single API call.

4. Timeout (Optional)

    - Type: number
    - Description: The maximum time (in milliseconds) to wait for the API response.

5. BasePath (Optional)

    - Type: string
    - Description: The base URL for API requests, useful for using alternative API endpoints.

6. Dimensions (Optional)

    - Type: number
    - Description: The number of dimensions for the output embedding vectors.

## Functionality

1. The node first loads the available embedding models using the listModels method.
2. During initialization, it processes the input parameters and credential data.
3. It then creates an instance of OpenAIEmbeddings with the specified configuration.
4. This instance can be used to generate embeddings for given text inputs.

## Use Cases

- Text similarity comparison
- Document clustering
- Semantic search
- Input preparation for machine learning models
- Content recommendation systems
​
## Notes

- The node uses the @langchain/openai package for interaction with the OpenAI API.
- It supports various additional parameters for fine-tuning the embedding process.
- The actual embedding generation occurs when the initialized node is used in a workflow.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
