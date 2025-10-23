---
description: AWSBedrock embedding models to generate embeddings for a given text.
---

# AWS Bedrock Embeddings

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="301"><figcaption><p>AWS Bedrock Embeddings Node</p></figcaption></figure>

The AWS Bedrock Embeddings node is a component that integrates AWS Bedrock’s embedding models into a larger system, allowing for the generation of embeddings for given text inputs. This node is particularly useful for tasks such as semantic search, text classification, and clustering.

## Parameters

### Credential (Optional)
  - Type: AWS API Credential

### Inputs

1. Region

    - Type: Async Options (listRegions)
    - Default: “us-east-1”
    - Description: AWS region for the Bedrock service

2. Model Name

    - Type: Async Options (listModels)
    - Default: “amazon.titan-embed-text-v1”
    - Description: The embedding model to use

3. Custom Model Name

    - Type: String
    - Optional: Yes
    - Description: If provided, overrides the selected Model Name

4. Cohere Input Type

    - Type: Options
    - Optional: Yes
    - Description: Specifies the type of input for Cohere models (v3+)
    - Options:
        - search_document
        - search_query
        - classification
        - clustering
        
5. Batch Size

    - Type: Number
    - Optional: Yes
    - Default: 50
    - Description: Document batch size for Titan model API calls

6. Max AWS API retries

    - Type: Number
      - Optional: Yes
      - Default: 5
      - Description: Maximum number of API call retries for Titan model
​
## Functionality

1. Model Initialization:

    - Sets up the BedrockEmbeddings model with provided parameters
    - Configures AWS credentials if provided

2. Embedding Generation:

    - For single queries: Uses embedQuery method
    - For multiple documents: Uses embedDocuments method
    - Handles different processing for Titan and Cohere models

3. Batch Processing:

    - Implements a batch processing system for Titan models to manage API rate limits
    - Includes retry logic with exponential backoff for handling throttling exceptions

4. Error Handling:

    - Provides specific error messages for invalid responses or exceeded retry limits
​
## Use Cases

1. Semantic search in vector databases
2. Text classification tasks
3. Document clustering
4. Enhancing natural language processing pipelines

## Notes

- The node dynamically loads available models and regions
- It supports both Amazon Titan and Cohere embedding models
- Special handling is implemented for Cohere models, requiring input type specification
- Batch processing and retry logic are implemented to handle API rate limits efficiently

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
