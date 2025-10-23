---
description: Chain that automatically select and call APIs based only on an OpenAPI spec.
---

# OpenAPI Chain

<figure><img src="../../../.gitbook/assets/image (25) (1).png" alt="" width="335"><figcaption><p>OpenAPI Chain Node</p></figcaption></figure>

The OpenAI Chain node enables seamless integration with OpenAI's language models, allowing you to generate, process, and analyze text using advanced AI within your workflows. This node is designed for flexible, intelligent interactions with OpenAI's API, supporting a wide range of natural language tasks.


## Parameters

1. **Chat Model** (Required)

  - Type: BaseChatModel
  - Description: The chat model used for interpreting queries and generating responses.

2. **YAML Link** (Optional)

  - Type: string
  - Description: URL link to the OpenAPI specification in YAML format.
  - Placeholder: https://api.speak.com/openapi.yaml
  - Note: If YAML link is provided, uploaded YAML File will be ignored.

3. **YAML File** (Optional)

  - Type: file
  - File Type: .yaml
  - Description: Uploaded OpenAPI specification file in YAML format.
  - Note: Ignored if YAML link is provided.

4. **Headers** (Optional)

  - Type: json
  - Description: Additional headers to be included in API requests.
  - Additional Params: true

5. **Input Moderation** (Optional)

  - Type: Moderation[]
  - Description: Moderation tools to detect and prevent harmful input.
  - Additional Params: true

## How It Works

1. The chain loads the OpenAPI specification from either the provided YAML link or uploaded file.
2. It receives a user query or instruction.
3. The chat model interprets the query to determine which API endpoint and method to use.
4. The chain constructs the appropriate API request, including any necessary parameters or headers.
5. It executes the API call and receives the response.
6. The chat model then interprets the API response and generates a human-readable answer to the original query.
7. The final response is returned, potentially including both the raw API data and the interpreted answer.


## Notes

- The effectiveness of the chain depends on the quality and completeness of the OpenAPI specification.
- It’s important to ensure that the provided chat model is capable of understanding and working with API concepts.
- The chain supports both YAML and JSON formats for OpenAPI specifications, but YAML is preferred.
- When using file upload, ensure that the YAML file is properly formatted and complete.
- The chain can handle complex API structures, including nested objects and arrays in requests and responses.
- For optimal performance, it’s recommended to use a chat model that has been fine-tuned or trained on API-related tasks.

The OpenAPI Chain node provides a powerful solution for creating intelligent, natural language interfaces to API systems defined by OpenAPI specifications. By leveraging advanced language models and standardized API descriptions, it enables developers to quickly build sophisticated applications that can interact with complex APIs based on simple user queries. This node is particularly valuable in scenarios where you want to provide easy access to API functionality without requiring users to understand the technical details of API operation.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
