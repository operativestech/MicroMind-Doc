---
description: OpenAI API to generate embeddings for a given text.
---

# OpenAI Embeddings Custom

<figure><img src="../../../.gitbook/assets/image (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="300"><figcaption><p>OpenAI Embeddings Custom Node</p></figcaption></figure>

The OpenAI Embeddings Custom node is a component designed to generate embeddings for given text using the OpenAI API. It’s an extension of the standard OpenAI Embeddings functionality, offering additional customization options.

## Parameters

### Credential (Required)
  - Type: openAIApi
  - Required Fields: openAIApiKey

### Inputs

1. Strip New Lines (optional)

    - Type: boolean
    - Description: Removes new line characters from the input text if set to true.

2. Batch Size (optional)

    - Type: number
    - Description: Sets the number of texts to process in a single API call.

3. Timeout (optional)

    - Type: number
    - Description: Sets the maximum time (in milliseconds) to wait for an API response.

4. BasePath (optional)

    - Type: string
    - Description: Specifies a custom base URL for the OpenAI API.

5. Model Name (optional)

    - Type: string
    - Description: Specifies the OpenAI model to use for generating embeddings.

6. Dimensions (optional)

    - Type: number
    - Description: Sets the number of dimensions for the output embeddings.
  ​
## Functionality

The node initializes an OpenAIEmbeddings instance with the provided parameters. It retrieves the OpenAI API key from the user’s credentials and applies any additional parameters specified in the node configuration. The resulting embeddings model can be used in downstream tasks that require text embeddings.

​
## Use Cases
  - Text similarity comparison
  - Document clustering
  - Semantic search
  - Feature extraction for machine learning models
  - Content-based recommendation systems
​
## Notes
  - This custom node allows for more fine-grained control over the embedding process compared to the standard OpenAI Embeddings node.
  - Users should be mindful of their API usage, as generating embeddings can consume a significant number of tokens.
  - The ‘dimensions’ parameter allows users to specify the size of the embedding vectors, which can be useful for compatibility with specific models or applications.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
