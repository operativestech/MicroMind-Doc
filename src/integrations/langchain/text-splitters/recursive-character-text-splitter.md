---
description: >-
  Split documents recursively by different characters - starting with "\n\n",
  then "\n", then " ".
---

# Recursive Character Text Splitter

<figure><img src="../../../.gitbook/assets/image (155).png" alt="" width="305"><figcaption><p>Recursive Character Text Splitter Node</p></figcaption></figure>

The RecursiveCharacterTextSplitter node is a text splitting component used for dividing large text documents into smaller chunks. It’s particularly useful for processing long documents that need to be broken down into more manageable pieces for analysis, summarization, or other natural language processing tasks.

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

3. Custom Separators

    - Label: Custom Separators

    - Name: separators

    - Type: string

    - Description: Array of custom separators to determine when to split the text, will override the default separators

    - Placeholder: ["|", "##", ">", "-"]

    - Optional: Yes

    - Additional: This is an advanced parameter


## Input

The node takes the following inputs:

- Text document(s) to be split (handled internally by the system)

- Configuration parameters as described above


## Output

The node outputs a RecursiveCharacterTextSplitter object, which can be used to split text documents into chunks based on the specified parameters.


## Usage

This node is typically used in document processing pipelines where large texts need to be broken down into smaller, more manageable pieces. It's particularly useful for:

1. Preparing text for large language models with context limitations

2. Breaking down documents for summarization tasks

3. Splitting text for parallel processing

4. Creating more granular sections for information retrieval or question-answering systems


## Implementation Details

- The node uses the ```code RecursiveCharacterTextSplitter``` class from the 'langchain/text_splitter' library.

- It supports dynamic configuration of chunk size, overlap, and custom separators.

- The ```code init``` method creates and returns a configured ```code RecursiveCharacterTextSplitter``` object based on the input parameters.

- Custom separators, if provided, are parsed from a JSON string to an array.


## Error Handling

The node includes error handling for parsing custom separators. If the separators string cannot be parsed as valid JSON, it will throw an error.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
