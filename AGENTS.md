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
- **Workspace** is the tenant boundary for destinations, assets, and Posts.
- **Destination** is a connected publishing target.
- **Post** is one channel's content and publishing state. Publishing changes
  the state of the post; it does not create a second customer object.
- **Post Set** is the immediate response envelope for Posts accepted together.
  It is not a durable resource.
- **Group** is an optional caller-defined label for related Posts. You can use
  it to filter the Post collection.

Do not substitute internal model names for these terms in explanatory content.

## Simplified Technical English

Write every public page in ASD-STE100 Simplified Technical English. This is a
requirement, not a preference.

- Use one idea for each sentence. Keep a descriptive sentence to 20 words or
  fewer, and an instruction to 20 words or fewer.
- Use the active voice. Use the passive voice only when the actor is unknown.
- Use the simple present tense. Do not use a gerund or a participle as a verb.
  Write "OpenPMM checks the file", not "OpenPMM is checking the file".
- Use one word for one meaning. Do not use a synonym for variety.
- Use articles ("the", "a") and complete sentences. Do not use telegraphic text.
- Prefer short, common words. Write "make sure" instead of "ensure", and "use"
  instead of "utilize".
- Do not use Latin abbreviations. Write "for example" instead of "e.g.".
- Give a number and a unit for each limit. For example, write "60 fps maximum".
- Do not use idioms, humor, or marketing adjectives.
- Give a warning or a caution before the step that it applies to.

## Style preferences

- Use active voice and second person ("you").
- Use short sentences. Give each sentence one idea.
- Use one approved term for each object. Do not use a synonym to add variety.
- Use a verb-and-object title for an action. For example, use `Create Post`.
- Do not add an article, condition, or result to an endpoint title.
- Use sentence case for headings.
- Bold UI elements: Click **Settings**.
- Use code formatting for file names, commands, paths, parameters, and code references.
- A draft is a Post state. State clearly when an action can publish externally.
- Use exact, tested examples. Prefer read-only examples in introductory content.

## Content boundaries

- Document only the public `/v1` API and shipped customer behavior.
- Exclude internal and admin routes, worker endpoints, provider credentials, deployment details, and unshipped behavior.
- Do not document private `/api` routes.
- Do not present the internal CLI as a public product until it ships.
- Never include real API keys, tokens, provider credentials, workspace IDs, or customer data.
- Do not leak internal technical details. Examples are module names, database
  tables and columns, queue and worker names, command-line tools, file paths,
  and internal error classes. Describe what the customer sees and does.
- Do not write about a plan, a phase, or a future feature. Do not use "yet",
  "soon", "for now", or "in a future release". Document the current behavior in
  the simple present tense.
- Verify each value against the shipped code or the live OpenAPI document
  before you publish it. Do not copy a limit from a plan document.

## Media guidelines pages

- `media/overview.mdx` holds the general rules. One page for each channel holds
  the exact limits, and the overview links to them with a `CardGroup`.
- Give the owner of each limit: OpenPMM, the provider, or the destination.
- State an OpenPMM product limit that is lower than the provider limit. The
  500 MiB upload limit is an example.
- Link to the first-party provider document at the end of each channel page.
- Update these pages when the channel limits in the product change.

## API navigation

`docs.json` sets the production OpenAPI URL on the `API reference` tab. It
lists each endpoint explicitly in a task-oriented group. Keep each
`METHOD /path` entry in exactly one group. Update this list when the public API
adds, removes, or moves an endpoint. Do not add an `Endpoints` wrapper around
these groups. Mintlify treats the explicit `pages` arrays as an allow-list, so
an omitted operation does not appear in the published API reference.
