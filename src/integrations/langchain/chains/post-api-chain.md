---
description: Chain to run queries against POST API.
---

# POST API Chain

<figure><img src="../../../.gitbook/assets/image (28).png" alt="" width="337"><figcaption><p>POST API Chain Node</p></figcaption></figure>

The POST API Chain node is designed to interact with APIs that require POST requests. It enables users to send data to external APIs by constructing request bodies and URLs based on provided documentation and user input, then processes the API responses to generate answers.

## Parameters

  - Language Model (Required)
    - Type: BaseLanguageModel
    - Description: The language model used to generate API URLs, request bodies, and process responses.

  - API Documentation (Required)
    - Type: string
    - Description: Description of how the API works. Should include details about endpoints, parameters, request/response formats, and body schema.
    - Rows: 4

  - Headers (Optional)
    - Type: json
    - Description: Headers to be included in the API request (e.g., authentication, content-type).
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

## How It Works

1. The chain receives a user question about the API.
2. It uses the language model and the URL prompt to generate an appropriate API URL based on the API documentation and the question.
3. The chain uses the body prompt to generate the required request body (payload) for the POST request.
4. It makes a POST request to the constructed URL, including any specified headers and the generated request body.
5. Upon receiving the API response, it uses the language model and the answer prompt to generate a human-readable answer to the original question.
6. The final answer is returned as output.

## Use Cases

- Creating or updating resources via external APIs
- Automating data submission tasks in chatbots or virtual assistants
- Simplifying complex API documentation for end-users
- Enabling natural language interfaces for data creation or modification
- Integrating multiple API sources to automate workflows requiring POST requests

it empowers developers to build systems that can interact with external APIs for data creation, updates, or other POST operations based on user instructions. 

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
