# Vectara QA Chain

A chain for performing question-answering tasks with Vectara.

<figure><img src="../../../.gitbook/assets/screely-1700662138252.png" alt=""><figcaption></figcaption></figure>

## Definitions

**A retrieval-based question-answering chain**, which integrates with a Vectara retrieval component and allows you to configure input parameters and perform question-answering tasks.

## Inputs

* [Vectara Store](../vector-stores/vectara.md)

## Parameters

| Name                   | Description                                                   |
| ---------------------- | ------------------------------------------------------------- |
| Summarizer Prompt Name | model to be used in generating the summary                    |
| Response Language      | desired language for the response                             |
| Max Summarized Results | number of top results to use in summarization (defaults to 7) |

## Outputs

| Name           | Description                   |
| -------------- | ----------------------------- |
| VectaraQAChain | Final node to return response |


## How It Works
1. The chain receives a user question.
2. If input moderation is enabled, it checks the input for potential harmful content.
3. The Vectara store retrieves relevant documents based on the question.
4. The retrieved documents are processed and ranked.
5. The specified summarizer prompt is used to generate a concise answer from the top-ranked documents.
6. The answer is formatted with reordered citations.
7. The final answer and source documents are returned as output.

The Vectara QA Chain node provides a sophisticated solution for building AI-powered question-answering systems that leverage Vectara’s advanced search and summarization capabilities. It excels in scenarios requiring accurate information retrieval and concise summarization from large document collections. 

This node is particularly valuable for enterprises needing to extract insights from vast knowledge bases, researchers seeking efficient ways to summarize findings, or developers building multilingual information retrieval systems.