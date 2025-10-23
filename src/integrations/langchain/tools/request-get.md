---
description: Execute HTTP GET requests.
---

# Request Get

<figure><img src="../../../.gitbook/assets/up-009.png" alt="" width="280"><figcaption><p>Request Get Node</p></figcaption></figure>

The Requests Get Tool is a component designed to execute HTTP GET requests within a larger system, 
It provides a way to integrate web-based data retrieval into workflows or agent-based systems.

## Purpose

This tool allows agents or workflows to make HTTP GET requests to specified URLs, enabling the retrieval of data from web services or APIs. It can be used to fetch information dynamically as part of a larger process or decision-making system.

## Input Parameters

1. URL

    - Type: string

    - Optional: Yes

    - Description: The exact URL to which the GET request will be made. If not provided, the agent may attempt to determine it from an AIPlugin (if available).

2. Description

    - Type: string

    - Optional: Yes

    - Default: Provided by desc variable (not shown in the given code)

    - Description: Acts as a prompt to guide the agent on when to use this tool. It helps in decision-making processes for tool selection.

3. Headers

    - Type: JSON

    - Optional: Yes

    - Description: Additional HTTP headers to be included in the request.


## Initialization

The ```text init``` method prepares the tool for use by:

1. Parsing the input parameters (URL, description, and headers).

2. Creating a ```text RequestParameters``` object with the provided inputs.

3. Instantiating and returning a new ```text RequestsGetTool``` with the prepared parameters.


## Usage in AI Systems

This tool is likely part of a larger AI or automation system where:

1. An agent or workflow manager can dynamically decide when to use this tool based on the provided description.

2. The tool can be used to fetch data from web services as part of a larger task or information gathering process.

3. The flexibility in URL and headers allows for interaction with various APIs and web services.



{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
