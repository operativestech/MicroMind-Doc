# Running in Production

## Mode

When running in production, we highly recommend using [Queue](running-aimicromind-using-queue.md) mode with the following settings:

* At least 2 main servers with load balancing, each starting from 2 CPU 4GB RAM
* At least 2 workers, each starting from 1 CPU 2GB RAM

You can configure auto scaling depending on the traffic and volume.

## Database

By default, AiMicromind will use SQLite as the database. However when running at scale, its recommended to use PostgresQL.

## Storage

Currently aimicromind only supports [AWS S3](https://aws.amazon.com/s3/) with plan to support more blob storage providers. This will allow files and logs to be stored on S3, instead of local file path. Refer [#for-storage](environment-variables.md#for-storage "mention")

## Encryption

AiMicromind uses an encryption key to encrypt/decrypt credentials you use such as OpenAI API keys. [AWS Secret Manager](https://aws.amazon.com/secrets-manager/) is recommended to be used in production for better security control and key rotation. Refer [#for-credentials](environment-variables.md#for-credentials "mention")

## API Key Storage

Users can create multiple API keys within aimicromind in order to authenticate with the [APIs](../using-aimicromind/api.md). By default, keys get stored as a JSON file to your local file path. However when you have multiple instances, each instance will create a new JSON file, causing confusion. You can change the behaviour to store into database instead. Refer [#for-aimicromind-api-keys](environment-variables.md#for-aimicromind-api-keys "mention")

## Rate Limit

When deployed to cloud/on-prem, most likely the instances are behind a proxy/load balancer. The IP address of the request might be the IP of the load balancer/reverse proxy, making the rate limiter effectively a global one and blocking all requests once the limit is reached or `undefined`. Setting the correct `NUMBER_OF_PROXIES` can resolve the issue. Refer [#rate-limit-setup](rate-limit.md#rate-limit-setup "mention")

## Load Testing

Artillery can be used to load testing your deployed aimicromind application. Example script can be found [here](https://github.com/operativestech/AiMicroMind_Platform_2025/blob/main/artillery-load-test.yml).
