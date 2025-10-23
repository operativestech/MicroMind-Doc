---
description: Read file from disk.
---

# Read File

<figure><img src="../../../.gitbook/assets/image (5) (1) (1) (1) (1) (1).png" alt="" width="303"><figcaption><p>Read File Node</p></figcaption></figure>

The Read File node is a tool component designed to read files from the disk. It’s part of a larger system, likely a workflow or automation platform that deals with file operations.

## Parameters

The node accepts one optional input parameter:

  - Base Path

    - Label: Base Path

    - Name: basePath

    - Type: string

    - Optional: true

    - Placeholder: C:\Users\User\Desktop

    - Description: The base directory path from which files will be read. If not provided, the default system path will be used.

## Functionality

1. The node initializes a ```code NodeFileStore``` instance, either with the provided base path or using the default path.

2. It creates a ```code ReadFileTool``` instance, which is the core component for reading files.

3. The ```code ReadFileTool``` uses a schema to validate input, expecting a ```code file_path``` string.

4. When called, the tool reads the contents of the specified file using the ```code store.readFile()``` method.

## Input/Output

- Input: A file path (string) representing the file to be read.

- Output: The contents of the file as a string.

## Usage

This node is typically used in scenarios where file contents need to be accessed or processed within a workflow. For example:

- Reading configuration files

- Processing text files

- Accessing data stored in files for further analysis or manipulation

## Error Handling

While not explicitly shown in the code, users should be aware that file operations can throw errors (e.g., file not found, permission issues). Proper error handling should be implemented when using this node in a workflow.


## Notes

- The actual file reading operation is performed by the ```code NodeFileStore``` class, which is not fully visible in the provided code snippet.

- This tool is designed to work within a larger system, likely integrating with other nodes or tools for complex workflows.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
