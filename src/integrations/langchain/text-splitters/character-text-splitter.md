---
description: Splits only on one type of character (defaults to "\n\n").
---

# Character Text Splitter

<figure><img src="../../../.gitbook/assets/image (150).png" alt="" width="305"><figcaption><p>Character Text Splitter</p></figcaption></figure>

The Character Text Splitter is a node used for splitting text into smaller chunks based on a specified character separator. It's particularly useful for processing large text documents into manageable pieces for further analysis or processing.


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

3. Custom Separator

    - Label: Custom Separator

    - Name: separator

    - Type: string

    - Description: Custom separator to determine when to split the text (overrides the default separator)

    - Placeholder: ” ” (space)

    - Optional: Yes

## Input

The node expects text input that needs to be split into smaller chunks.


## Output

The node outputs an instance of CharacterTextSplitter configured with the specified parameters, which can be used to split input text into chunks.


## Usage

This node is typically used in text processing pipelines where large documents need to be broken down into smaller pieces. It's particularly useful in scenarios such as:

1. Preparing text for embedding or semantic analysis

2. Breaking down large documents for summarization

3. Splitting text for parallel processing

4. Preparing input for language models with token limits

The ability to customize chunk size, overlap, and separator makes this node versatile for various text processing needs.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
