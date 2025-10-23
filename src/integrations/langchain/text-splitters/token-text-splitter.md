---
description: >-
  Splits a raw text string by first converting the text into BPE tokens, then
  split these tokens into chunks and convert the tokens within a single chunk
  back into text.
---

# Token Text Splitter

<figure><img src="../../../.gitbook/assets/image (156).png" alt="" width="305"><figcaption><p>Token Text Splitter Node</p></figcaption></figure>

The Token Text Splitter is a component used for splitting text into smaller chunks based on token count. It utilizes the TikToken library for tokenization, which is commonly used in language models like GPT.

## Parameters

### Encoding Name

- Type: Options

- Default: gpt2

- Available Options:

    - gpt2

    - r50k_base

    - p50k_base

    - p50k_edit

    - cl100k_base

- Description: Specifies the encoding scheme to use for tokenization. Different models may use different encodings.


## Chunk Size

- Type: Number

- Default: 1000

- Optional: Yes

- Description: The number of characters in each chunk. This determines the maximum size of each text segment after splitting.


## Chunk Overlap

- Type: Number

- Default: 200

- Optional: Yes

- Description: The number of characters to overlap between chunks. This helps maintain context between chunks.


## Input/Output

- Input: Raw text string

- Output: An array of text chunks


## Usage

This node is particularly useful in scenarios where you need to process large amounts of text with language models that have a maximum token limit. By splitting the text into smaller chunks, you can process each chunk separately and then combine the results.

Common use cases include:

1. Preparing text for summarization

2. Breaking down large documents for question-answering systems

3. Preprocessing text for semantic search or embeddings


## Implementation Details

The node uses the ```code TokenTextSplitter``` class from the LangChain library, which in turn uses the TikToken library for tokenization. The splitting process ensures that the text is split at token boundaries rather than arbitrary character positions, which can be more semantically meaningful for many NLP tasks.


## Note

When using this splitter, be aware that the actual number of tokens in each chunk may vary slightly from the specified chunk size, as the splitter converts tokens back to text for the final output. The chunk size parameter is used as a target, but the exact size may differ to maintain token integrity.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
