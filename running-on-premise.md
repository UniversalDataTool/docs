---
description: Run the Universal Data Tool on your infrastructure.
---

# Running On-Premise

> For small companies or projects, you might want to consider just using the [Desktop Application](installation.md#using-on-desktop-windows-mac-linux) or [udt.dev](https://udt.dev), which requires less setup!

The Universal Data Tool can be run and customized on your own infrastructure easily. This is best for users who want to keep their version of Universal Data Tool stable, and don't need new features from weekly releases. You may also want to keep your data within your network.

## Run via Docker

The Universal Data Tool builds docker containers on every new release. You can run the Universal Data Tool using...

```bash
# Starts the Universal Data Tool on port 3000 and a collaborative server on 3001
docker run -d -p 3000:3000 -p 3001:3001 \
             -e UDT_collaborationServer_url=http://localhost:3001 \
             universaldatatool/universaldatatool
```

You can provide different options to the docker container to control various aspects of Universal Data Tool. Below is a table of a few of the configuration parameters can customize. You'll know if a configuration value is used because it will appear in the starting logs like the following image...

![Configuration values are shown in a table on start](.gitbook/assets/image%20%2872%29.png)

| Environment Var | Description |
| :--- | :--- |
| `UDT_collaborationServer_url` | Collaboration server URL  |
| `UDT_pluginUrls` | Comma-delimited URLs to plugins that should be loaded by default |
| `UDT_auth_proxy_corsproxy` | Proxy to use for CORS requests, e.g. to make api requests that are disallowed by CORs |
| `UDT_auth_s3iam_accessKeyId` | Access Key for uploading/importing from AWS S3 buckets |
| `UDT_auth_s3iam_secretAccessKey` | Secret Access Key for uploading/importing from AWS S3 buckets |
| `UDT_s3iam_region` | Region of S3 Bucket |
| `UDT_auth_cognito_identityPoolId` | Cognito Identity Pool Id |
| `UDT_auth_cognito_region` | Cognito Region |
| `UDT_auth_cognito_userPoolId` | Cognito user pool id |
| `UDT_auth_cognito_userPoolWebClientId` | Cognito user pool web client id |
| `UDT_auth_cognito_storage_awsS3_bucket` | Bucket to use for Cognito object storage |
| `UDT_auth_cognito_storage_awsS3_region` | Region of bucket to use for Cognito |
| `UDT_labelhelp_disabled` | Disable remote paid collaboration requests |
| `UDT_labelhelp_apikey` | API Key for requesting work from Label Help |

These are the most common configuration values, but you can also customize hotkeys or any other attribute the appears in the [AppConfig](https://github.com/UniversalDataTool/universal-data-tool/blob/master/src/components/AppConfig/index.js).

## Independent Collaboration Server

Sometimes, you may want to run the Collaboration Server on a different machine than the Client Application, you can do this by using the npm module.

```text
# via npm
npm install -g udt-collaboration-server

udt-collaboration-server --port 3001
```

