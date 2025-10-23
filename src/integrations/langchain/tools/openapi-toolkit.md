---
description: Load OpenAPI specification.
---

# OpenAPI Toolkit

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1).png" alt="" width="306"><figcaption><p>OpenAPI Toolkit Node</p></figcaption></figure>\

The Open API Toolkit node is a component that loads and initializes an Open API specification, creating a set of tools that can be used to interact with the API described by the specification.

## Parameters

### Inputs

1. Language Model

  - Description: The language model to be used with the OpenAPI toolkit

2. YAML File

File Type: .yaml

  - Description: The OpenAPI specification file in YAML format

### Credential (Optional)

  - Description: Only needed if the YAML OpenAPI Spec requires authentication

## Functionality

1. Loads the provided YAML file containing the OpenAPI specification

2. Supports loading from base64-encoded string or file storage

3. Initializes the OpenApiToolkit with the loaded specification and provided language model

4. Handles authentication if credentials are provided

5. Returns a set of tools based on the OpenAPI specification


## Usage

This node is used to create a toolkit of tools based on an OpenAPI specification. These tools can be used in various AI applications, such as chatbots or agents, to interact with the API described by the specification.


## Output

The node returns an array of tools generated from the OpenAPI specification, which can be used in downstream nodes or processes.

## Notes

- The node supports loading YAML files from both base64-encoded strings and file storage systems

- Authentication is handled through optional credentials, supporting Bearer token authentication

- The node is designed to be flexible and can be integrated into various AI workflows that require API interaction based on OpenAPI specifications

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
