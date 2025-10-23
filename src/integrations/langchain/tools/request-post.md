---
description: Execute HTTP POST requests.
---

# Request Post

<figure><img src="../../../.gitbook/assets/up-010.png" alt="" width="280"><figcaption><p>Request Post Node</p></figcaption></figure>

The Requests Post node is a tool for executing HTTP POST requests within a larger system, likely an AI-powered application or workflow.

## Input Parameters

1. URL

  - Type: string

  - Optional: Yes

  - Description: The exact URL to which the POST request will be made. If not specified, the agent will attempt to determine it from an AIPlugin if provided.

2. Body

  - Type: JSON

  - Optional: Yes

  - Description: The JSON body for the POST request. If not specified, the agent will attempt to determine it from an AIPlugin if provided.

3. Description

  - Type: string

  - Optional: Yes

  - Default: A predefined description (stored in the desc variable)

  - Description: Acts as a prompt to inform the agent when it should use this tool.

4. Headers

  - Type: JSON

  - Optional: Yes

  - Description: HTTP headers to be included with the request.


## Initialization

The node’s ```code init``` method processes the input data and creates a new RequestsPostTool instance with the following steps:

1. Extracts input parameters (headers, URL, description, and body)

2. Parses JSON inputs for headers and body if they are provided as strings

3. Constructs a RequestParameters object with the processed inputs

4. Returns a new RequestsPostTool instance initialized with the RequestParameters


## Usage

This node is designed to be used within a larger system, likely as part of an AI-powered workflow. It provides a flexible way to make HTTP POST requests, either with explicitly provided parameters or by allowing an AI agent to determine the necessary details.

The node can be particularly useful in scenarios such as:

- Sending data to external APIs

- Updating remote resources

- Triggering actions in other systems

- Integrating with web services that require POST requests

By providing a description, the node can guide an AI agent on when and how to use this tool, making it a versatile component in automated workflows or AI-driven applications.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
