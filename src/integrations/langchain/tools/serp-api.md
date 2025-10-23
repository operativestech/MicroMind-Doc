---
description: Wrapper around SerpAPI - a real-time API to access Google search results.
---

# Serp API

<figure><img src="../../../.gitbook/assets/image (10) (1) (1).png" alt="" width="301"><figcaption>Serp API Node</figcaption></figure>

The SerpAPI Tool Node is a wrapper around the SerpAPI service, which provides real-time access to Google search results. This node is part of a larger system for building AI-powered applications, likely within a visual programming or node-based environment.

## Parameters

This node doesn't have any additional input parameters beyond the required credential.

## Initialization

The ```text init``` method is responsible for setting up the SerpAPI tool:

1. It retrieves the credential data associated with the node.

2. Extracts the SerpAPI key from the credential data.

3. Creates and returns a new instance of the SerpAPI class using the extracted API key.


## Usage

The SerpAPI Tool Node is used to integrate Google search capabilities into AI workflows. It allows the AI to perform web searches and retrieve up-to-date information from the internet. This can be particularly useful for:

  - Answering questions that require current information

  - Fact-checking or verification tasks

  - Gathering data for research or analysis

  - Enhancing the knowledge base of language models with real-time web data


## Note

To use this node, you must have a valid SerpAPI key stored in the system's credential manager under the name 'serpApi'. Ensure that you have an active subscription to SerpAPI and that your usage complies with their terms of service.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
