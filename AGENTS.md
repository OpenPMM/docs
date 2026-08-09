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
- **API credential** is an account-owned bearer key. It can have access to all
  workspaces or selected workspaces.
- **Workspace** is the tenant boundary for destinations, assets, drafts, and
  posts.
- **Destination** is a connected social account that can receive content.
- **Post** is one channel's content and publishing state. Publishing changes
  the state of the post; it does not create a second customer object.
- **Post group** contains related channel drafts. Use this term only when you
  document the `/post-groups` resource.
- **Post submission** describes posts that were created together. The current
  wire object is `send_group`; use that exact name only when you document its
  path or response.

Do not substitute internal model names for these terms in explanatory content.

## Style preferences

- Use ASD-STE100 Simplified Technical English for all public copy.
- Use active voice and second person ("you").
- Use short sentences. Give each sentence one idea.
- Use one approved term for each object. Do not use a synonym to add variety.
- Use a verb-and-object title for an action. For example, use `Create Post`.
- Do not add an article, condition, or result to an endpoint title.
- Use sentence case for headings.
- Bold UI elements: Click **Settings**.
- Use code formatting for file names, commands, paths, parameters, and code references.
- Distinguish drafts from posts that can publish. State clearly when an action
  can publish externally.
- Use exact, tested examples. Prefer read-only examples in introductory content.

## Content boundaries

- Document only the public `/v1` API and shipped customer behavior.
- Exclude internal and admin routes, worker endpoints, provider credentials, deployment details, and unshipped behavior.
- Do not document private `/api` routes.
- Do not present the internal CLI as a public product until it ships.
- Never include real API keys, tokens, provider credentials, workspace IDs, or customer data.

## API navigation

`docs.json` sets the production OpenAPI URL on the `API reference` tab. It
lists each endpoint explicitly under Posts, Drafts, Assets, Destinations, or
Account. Keep each `METHOD /path` entry in exactly one group. Update this list
when the public API adds, removes, or moves an endpoint. Do not add an
`Endpoints` wrapper around these groups.
