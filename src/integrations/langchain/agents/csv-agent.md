---
description: Agent used to answer queries on CSV data.
---

# CSV Agent

<figure><img src="../../../.gitbook/assets/image (16) (1) (1).png" alt="" width="273"><figcaption><p>CSV Agent Node</p></figcaption></figure>

## CSV Agent Functionality

This agent is designed to answer natural language queries based on CSV data. 
It works by loading the CSV file into a pandas DataFrame and leveraging a language model to analyze and respond to user queries.

For example, the CSV Agent can be used to answer questions like:

* "How many rows are in the CSV?"
* "What is the average value of column ‘age’?"
* "Show me a summary of entries where 'column X' > 100"

## Inputs

The CSV Agent requires the following inputs to function effectively:

### Required Parameters

* **(LLM) Language Model**: The language model to be used for processing queries. This input is required and helps determine the quality and accuracy of responses provided by the agent.

* **CSV File**: Required input. This field is used to upload the CSV file that the agent will analyze. The uploaded file should contain the data you want the agent to process and query using natural language instructions.

### Optional Parameters

* **Input Moderation**: Optional input that enables content moderation. This helps ensure that queries are appropriate and do not contain offensive or harmful content.


## How It Works
1. The agent first loads the CSV file using either the default or custom Pandas read_csv function.
2. It converts the CSV data into a Pandas DataFrame using Pyodide (a Python runtime for the browser).
3. A language model interprets the user’s query and generates Python code to analyze the data.
4. The generated Python code is executed using Pyodide to perform the analysis.
5. The results of the analysis are then passed back to the language model to generate a human-readable response.
6. The final answer is returned to the user.

The CSV Agent node provides a powerful interface for interacting with CSV data using natural language, making it easier for users to gain insights from their CSV files without needing to write complex queries or scripts. It’s particularly useful for data analysts, business users, or anyone who needs to quickly extract information from CSV data without diving into the technicalities of data manipulation.

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
