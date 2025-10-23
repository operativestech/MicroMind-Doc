# Cloud Migration

This guide is to help users to migrate from Cloud V1 to V2.

In Cloud V1, the URL of the apps looks like <mark style="color:blue;">**https://\<your-instance-name>.app.aimicromind.com**</mark>

In Cloud V2, the URL of the apps is <mark style="color:blue;">**https://cloud.aimicromind.com**</mark>

Why Cloud V2? We have re-written cloud from scratch, that has 5x speed improvement, ability to have multiple workspaces, organization members, and most importantly it is highly scalable with [production-ready architecture](../configuration/running-in-production.md).

1. Login to Cloud V1 via [https://aimicromind.com/auth/login](https://aimicromind.com/auth/login)
2. In your dashboard, at the top right corner, select Export:

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

3. Select the data you would like to export:

<figure><img src="../.gitbook/assets/image (20).png" alt="" width="563"><figcaption></figcaption></figure>

4. Save the exported JSON file.
5. Navigate to Cloud V2 [https://cloud.aimicromind.com](https://cloud.aimicromind.com/)
6. Cloud V2 account does not sync with your existing account in Cloud V1, you'll have to register again or sign in with Google/Github.

<figure><img src="../.gitbook/assets/image (37).png" alt="" width="563"><figcaption></figcaption></figure>

7. Once logged in, from the dashboard top right corner, click Import and upload the exported JSON file.

<figure><img src="../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

8. New user by default is on the **Free Plan** with a limitation of 2 flows and assistants (for each).  If your exported data has more than that, importing the exported JSON file will throw an error. This is why we are giving <mark style="color:orange;">**FIRST MONTH FREE**</mark> on **Starter Plan** which has unlimited flows & assistants!

<figure><img src="../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>

9. Click the **Get Started** button, and add your preferred payment method:

<figure><img src="../.gitbook/assets/image (67).png" alt="" width="563"><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (80).png" alt=""><figcaption></figcaption></figure>

10. After added payment method, navigate back to AiMicromind, click Get Started on the selected plan and Confirm Change:

<figure><img src="../.gitbook/assets/image (95).png" alt="" width="563"><figcaption></figcaption></figure>

11. If everything goes smoothly, you should be on Starter Plan with unlimited flows & assistants! Hooray :tada: Try importing the JSON file again if it was failing previously due to the free plan limitation.

{% hint style="success" %}
All the IDs from exported data remain the same, so you don't have to worry about updating the ID for the API, you just need to update the URL such as [https://cloud.aimicromind.com/api/v1/prediction/69fb1055-ghj324-ghj-0a4ytrerf](https://cloud.aimicromind.com/api/v1/prediction/69fb1055-ghj324-ghj-0a4ytrerf)
{% endhint %}

{% hint style="warning" %}
Credentials are not exported. You will have to create new credentials and use those in the flows and assistants.
{% endhint %}

11. After you have verified everything is working as expected, you can now cancel the Cloud V1 subscription.
12. From the left side panel, click Account Settings, scroll to the bottom, and you will see **Cancel Previous Subscription**:

<figure><img src="../.gitbook/assets/image (135).png" alt=""><figcaption></figcaption></figure>

13. Enter your previous email that was used to sign up the Cloud V1, and hit **Send Instructions**.
14. You will then receive an email to cancel your previous subscription:

<figure><img src="../.gitbook/assets/image (136).png" alt="" width="563"><figcaption></figcaption></figure>

15. Clicking the **Manage Subscription** button will bring you to a portal where you can cancel the Cloud V1 subscription. Your Cloud V1 app will then get shut down on the next billing cycle.

<figure><img src="../.gitbook/assets/image (137).png" alt=""><figcaption></figcaption></figure>

We sincerely apologize for any inconvenience we have caused during the process of migration. If anything we would love to help, don't hesitate to reach us at support@aimicromind.com.
