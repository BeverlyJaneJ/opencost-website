---
sidebar_position: 8
---

# GCP integration

OpenCost automatically reads node information from `node.spec.providerID` to understand which cloud service provider (CSP) is in use. If it detects the provider is GCP, it attempts to pull data for node pricing. To do this, OpenCost uses the [GCP Cloud Billing API](https://cloud.google.com/billing/), which requires an API key.

## GCP pricing configuraiton

To enable OpenCost to get pricing information from your GCP project, you must:

1. Enable the Cloud Billing API.

2. Generate an API key that has permissions to access it.

### Enabling Cloud Billing API

To enable the Cloud Billing API:

1. Click the "Enable the API" button.

2. Follow the prompts on [Get Google Cloud pricing information](https://cloud.google.com/billing/v1/how-tos/catalog-api).

### Generating the API key

You need to generate an API that will be used in place of the default key in the `CLOUD_PROVIDER_API_KEY` environment variable. To generate an API key:

1. Follow the steps on [Authenticate using API keys](https://cloud.google.com/docs/authentication/api-keys).

2. Optionally edit the key and restrict the key to only the Cloud Billing API.
