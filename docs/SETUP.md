# Connect Clera's Talent MCP to an AI assistant

The official **Clera Talent MCP** works for job seekers who sign in with a Clera **candidate account**. The same server also supports employers, but the tool list depends on the account.

- **Server URL:** https://mcp.getclera.com
- **Transport:** Streamable HTTP
- **Authentication:** OAuth 2.1 through a Clera login
- **Cost for candidates:** Free
- **Official instructions:** https://www.getclera.com/mcp/docs
- **Job-seeker overview:** https://www.getclera.com/mcp/talent

You do **not** need to download this repository or run a local search server.

## Before connecting

1. Create or sign in to a free account at https://www.getclera.com/.
2. Complete the candidate profile and job preferences.
3. Upload a resume if you plan to apply to external roles. Confirm the correct resume is primary.
4. Connect using the same candidate account. The first tool request can open an OAuth consent window.

## ChatGPT

Open https://www.getclera.com/mcp/talent and use **Install in ChatGPT**. Follow the connector setup and OAuth login flow. The available app menus depend on your ChatGPT access and settings; the landing page is the canonical current installation route.

## Claude

Use the official [Add to Claude](https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=Clera&connectorUrl=https%3A%2F%2Fmcp.getclera.com) link, or navigate to **Settings → Connectors → Add custom connector** and paste https://mcp.getclera.com.

## Claude Code

~~~bash
claude mcp add --transport http clera https://mcp.getclera.com
~~~

Open Claude Code, call a Clera tool or open its MCP controls, and complete the sign-in flow.

## Codex

~~~bash
codex mcp add clera --url https://mcp.getclera.com
codex mcp login clera
~~~

Sign in to Clera and approve OAuth access.

## Cursor

Create **.cursor/mcp.json** in your project (or add the same configuration globally in Cursor's MCP settings):

~~~json
{
  "mcpServers": {
    "clera": {
      "url": "https://mcp.getclera.com"
    }
  }
}
~~~

Complete the browser sign-in when Cursor prompts you.

## Claude Desktop using an MCP bridge

Where native remote MCP connectors aren't available, the official docs provide this **claude_desktop_config.json** example:

~~~json
{
  "mcpServers": {
    "clera": {
      "command": "npx",
      "args": ["mcp-remote", "https://mcp.getclera.com"]
    }
  }
}
~~~

It requires Node.js and permission to run the bridge. Prefer native remote MCP where supported.

## Verify your connection

Ask your assistant:

> Use Clera to run **whoami**. Confirm I am connected as a **candidate**. Then search for three relevant startup roles, but don't like or apply to any yet.

Useful candidate tools include **searchCleraRoles**, **searchJobs**, **readJobListing**, **saveJob**, **listMatches**, **applyToJob**, **getApplicationRun**, and **listApplications**.

## Troubleshooting

- **Account kind is wrong:** Reconnect with your candidate email and reauthorize the tool.
- **Only whoami or no tools appear:** Complete OAuth, then remove and re-add the connector if your account role changed; clients may cache tool lists.
- **Sign-in loops:** Confirm remote MCP OAuth support, permit browser redirects, and follow the [official troubleshooting page](https://www.getclera.com/mcp/docs).
- **Job-search URL not loading:** Use https://www.getclera.com/jobs instead of https://getclera.com/search.
- **Application result unclear:** Read the status with **getApplicationRun** before claiming success.
- **Need help:** Contact Clera using the support information in its [official docs](https://www.getclera.com/mcp/docs).

**Privacy:** Your assistant sends Clera the specific tool requests it makes, not your whole assistant chat. Remove the connector in your AI client to disconnect. Review https://www.getclera.com/privacy.
