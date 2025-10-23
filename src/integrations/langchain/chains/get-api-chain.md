---
description: Chain to run queries against GET API.
---

# GET API Chain

<figure><img src="../../../.gitbook/assets/image (24) (1).png" alt="" width="337"><figcaption><p>GET API Chain Node</p></figcaption></figure>

The GET API Chain node is designed to run queries against GET APIs. It constructs API URLs based on given documentation and user questions, then processes the API responses to answer queries.

## Parameters

  - Language Model (Required)
    - Type: BaseLanguageModel
    - Description: The language model used to generate API URLs and process responses.

  - API Documentation (Required)
    - Type: string
    - Description: Description of how the API works. Should include details about endpoints, parameters, and response formats.
    - Rows: 4

  - Headers (Optional)
    - Type: json
    - Description: Headers to be included in the API request.
    - Additional Params: true

  - URL Prompt (Optional)
    - Type: string
    - Description: Prompt used to tell LLMs how to construct the URL.
    - Default: A predefined prompt template for URL construction.
    - Rows: 4
    - Additional Params: true
      
  - Answer Prompt (Optional)
    - Type: string
    - Description: Prompt used to tell LLMs how to process the API response.
    - Default: A predefined prompt template for answer generation.
    - Rows: 4
    - Additional Params: true

## Input

A string containing the user’s question or query about the API.

## Output

A string containing the answer to the user’s question, based on the API response.

## How It Works

1. The chain receives a user question about the API.
2. It uses the language model and the URL prompt to generate an appropriate API URL based on the API documentation and the question.
3. The chain makes a GET request to the constructed URL, including any specified headers.
4. Upon receiving the API response, it uses the language model and the answer prompt to generate a human-readable answer to the original question.
5. The final answer is returned as output.

## Use Cases

- Querying external APIs to answer user questions
- Automating API interactions in chatbots or virtual assistants
- Simplifying complex API documentation for end-users
- Creating natural language interfaces for data retrieval from APIs
- Integrating multiple API sources to answer complex queries

## Special Features

- Dynamic URL Generation: Constructs API URLs based on natural language questions.
- Flexible API Documentation: Can work with various APIs by providing appropriate documentation.
- Customizable Prompts: Allows fine-tuning of URL construction and answer generation processes.
- Header Support: Enables authentication and other custom headers for API requests.
- Language Model Integration: Leverages advanced language models for intelligent API interaction.
​
## Notes

- The quality of results depends significantly on the completeness and accuracy of the provided API documentation.
- Custom URL and answer prompts can be used to optimize the chain for specific APIs or use cases.
- The chain is designed for GET requests only and may not be suitable for APIs requiring other HTTP methods.
- Proper error handling should be implemented when using this chain in production environments.
- The effectiveness of the chain can vary depending on the complexity of the API and the nature of the user queries.

The GET API Chain node provides a powerful tool for creating natural language interfaces to GET APIs. By combining API documentation, language models, and customizable prompts, it enables developers to build sophisticated systems that can interact with external APIs based on user queries. This node is particularly valuable in scenarios where you want to provide a user-friendly interface to complex API systems or integrate API-based data retrieval into conversational AI applications.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
