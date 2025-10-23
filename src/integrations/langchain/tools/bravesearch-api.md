---
description: >-
  Wrapper around BraveSearch API - a real-time API to access Brave search
  results.
---

# BraveSearch API

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1).png" alt="" width="299"><figcaption><p>BraveSearch API Node</p></figcaption></figure>

Brave Search is a privacy-focused search engine with its own independent web index, providing high-quality, fresh, and unbiased search results. This node enables AI agents or chatflows built in AIMicromind to access up-to-date information from the web, enhancing their capabilities with real-time data.

## Parameters

- The node doesn’t have any specific input parameters. However, it requires a credential to be connected


## Input/Output

- **Input**: The node doesn’t require any specific inputs at initialization.

- **Output**: An instance of the BraveSearch class from the @langchain/community/tools/brave_search package.


## Initialization

The node’s init method performs the following steps:

1. Retrieves the credential data associated with the node.

2. Extracts the Brave API key from the credential data.

3. Creates and returns a new instance of the BraveSearch class, initialized with the API key.

## Usage

This node is typically used in workflows or applications where search functionality is required. It can be combined with other nodes or tools to create more complex search-based operations or to feed search results into other processes.

## Important Notes
- Requires a valid Brave Search API key for authentication.

- Supports integration with text splitters for better content handling.

- Handles API rate limits and errors internally to ensure smooth operation.

- Preserves the privacy-focused nature of Brave Search.

- Results include snippets and metadata useful for downstream processing or display.

- Can be combined with other nodes in AIMicromind to build powerful agents that utilize live web data.


{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
