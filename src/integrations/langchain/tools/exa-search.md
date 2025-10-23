---
description: Wrapper around Exa Search API - search engine fully designed for use by LLMs.
---

# Exa Search

<figure><img src="../../../.gitbook/assets/up-007.png" alt="" width="285"><figcaption><p>Exa Search Node</p></figcaption></figure>

The ExaSearch node is a wrapper around the Exa Search API, designed to be used as a tool within a larger system, likely for AI-powered applications. Exa is a search engine specifically optimized for use by Language Models (LLMs).

## Parameters

### Required

- Credential: An API key for Exa Search (credential type: exaSearchApi)

### Optional

- **Tool Description**: A custom description of the tool’s functionality (default provided)

- **Num of Results**: Number of search results to return (default: 10, max varies by plan)

- **Search Type**: Options include ‘keyword’, ‘neural’, or ‘magic’ (auto-decides between keyword and neural)

- **Use Auto Prompt**: Boolean to enable query conversion to Exa format

- **Category**: Specifies a data category to focus the search (e.g., company, research paper, news)

- **Include Domains**: List of domains to include in the search

- **Exclude Domains**: List of domains to exclude from the search

- **Start Crawl Date**: ISO 8601 date to set the earliest crawl date for results

- **End Crawl Date**: ISO 8601 date to set the latest crawl date for results

- **Start Published Date**: ISO 8601 date to set the earliest publication date for results

- **End Published Date**: ISO 8601 date to set the latest publication date for results

## Input

The input to this node should be an Exa-optimized query string. If ‘Use Auto Prompt’ is enabled, the input can be a natural language query that will be converted to Exa format.


## Output

The output is a JSON array containing the search results. Each result typically includes details such as the URL, title, snippet, and other metadata related to the search hit.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
