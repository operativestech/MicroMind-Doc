---
description: Split your content into documents based on the Markdown headers.
---

# Markdown Text Splitter

<figure><img src="../../../.gitbook/assets/image (153).png" alt="" width="311"><figcaption><p>Markdown Text Splitter Node</p></figcaption></figure>

The Markdown Text Splitter is a specialized text splitting component designed to divide Markdown content into smaller, manageable chunks based on Markdown headers. This node is particularly useful for processing large Markdown documents while maintaining the structural integrity of the content.

## Parameters

The Markdown Text Splitter accepts two optional parameters:

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


## Input/Output

- **Input**: The node takes Markdown text as input (implicitly, through the text splitting process).

- **Output**: The node outputs an instance of the MarkdownTextSplitter class, which can be used to split Markdown text into chunks.


## Usage

The Markdown Text Splitter is initialized with the specified chunk size and overlap. When used, it will:

1. Analyze the structure of the Markdown document.

2. Split the text into chunks, respecting Markdown headers as natural break points.

3. Ensure each chunk is approximately the specified size (chunkSize).

4. Create an overlap between chunks to maintain context (chunkOverlap).

This node is particularly useful in workflows where you need to process large Markdown documents while preserving their structure, such as in document analysis, content summarization, or when preparing text for large language models with input size limitations.


## Implementation Details

- The node uses the ```code MarkdownTextSplitter``` class from the 'langchain/text_splitter' library.

- It extends the ```code INode``` interface, making it compatible with the larger node-based system it's part of.

- The ```code init``` method creates and returns an instance of ```code MarkdownTextSplitter``` with the specified parameters.


## Best Practices

- Adjust the chunk size based on your specific use case and the requirements of downstream processes.

- Use a chunk overlap to ensure context is maintained between chunks, especially for tasks that require understanding across section boundaries.

- Consider the structure of your Markdown documents when setting the chunk size to avoid breaking important sections mid-content.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
