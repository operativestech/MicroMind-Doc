---
description: Learn how to deploy aimicromind on Render
---

# Render

***

1. Fork [aimicromind Official Repository](https://github.com/operativestech/AiMicroMind_Platform_2025)
2. Visit your github profile to assure you have successfully made a fork
3. Sign in to [Render](https://dashboard.render.com)
4. Click **New +**

<figure><img src="../../.gitbook/assets/render/1.png" alt="" width="563"><figcaption></figcaption></figure>

5. Select **Web Service**

<figure><img src="../../.gitbook/assets/render/2.png" alt=""><figcaption></figcaption></figure>

6. Connect Your GitHub Account
7. Select your forked aimicromind repo and click **Connect**

<figure><img src="../../.gitbook/assets/render/3.png" alt="" width="563"><figcaption></figcaption></figure>

8. Fill in your preferred **Name** and **Region.**
9. Select `Docker` as your **Runtime**

<figure><img src="../../.gitbook/assets/render/4.png" alt=""><figcaption></figcaption></figure>

9. Select an **Instance**

<figure><img src="../../.gitbook/assets/render/5.png" alt=""><figcaption></figcaption></figure>

10. _(Optional)_ Add app level authorization, click **Advanced** and add `Environment Variable`

* AIMICROMIND\_USERNAME
* AIMICROMIND\_PASSWORD

<figure><img src="../../.gitbook/assets/render/6.png" alt=""><figcaption></figcaption></figure>

Add `NODE_VERSION` with value `18.18.1` as the node version to run the instance.

There are list of env variables you can configure. Refer to [environment-variables.md](../environment-variables.md "mention")

11. Click **Create Web Service**

<figure><img src="../../.gitbook/assets/render/7.png" alt=""><figcaption></figcaption></figure>

12. Navigate to the deployed URL and that's it [🚀](https://emojipedia.org/rocket/)[🚀](https://emojipedia.org/rocket/)

<figure><img src="../../.gitbook/assets/render/8.png" alt=""><figcaption></figcaption></figure>

## Persistent Disk

The default filesystem for services running on Render is ephemeral. aimicromind data isn’t persisted across deploys and restarts. To solve this issue, we can use [Render Disk](https://render.com/docs/disks).

1. On the left hand side bar, click **Disks**
2. Name your disk, and specify the **Mount Path** to `/opt/render/.aimicromind`

<figure><img src="../../.gitbook/assets/render/9.png" alt=""><figcaption></figcaption></figure>

3. Click the **Environment** section, and add these new environment variables:

* DATABASE\_PATH - `/opt/render/.aimicromind`
* APIKEY\_PATH - `/opt/render/.aimicromind`
* LOG\_PATH - `/opt/render/.aimicromind/logs`
* SECRETKEY\_PATH - `/opt/render/.aimicromind`
* BLOB\_STORAGE\_PATH - `/opt/render/.aimicromind/storage`

<figure><img src="../../.gitbook/assets/image (1) (5).png" alt=""><figcaption></figcaption></figure>

4. Click **Manual Deploy** then select **Clear build cache & deploy**

<figure><img src="../../.gitbook/assets/render/11.png" alt=""><figcaption></figcaption></figure>

5. Now try creating a flow and save it in AiMicromind. Then try restarting service or redeploy, you should still be able to see the flow you have saved previously.

Watch how to deploy to Render (coming soon)
