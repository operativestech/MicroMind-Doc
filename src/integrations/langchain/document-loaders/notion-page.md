---
description: Load data from Notion Page (including child pages all as separate documents).
---

# Notion Page

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="262"><figcaption><p>Notion Page Node</p></figcaption></figure>

Notion is a collaboration platform that combines note-taking, knowledge management, and project management. This module provides three different loaders to process Notion content: Database, Page, and Folder loaders.

## Notion Page Loader

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1) (1) (1) (2).png" alt="" width="262"><figcaption><p>Notion Page Node</p></figcaption></figure>

The Page loader extracts content from Notion pages, including all child pages as separate documents.

### Features

* Load page content as documents
* Process child pages recursively
* Extract page properties
* Handle page hierarchy
* Support text splitting
* Customize metadata extraction

### Required Parameters

* **Connect Credential**: Notion API credentials
* **Page Id**: The 32-character hex identifier from the page URL

## Common Features

All Notion loaders support:

### Optional Parameters

* **Text Splitter**: A text splitter to process the extracted content
* **Additional Metadata**: JSON object with additional metadata
* **Omit Metadata Keys**: Comma-separated list of metadata keys to omit

### Outputs

* **Document**: Array of document objects containing metadata and pageContent
* **Text**: Concatenated string from pageContent of documents

## Authentication

### API Authentication (Database & Page Loaders)

* Requires Notion Integration Token
* API rate limiting handled automatically
* Support for workspace-level access
* Secure credential management

### Local Access (Folder Loader)

* No authentication required
* Direct file system access
* Process offline content
* Handle exported data

## Document Structure

Each document contains:

* **pageContent**: Extracted text content
* **metadata**:
  * source: Original source (URL or file path)
  * title: Page or database title
  * properties: Notion properties
  * Additional custom metadata

## Notes

* API loaders require Notion integration setup
* Folder loader needs exported content
* Rate limiting handled automatically
* Memory-efficient processing
* Error handling for invalid inputs
* Support for large datasets
* Flexible output formats
* Metadata customization

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
