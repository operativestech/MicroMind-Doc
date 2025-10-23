---
description: Generate embeddings for a given text using open source model on Ollama.
---

# Ollama Embeddings

<figure><img src="../../../.gitbook/assets/image (11) (1) (1) (1).png" alt="" width="299"><figcaption><p>Ollama Embeddings Node</p></figcaption></figure>

The Ollama Embeddings node is used to generate embeddings for given text using open-source models on Ollama. It leverages the ```code OllamaEmbeddings``` class from the ```code @langchain/community/embeddings/ollama``` package.

## Parameters

### Inputs

1. Base URL (string)

    - Default: “http://localhost:11434”
    - The base URL for the Ollama API.

2. Model Name (string)

    - Placeholder: “llama2”
    - The name of the Ollama model to use for generating embeddings.

3. Number of GPU (number, optional)

    - Description: The number of layers to send to the GPU(s). On macOS, it defaults to 1 to enable metal support, 0 to disable.
    - Additional parameter

4. Number of Thread (number, optional)

    - Description: Sets the number of threads to use during computation. By default, Ollama will detect this for optimal performance. It is recommended to set this value to the number of physical CPU cores your system has.
    - Additional parameter

5. Use MMap (boolean, optional)

    - Default: true
    - Determines whether to use memory mapping for loading the model.
    - Additional parameter

## Output

The node initializes and returns an instance of the OllamaEmbeddings class, which can be used to generate embeddings for input text.


## Usage

This node is particularly useful in workflows that require text embeddings, such as:

- Semantic search
- Text clustering
- Document similarity comparisons
- Feature extraction for machine learning models

By leveraging Ollama’s open-source models, users can generate high-quality embeddings locally or on their own infrastructure, providing more control over the embedding process and reducing dependency on external API services.

​
## Notes
- The node uses the @langchain/community/embeddings/ollama package, which should be installed in the project.
- Make sure the Ollama service is running and accessible at the specified Base URL.
- The additional parameters (Number of GPU, Number of Thread, and Use MMap) allow for fine-tuning the embedding generation process based on available hardware and specific requirements.

{% hint style="info" %}

This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
