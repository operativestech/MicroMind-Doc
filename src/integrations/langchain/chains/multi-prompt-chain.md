---
description: >-
  Chain automatically picks an appropriate prompt from multiple prompt
  templates.
---

# Multi Prompt Chain

<figure><img src="../../../.gitbook/assets/image (32).png" alt="" width="334"><figcaption><p>Multi Prompt Chain Node</p></figcaption></figure>

The Multi Prompt Chain is an advanced chain that automatically selects and uses the most appropriate prompt from multiple predefined prompts based on the input query. It’s designed to handle a wide range of queries by dynamically choosing the best-suited prompt for each specific input.

## Parameters

- Language Model (Required)

  -  Type: BaseLanguageModel
  -  Description: The language model to be used for generating responses and selecting prompts.

- Prompt Retriever (Required)

  -  Type: PromptRetriever[]
  -  Description: An array of prompt retrievers, each containing a prompt template, name, and description.
  -  List: true

- Input Moderation (Optional)

  -  Type: Moderation[]
  -  Description: Moderation tools to detect and prevent harmful input.
  -  List: true

## How It Works

1. The chain receives a user input.
2. If input moderation is enabled, it checks the input for potential harmful content.
3. The language model analyzes the input to determine which prompt from the provided set is most appropriate.
4. The selected prompt is then used to format the input for the language model.
5. The language model generates a response based on the formatted prompt and input.
6. The final response is returned as output.

## Use Cases

- Creating versatile chatbots that can handle a wide range of topics
- Building AI assistants capable of adapting to different types of user queries
- Implementing dynamic Q&A systems that can switch between different knowledge domains
- Developing content generation tools that can adapt to various writing styles or formats
- Creating flexible customer support systems that can handle diverse inquiries

## Special Features

- Dynamic Prompt Selection: Automatically chooses the most appropriate prompt for each input.
- Multiple Domain Support: Can handle queries across various topics or domains using specialized prompts.
- Flexible Configuration: Allows for easy addition or modification of prompt templates.
- Input Moderation: Optional safeguards against inappropriate or harmful inputs.
- Scalability: Can be expanded to cover new topics or query types by adding new prompt templates.
- Improved Accuracy: By using specialized prompts, it can provide more accurate and relevant responses.

## Notes

- The effectiveness of the chain depends on the quality and diversity of the provided prompt templates.
- Careful design of prompt descriptions is crucial for accurate prompt selection.
- The chain may require more computation time compared to single-prompt chains due to the selection process.
- It’s important to ensure that the language model is capable of accurately selecting between prompts.
- For best results, prompt templates should be distinct and cover a wide range of potential query types.
- Regular analysis of chain performance can help identify areas where new prompts might be needed.
- The chain supports streaming responses for real-time interaction in compatible environments.

The Multi Prompt Chain node provides a sophisticated solution for creating highly adaptable AI systems that can handle a diverse range of inputs. By dynamically selecting the most appropriate prompt for each query, it combines the specificity of specialized prompts with the flexibility of a general-purpose system. This node is particularly valuable in scenarios where the input queries can vary widely in topic, style, or intent, such as in multi-purpose virtual assistants, comprehensive customer support systems, or versatile content generation tools. Its ability to adapt to different types of inputs makes it a powerful component for building more intelligent and responsive AI applications.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
