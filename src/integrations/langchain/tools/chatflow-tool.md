---
description: Execute another chatflow and get the response.
---

# Chatflow Tool

<figure><img src="../../../.gitbook/assets/image (26).png" alt="" width="248"> <figcaption><p>Chatflow Tool</p></figcaption></figure>

The Chatflow Tool node is a specialized tool that allows the execution of another chat flow within a project. It’s particularly useful for creating modular and reusable components in complex conversational AI systems.


## Parameters

### Main Parameters

1. Select Chatflow

    - Type: asyncOptions

    - Description: Allows selection of an existing chatflow to be used as a tool.

2. Tool Name

    - Type: string

    - Description: Name of the tool, used for identification.

3. Tool Description

    - Type: string

    - Description: Detailed description of the tool’s functionality, used by the LLM to determine when to use this tool.

4. Return Direct

    - Type: boolean

    - Optional: Yes

    - Description: Determines if the tool’s output should be returned directly.

### Additional Parameters

1. Override Config

    - Type: json

    - Optional: Yes

    - Description: Allows overriding the configuration passed to the Chatflow.

2. Base URL

    - Type: string

    - Optional: Yes

    - Default: URL of the incoming request

    - Description: Base URL useful for executing the Chatflow through an alternative route.

3. Start new session per message

    - Type: boolean

    - Optional: Yes

    - Default: false

    - Description: Determines whether to continue the session with the Chatflow tool or start a new one with each interaction.

4. Use Question from Chat

    - Type: boolean

    - Optional: Yes

    - Description: If enabled, uses the question from the chat as input to the chatflow, overriding custom input.

5. Custom Input

    - Type: string

    - Optional: Yes

    - Description: Custom input to be passed to the chatflow. If empty, the LLM decides the input.

## Functionality

1. Initializes with selected parameters and credentials.

2. Creates a ChatflowTool instance with the specified configuration.

3. When called, it executes the selected chatflow using the provided input.

4. The tool makes an HTTP POST request to the specified API endpoint.

5. The response from the executed chatflow is returned as a string.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
