---
description: Split documents based on language-specific syntax.
---

# Code Text Splitter

<figure><img src="../../../.gitbook/assets/image (151).png" alt="" width="296"><figcaption><p>Code Text Splitter Node</p></figcaption></figure>

The Code Text Splitter is a specialized text splitter designed to split documents based on language-specific syntax. It utilizes the ```code RecursiveCharacterTextSplitter``` from the LangChain library to perform intelligent splitting of code documents.

## Parameters

1. Language

    - Type: Options

    - Description: The programming language of the code to be split.

2. Chunk Size

    - Type: Number

    - Default: 1000

    - Optional: Yes

    - Description: The number of characters in each chunk. This determines the size of the text segments after splitting.


3. Chunk Overlap

    - Type: Number

    - Default: 200

    - Optional: Yes

    - Description: The number of characters to overlap between chunks. This helps maintain context between split segments.


## Input/Output

### Input

The node expects code or text input in the specified language.

### Output

The node outputs split text chunks based on the specified parameters and language-specific syntax.

### Usage

This node is particularly useful in workflows that involve processing or analyzing code, such as:

- Code summarization

- Code analysis tasks

- Preparing code for language models

- Splitting large codebases for easier processing

By respecting the syntax of the chosen programming language, it ensures that the splitting process maintains the logical structure of the code as much as possible, which can lead to better results in downstream tasks.

## Implementation Details

The node uses the RecursiveCharacterTextSplitter.fromLanguage() method from LangChain, which applies language-specific splitting rules. This method is more intelligent than a simple character-based split, as it attempts to split at appropriate syntactic boundaries for the given language.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
