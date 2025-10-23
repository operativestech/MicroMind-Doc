---
description: Check whether content complies with OpenAI usage policies.
---

# OpenAI Moderation

<figure><img src="../../../.gitbook/assets/image (3) (1) (1) (1) (1) (1) (1) (1) (1).png" alt="" width="302"><figcaption><p>OpenAI Moderation Node</p></figcaption></figure>

The OpenAI Moderation node leverages OpenAI’s content moderation API to analyze input text for potentially harmful or inappropriate content, ensuring compliance with OpenAI’s usage policies.

## Parameters

### Credential (Required)

- Type: credential

- Credential Names: openAIApi

- Description: OpenAI API credentials for accessing the moderation service


### Inputs

1. Error Message (optional)

    - Type: string

    - Default: “Cannot Process! Input violates OpenAI’s content moderation policies.”

    - Description: Custom error message to display when content violates moderation policies

​
## Functionality

The OpenAI Moderation node provides real-time content analysis through the following features:

1. Content Analysis

- Analyzes text for harmful or inappropriate content

- Uses OpenAI’s advanced moderation models

- Provides detailed categorization of potential violations

2. Policy Enforcement

- Ensures compliance with OpenAI’s usage policies

- Prevents processing of prohibited content

- Maintains consistent content standards

3. Integration Features

- Seamless integration with OpenAI services

- Real-time moderation checks

- Customizable error handling

​
## Use Cases

1. Content Pre-screening

- Filter user inputs before processing

- Prevent policy violations

- Maintain content quality

2. API Compliance

- Ensure adherence to OpenAI’s policies

- Prevent API usage violations

- Manage content restrictions

3. Safety Monitoring

- Detect harmful content

- Flag inappropriate submissions

- Protect system integrity

​
## Integration Notes

- Place the node before OpenAI API calls in your workflow

- Configure appropriate error handling

- Monitor moderation results for system optimization

- Consider implementing retry logic for temporary failures

​
## Best Practices

1. Configuration

- Use clear, informative error messages

- Set appropriate timeout values

- Implement proper error handling

2. Monitoring

- Track moderation results

- Monitor false positives/negatives

- Adjust settings based on performance

3. Maintenance

- Keep API credentials secure

- Update error messages as needed

- Monitor OpenAI policy changes

{% hint style="info" %}
This section is a work in progress. We appreciate any help you can provide in completing this section. Please check our [Contribution Guide](../../../contributing/) to get started.
{% endhint %}
