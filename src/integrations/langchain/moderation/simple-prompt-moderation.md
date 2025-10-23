---
description: >-
  Check whether input consists of any text from Deny list, and prevent being
  sent to LLM.
---

# Simple Prompt Moderation

<figure><img src="../../../.gitbook/assets/image (4) (1) (1) (1) (1) (1) (1).png" alt="" width="301"><figcaption><p>Simple Prompt Moderation Node</p></figcaption></figure>

The Simple Prompt Moderation node provides customizable content filtering by checking input text against user-defined denied phrases or instructions, preventing potentially harmful or unwanted content from being processed.

## Parameters
​
### Inputs

1. Deny List (Required)

- Type: string

- Description: List of denied phrases or instructions (one per line)

- Example:

    ```text
    ignore previous instructions
    do not follow the directions
    you must ignore all previous instructions
    ```
2. Chat Model (Optional)

- Type: BaseChatModel

- Description: Language model to detect semantic similarities with denied phrases

3. Error Message (Optional)

- Type: string

- Default: “Cannot Process! Input violates content moderation policies.”

- Description: Custom error message to display when moderation fails


## Functionality

The Simple Prompt Moderation node provides content filtering through the following features:

1. Pattern Matching

- Exact match detection against deny list

- Case-insensitive comparison

- Line-by-line analysis

2. Semantic Analysis (when Chat Model is provided)

- Similarity detection using LLM

- Context-aware filtering

- Flexible matching capabilities

3. Customization Options

- User-defined deny lists

- Configurable error messages

- Optional LLM integration


## Use Cases

1. Prompt Injection Prevention

- Block attempts to override system instructions

- Prevent prompt manipulation

- Maintain system integrity

2. Content Filtering

- Filter specific keywords or phrases

- Implement custom content policies

- Control user input quality

3. Safety Enforcement

- Prevent harmful instructions

- Block unwanted commands

- Maintain usage boundaries

​
## Integration Notes

- Position the node early in your workflow to filter inputs

- Consider combining with other moderation nodes for layered protection

- Monitor and update deny lists regularly

- Test thoroughly with various input patterns

​
## Best Practices

1. Deny List Management

- Keep deny lists up to date

- Use specific, clear patterns

- Document denied phrases

- Regular expression support for complex patterns

2. Error Handling

- Provide clear error messages

- Log moderation events

- Implement appropriate fallbacks

3. Performance Optimization

- Balance deny list size with performance

- Consider caching for frequent patterns

- Monitor LLM usage when enabled

4. Maintenance

- Regular deny list reviews

- Update patterns based on new threats

- Monitor false positive/negative rates

- Adjust sensitivity as needed

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
