---
description: Wrapper around Serper.dev - Google Search API.
---

# Serper

<figure><img src="../../../.gitbook/assets/image (11) (1) (1).png" alt="" width="305"><figcaption><p>Serper Node</p></figcaption></figure>

The Serper node is a wrapper around the Serper.dev Google Search API. It provides a tool for performing Google searches within your application.


## Parameters

This node doesn't have any input parameters specific to its functionality. However, it requires a credential to be connected:


## Input/Output

- The node doesn't have any specific inputs defined in the inputs array. 
- The main input it requires is the Serper API key, which is obtained through the connected credential.

- Output is not explicitly defined in this class, but it will return a new instance of the Serper class from the @langchain/community/tools/serper package.


## Functionality

The Serper node initializes a Serper tool that can be used for Google searches. Here’s how it works:

1. When initialized, it retrieves the credential data associated with the node.

2. It extracts the Serper API key from the credential data.

3. It creates and returns a new instance of the Serper class, passing the API key as a parameter.


## Usage

This node is typically used as part of a larger workflow where Google search functionality is needed. It can be combined with other nodes to create more complex search and information retrieval systems.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
