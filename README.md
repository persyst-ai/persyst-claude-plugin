# Persyst for Claude

[Persyst](https://www.persyst.ai) manages what your company's AI can access.
Give every team and client exactly the access they need, serve one connector
across all your clients' tools, search documents and tasks intelligently, and
let Claude read your code repositories.

It works with GitHub and GitLab, Asana, Notion, Google Drive, Search Console,
databases and other MCP servers. Writes run under each person's own connected
account, and every call is logged for administrators.

## What's inside

| Path                      | Purpose                                                 |
| ------------------------- | ------------------------------------------------------- |
| `.mcp.json`               | Persyst remote MCP server                               |
| `skills/persyst/SKILL.md` | How Claude discovers and calls your connectors          |
| `.claude-plugin/`         | Plugin manifest and a single-plugin marketplace         |

## MCP server

|           |                                                    |
| --------- | -------------------------------------------------- |
| URL       | `https://mcp.persyst.ai`                           |
| Transport | Streamable HTTP                                    |
| Auth      | OAuth 2.1 (dynamic client registration, PKCE)      |

No API key or secret is stored in this plugin. On first use, Claude opens the
Persyst sign-in page; tokens are handled and refreshed by Claude.

## Install

From the Claude plugin directory, search for **Persyst**. In Claude Code you
can also add this repository as a marketplace:

```
/plugin marketplace add persyst-ai/persyst-claude-plugin
/plugin install persyst@persyst
```

Then run `/mcp` to sign in to Persyst.

## Try it

- "What tools do I have in Persyst?"
- "Where is login handled in our code?"
- "Which Asana tasks are overdue?"
- "How many signups did we have last week?"

Databases are read-only. Writes (for example creating an Asana task) are
announced before they happen and use your own connected account.

## Support

- Website: https://www.persyst.ai
- Contact: contact@persyst.ai
- Privacy policy: https://www.persyst.ai/en/privacy-policy
- Terms of service: https://www.persyst.ai/en/terms-of-service

## License

MIT
