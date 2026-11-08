# Airwallex MCP setup and connection checker

Generate Airwallex MCP client configuration, inspect available tools and validate hosted endpoint access through PipMCP.

Maintainer: jannikco · License: MIT · Verification: **mock-only**

## Quick start

Requires Node.js 22 or later.

```sh
npm ci
npm test
npm start
```

The default example runs locally without credentials and makes no external changes. Verification status describes recorded evidence; local configuration tests do not establish that provider authentication or execution works.

## Connect airwallex

[Create or sign in to PipMCP](https://pipmcp.com/register?app=airwallex&utm_source=github&utm_campaign=github-airwallex-mcp) and select the integration. Connect your authorized provider account and copy its hosted MCP endpoint. Set PIPMCP_ENDPOINT and, if required, PIPMCP_TOKEN in your environment. Run npm start to produce client configuration; run npm start -- --live for a read-only connection check. Provider app presence is catalog evidence, not live verification.

## Managed service

[Continue with PipMCP](https://pipmcp.com/register?app=airwallex&utm_source=github&utm_campaign=github-airwallex-mcp). This repository is maintained by the integration team and does not imply endorsement by LinkedIn or other providers.

## Provenance and support

Source revision: abb76515adb8b00a9aa01ec7d4c718306c65f751141789639921f4e0cd5c9e53. The complete manifest is in integration.json; SHA256SUMS covers the reviewed artifact. Open a repository issue without credentials or personal data. See SECURITY.md for sensitive reports. No telemetry is sent by this code; signup links include explicit campaign parameters.

## Provider setup inventory

Run `npm start -- --setup` to inspect this app's recorded authentication requirements and setup links offline. Credentials are entered in PipMCP; this repository lists required field names only.

```json
{
  "type": "token_exchange",
  "requiredCredentialFields": [
    "provider_exchange_credentials"
  ],
  "requiredHeaderNames": [
    "x-client-id",
    "x-api-key"
  ],
  "helpUrl": "https://www.airwallex.com/docs/developer-tools/api/manage-api-keys",
  "tenantRequired": false,
  "accountParameterNames": []
}
```

Provider documentation: https://raw.githubusercontent.com/airwallex/airwallex-openapi/main/openapi/client-api/2026-08-21/airwallex-openapi-2026-08-21.json
Provider website: https://www.airwallex.com/
