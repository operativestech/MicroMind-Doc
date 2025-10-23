---
description: Load data from the exported and unzipped Notion folder.
---

# Notion Folder

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="259"><figcaption><p>Notion Folder Node</p></figcaption></figure>

Notion is a collaboration platform that combines note-taking, knowledge management, and project management. This module provides three different loaders to process Notion content: Database, Page, and Folder loaders.

The Folder loader processes exported and unzipped Notion content from a local folder.

### Features

* Process exported Notion content
* Handle multiple pages
* Support local file system
* Extract page content
* Maintain document structure
* Support text splitting
* Customize metadata extraction

### Required Parameters

* **Notion Folder**: Path to the exported and unzipped Notion folder

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
