---
description: >-
  Parse the output of an LLM call into a given structure by providing a Zod
  schema.
---

# Advanced Structured Output Parser

<figure><img src="../../../.gitbook/assets/image (129).png" alt="" width="299"><figcaption><p>Advanced Structured Output Parser Node</p></figcaption></figure>

The Advanced Structured Output Parser Function is designed to parse the output of a language model (LLM) into a highly controlled, structured format by leveraging advanced schema definitions—commonly using libraries like Zod (for TypeScript) or similar schema validation tools. This parser is particularly useful when you need strong guarantees about the structure, types, and validation of data returned from an LLM, supporting more complex and nested schemas than basic parsers

## Key Features

- **Schema-Driven Parsing**: Accepts a detailed schema (e.g., Zod schema) that defines the exact structure, data types, and validation rules for the expected output.

- **Advanced Validation**: Ensures that the LLM output strictly adheres to the schema, catching errors or inconsistencies early.

- **Complex Structures**: Supports nested objects, arrays, enums, and other advanced data types, making it suitable for sophisticated workflows.

- **Error Handling**: Can provide detailed feedback if the output does not match the schema, allowing for robust error management.


## Parameters
 
### Inputs

1. Autofix (Optional)

    - Type: boolean

    - Description: Enables automatic error correction by making additional model calls when parsing fails

    - Default: false

2. Example JSON (Required)

    - Type: string

    - Description: Zod schema definition for output structure validation

    - Default Example:
    
    ```code 
        z.object({
                title: z.string(),
                yearOfRelease: z.number().int(),
                genres: z.array(z.enum(['Action', 'Comedy', 'Drama', 'Sci-Fi'])).max(2),
                shortDescription: z.string().max(500)
        })
          ```

## Comparison between Structured Output Parser & Advanced Structured Output Parser 

| Feature                   | Structured Output Parser                        | Advanced Structured Output Parser Function                |
|---------------------------|-------------------------------------------------|----------------------------------------------------------|
| Schema Complexity         | Simple (flat JSON/dictionary)               | Complex (nested, enums, advanced validation)          |
| Validation                | Basic type and field checks                | Strong, schema-driven, detailed error reporting       |
| Supported Schema Types    | JSON Schema, Example-based                  | Zod schema, Pydantic, advanced schema libs           |
| Use Case                  | Simple, final output formatting              | Complex, multi-layered, deeply validated output        |
| Error Handling            | Limited                                      | Detailed, with feedback on schema mismatches         |
| Integration               | Quick setup, less flexible                  | Requires schema definition, more flexible              |


{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
