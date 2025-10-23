---
description: >-
  Converts Html to Markdown and then split your content into documents based on
  the Markdown headers.
---

# Html-To-Markdown Text Splitter

<figure><img src="../../../.gitbook/assets/image (152).png" alt="" width="301"><figcaption><p>Html-To-Markdown Text Splitter Node</p></figcaption></figure>

The HtmlToMarkdown Text Splitter is a specialized text splitter that converts HTML content to Markdown and then splits the resulting Markdown text into smaller chunks based on headers. This node is particularly useful for processing HTML documents and preparing them for further natural language processing or analysis tasks.

## Parameters

1. Chunk Size

    - Label: Chunk Size

    - Name: chunkSize

    - Type: number

    - Description: Number of characters in each chunk

    - Default: 1000

    - Optional: Yes

2. Chunk Overlap

    - Label: Chunk Overlap

    - Name: chunkOverlap

    - Type: number

    - Description: Number of characters to overlap between chunks

    - Default: 200

    - Optional: Yes


## Input

The node expects HTML text as input.

## Output

The node outputs an array of string chunks, where each chunk is a section of the Markdown-converted HTML, split according to the specified chunk size and overlap.

## How It Works

1. The node receives HTML text as input.

2. It uses the ```code NodeHtmlMarkdown.translate()``` function to convert the HTML to Markdown.

3. The resulting Markdown is then split into chunks using the ```code MarkdownTextSplitter``` class from the ```code langchain/text_splitter``` package.

4. The splitting process respects Markdown headers and the specified chunk size and overlap parameters.


## Use Cases

- Processing HTML content from web scraping for natural language processing tasks

- Preparing HTML documents for text analysis or summarization

- Converting and chunking HTML-based documentation for improved searchability or processing

## Notes

- This node extends the functionality of the MarkdownTextSplitter class to handle HTML input.

- The conversion from HTML to Markdown allows for better preservation of document structure compared to plain text splitting.

- The chunk size and overlap can be adjusted to optimize for specific downstream tasks or models.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
