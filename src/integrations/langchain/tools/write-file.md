---
description: Write file to disk.
---

# Write File

<figure><img src="../../../.gitbook/assets/image (13) (1) (1).png" alt="" width="308"><figcaption><p>Write File Node</p></figcaption></figure>

The WriteFile node is a tool component that allows writing text content to files on the disk. It’s part of a larger system, likely a node-based workflow or automation tool.

## Parameters

The node accepts one optional input parameter:

- Base Path

    - Label: Base Path

    - Name: basePath

    - Type: string

    - Optional: true

    - Placeholder: C:\Users\User\Desktop

    - Description: The base directory path for file operations. If not provided, a default path will be used.

## Functionality

This node creates a ```code WriteFileTool``` instance, which is a structured tool for writing files. It uses a ```code NodeFileStore``` to handle the actual file operations.


## Input/Output

- Input:

    - file_path: A string representing the name or path of the file to be written.

    - text: A string containing the content to be written to the file.

- Output:

    - A success message: "File written to successfully."

## Usage

The WriteFile node is used when you need to save text content to a file as part of a workflow or process. It can be useful for:

- Saving generated content

- Logging information

- Creating or updating configuration files

- Exporting data from other nodes or processes


## Notes

- Ensure that the process has the necessary permissions to write to the specified locations.

- Be cautious when using this tool, as it can overwrite existing files.

- The actual file path used will be a combination of the optional base path and the provided file_path in the tool's input.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
