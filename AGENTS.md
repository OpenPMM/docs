# OpenPMM documentation instructions

## About this project

- This is the public OpenPMM documentation site built with [Mintlify](https://mintlify.com).
- Pages are MDX files with YAML frontmatter.
- Configuration lives in `docs.json`.
- The public API reference is generated from `https://api.openpmm.com/v1/openapi.json`.
- Use the Mintlify MCP server, `https://mcp.mintlify.com`, for content and settings when it is available.
- Use the Mintlify docs MCP server, `https://www.mintlify.com/docs/mcp`, for current Mintlify product guidance.

## Public terminology

- **Account** is a person's OpenPMM identity.
- **Workspace** is the tenant boundary for API keys, destinations, and posts.
- **Destination** is a connected social account that can receive content.
- **Post** is content prepared for one destination.
- **Send** is the durable result of confirmed publishing work. Use the exact API resource name when documenting an endpoint.

Do not substitute internal model names for these terms in explanatory content.

## Style preferences

- Use active voice and second person ("you").
- Keep sentences concise. Give each sentence one idea.
- Use sentence case for headings.
- Bold UI elements: Click **Settings**.
- Use code formatting for file names, commands, paths, parameters, and code references.
- Distinguish editable posts from confirmed sends. State clearly when an action can publish externally.
- Use exact, tested examples. Prefer read-only examples in introductory content.

## Content boundaries

- Document only the public `/v1` API and shipped customer behavior.
- Exclude internal and admin routes, worker endpoints, provider credentials, deployment details, and unshipped behavior.
- Do not document private `/api` routes.
- Do not present the internal CLI as a public product until it ships.
- Never include real API keys, tokens, provider credentials, workspace IDs, or customer data.
