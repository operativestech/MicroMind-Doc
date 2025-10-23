---
description: Gives agent the ability to visit a website and extract information.
---

# Web Browser

<figure><img src="../../../.gitbook/assets/image (12) (1) (1).png" alt="" width="309"><figcaption><p>Web Browser Node</p></figcaption></figure>

The Web Browser tool is a component that gives an AI agent the ability to visit a website and extract information. It is implemented as a node in a larger system, likely for AI-powered web browsing and information retrieval.

## Parameters

The Web Browser tool requires two input parameters:

1. Language Model

    - Label: Language Model

    - Name: model

    - Type: BaseLanguageModel

2. Embeddings

    - Label: Embeddings

    - Name: embeddings

    - Type: Embeddings


## Functionality

The tool initializes a WebBrowser instance from the langchain library, which combines a language model and embeddings to process and understand web content.


## Usage

This tool is typically used as part of a larger AI system or agent. It allows the agent to:

1. Visit specified web pages

2. Extract text and other information from those pages

3. Process and understand the content using the provided language model and embeddings

## Integration

This tool can be integrated into AI workflows that require web browsing capabilities. It’s particularly useful for:

- Information gathering tasks

- Web scraping

- Real-time data analysis from web sources

## Notes

- The effectiveness of this tool depends on the quality of the provided language model and embeddings.

- Proper error handling and rate limiting should be implemented when using this tool to respect website policies and prevent overloading servers.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
