---
description: >-
  Wrapper around Google Custom Search API - a real-time API to access Google
  search results.
---

# Google Custom Search

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="310"><figcaption><p>Google Custom Search Node</p></figcaption></figure>

The Google Custom Search API node is a tool that provides access to Google’s Custom Search Engine (CSE) functionality. It allows users to perform programmatic searches using Google’s search technology, tailored to specific domains or content.

## Parameters

The node doesn’t have any direct input parameters. Instead, it relies on credentials for authentication and configuration.


## Credentials Required

- **Google API Key**: Used for authentication with Google’s API services.

- **Google Custom Search Engine ID**: Identifies the specific Custom Search Engine to be used.

## Initialization

The node initializes by:

1. Retrieving credential data.

2. Extracting the Google API Key and Custom Search Engine ID from the credentials.

3. Creating and returning a new instance of GoogleCustomSearch with these parameters.

## Base Classes

The node inherits from:

- GoogleCustomSearchAPI

- Any base classes of the GoogleCustomSearch class from the @langchain/community/tools/google_custom_search package.


## Usage

This node is typically used in workflows or applications that require:

- Targeted web searches within specific domains

- Integration of Google search capabilities into custom applications

- Automated information retrieval from the web


## Input/Output

- Input: No direct inputs are required for this node.

- Output: Returns an initialized GoogleCustomSearch instance, which can be used to perform custom searches.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
