# OpenPMM documentation

Public documentation for [OpenPMM](https://www.openpmm.com), built with [Mintlify](https://mintlify.com).

The deployed site is available at [www.openpmm.com/docs](https://www.openpmm.com/docs). Guides live in this repository. Mintlify generates the endpoint reference from the production OpenAPI document at `https://api.openpmm.com/v1/openapi.json`.

## Local development

Install the Mintlify CLI:

```bash
npm install --global mint
```

Start the local preview from this directory:

```bash
mint dev
```

Open `http://localhost:3000`.

## Validate changes

Run all documentation checks before publishing:

```bash
mint validate
mint broken-links
mint a11y
```

## Publishing

Mintlify deploys changes from the default branch through its GitHub App. A successful production API deployment also calls Mintlify's deployment trigger so changes to the remote OpenAPI document regenerate the endpoint reference.

The marketing site keeps control of `www.openpmm.com` and proxies only `/docs` to Mintlify. Do not replace the existing `www` DNS record with a Mintlify CNAME.

## Content boundaries

Use **Account**, **Workspace**, **Destination**, **Post**, and **Send** in public explanations. Do not document internal or admin routes, worker endpoints, provider credentials, or behavior that has not shipped. See [`AGENTS.md`](./AGENTS.md) for the complete writing rules.
