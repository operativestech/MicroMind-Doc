---
description: Chain to run queries against LLMs.
---

# LLM Chain

<figure><img src="../../../.gitbook/assets/image (31).png" alt="" width="341"><figcaption><p>LLM Chain Node</p></figcaption></figure>

The LLM Chain is a versatile component designed to run queries against Large Language Models (LLMs). It provides a flexible interface for prompt engineering, allowing users to construct complex prompts and process LLM responses efficiently.

## Parameters

- Language Model (Required)
  -  Type: BaseLanguageModel
  -  Description: The language model to be used for generating responses.

- Prompt (Required)
  -  Type: BasePromptTemplate
  -  Description: The prompt template to be used for constructing queries to the LLM.

- Output Parser (Optional)
  -  Type: BaseLLMOutputParser
  -  Description: Parser to process and structure the output from the LLM.

- Input Moderation (Optional)
  -  Type: Moderation[]
  -  Description: Moderation tools to detect and prevent harmful input.
  -  List: true

- Chain Name (Optional)

  -  Type: string
  -  Description: A name for the chain, useful for identification in complex workflows.
  -  Placeholder: “Name Your Chain”


## How It Works

1. The chain receives input, which is used to populate the prompt template.
2. If input moderation is enabled, it checks the input for potential harmful content.
3. The populated prompt is sent to the language model for processing.
4. The LLM generates a response based on the prompt.
5. If an output parser is specified, it processes the LLM’s response.
6. The final output (either the processed response or the chain object) is returned.


## Use Cases

- Generating creative content based on specific prompts
- Answering questions or providing explanations on various topics
- Translating or paraphrasing text
- Analyzing and summarizing documents
- Generating code or technical documentation
- Creating conversational AI components

## Notes

- The effectiveness of the chain heavily depends on the quality of the prompt template and the capabilities of the chosen language model.
- Custom prompt templates can significantly influence the behavior and output of the chain.
- When using the chain in production, implement proper error handling, especially for potential API failures or moderation issues.
- Consider the token limits of the chosen LLM when designing prompts and processing outputs.
- The chain supports both text-only and multi-modal (text + image) inputs, depending on the language model’s capabilities.
- Output parsing can be crucial for integrating LLM responses into structured workflows or databases.

The LLM Chain node serves as a fundamental building block for creating AI-powered applications leveraging large language models. Its flexibility in prompt engineering and output processing makes it suitable for a wide range of natural language processing tasks. This node is particularly valuable in scenarios requiring complex language understanding, generation, or transformation, such as in content creation tools, advanced chatbots, or data analysis systems that need to interpret and generate human-like text.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
