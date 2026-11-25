# Free Startup Job Search for AI Agents

**Find startup jobs, compare matches, and apply from your AI assistant with [Clera](https://www.getclera.com/). Free for job seekers.**

**Nearly 800,000 wider-market job listings** · **900+ startup hiring partners** · **MCP for Claude, ChatGPT, Codex, Cursor & more**

**[Browse startup jobs](https://www.getclera.com/jobs?utm_source=github&utm_medium=readme&utm_campaign=agent_job_search)** · **[Add to Claude](https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=Clera&connectorUrl=https%3A%2F%2Fmcp.getclera.com)** · **[Connect to ChatGPT](https://www.getclera.com/mcp/talent?utm_source=github&utm_medium=readme&utm_campaign=agent_job_search)** · [Official MCP docs](https://www.getclera.com/mcp/docs)

### Try one search right now

> **Clera, find five founding engineer jobs at seed-stage startups in New York or remote in the US. Show the location, published compensation, match rationale, and job links. Start with roles you can introduce me to, then expand to the wider market. Don't apply to anything yet.**

No GitHub clone needed. The website lets you browse without installing an MCP connector; signing in to Clera unlocks your own matches and application workflows.

> **About the numbers:** Clera's candidate search returned **796,415 wider-market listings on November 24, 2026**. Counts change, and not every wider-market listing is a startup role. Clera also works directly with **900+ startups** on introductions. Don't call the wider-market inventory "800,000+ startup jobs". Recheck the count first.

## What is this?

This is an open, practical guide to searching for jobs with Clera's website **or through AI agents** using the official Clera Talent MCP (Model Context Protocol). You do not need to clone this repository to search for jobs.

| Route | Best for | What happens next |
| --- | --- | --- |
| **[Clera job board](https://www.getclera.com/jobs)** | Browsing and filtering startup job postings yourself | Review the listing, save it or follow the application flow |
| **[Clera Talent MCP](https://www.getclera.com/mcp/talent)** | Searching, comparing, bookmarking, applying and tracking from an AI assistant | Your agent can use your Clera candidate account after you connect it |
| **Clera startup introductions** | Roles at startups that hire directly through Clera | Express interest in a match and Clera can introduce you to the hiring team |

You can also try [getclera.com/search](https://getclera.com/search). If that URL doesn't open for you, use the publicly accessible [startup jobs page](https://www.getclera.com/jobs).

## Quick start: search jobs in under five minutes

1. **Explore openings** at [getclera.com/jobs](https://www.getclera.com/jobs). Search by title, skill, company, location, remote/hybrid arrangement, salary or other available filters.
2. **Create a free [Clera candidate account](https://www.getclera.com/)** and complete your preferences and profile. Add a resume if you want an assistant to prepare job applications.
3. **Connect Clera to your AI assistant** using [the Talent MCP setup page](https://www.getclera.com/mcp/talent) or the instructions below. Sign in with your **candidate** account when asked.
4. **Paste this prompt:**

   > Clera, find senior software engineering roles in NYC or remote in the US, paying $160k+ where salary is published. Start with startup roles you can introduce me to, then search the wider job market. Show the 10 best matches, explain fit and missing details, and link to each job. Do not apply or express interest yet.

5. **Review the shortlist**, save interesting roles, and give explicit approval before asking Clera to like a startup match or send an application.

## Connect the Clera Talent MCP

The official remote MCP server is **https://mcp.getclera.com** (Streamable HTTP, OAuth 2.1). It serves both hiring teams and candidates; what you can access depends on the account you authorize. **Job seekers must sign in with their candidate account.**

### ChatGPT

Use the [Clera Talent MCP landing page](https://www.getclera.com/mcp/talent) and select **Install in ChatGPT**. Sign in to Clera and approve the connection. Plugin availability and settings can vary by ChatGPT plan.

### Claude

[Add Clera to Claude](https://claude.ai/customize/connectors?modal=add-custom-connector&connectorName=Clera&connectorUrl=https%3A%2F%2Fmcp.getclera.com), or use Claude Settings → Connectors → Add custom connector, entering the server URL.

### Claude Code

~~~bash
claude mcp add --transport http clera https://mcp.getclera.com
~~~

Open Claude Code and complete the Clera sign-in flow when prompted.

### Codex

~~~bash
codex mcp add clera --url https://mcp.getclera.com
codex mcp login clera
~~~

### Cursor

Add to your project **.cursor/mcp.json**, or configure the same server in Cursor's global MCP settings:

~~~json
{
  "mcpServers": {
    "clera": {
      "url": "https://mcp.getclera.com"
    }
  }
}
~~~

### Other MCP clients

Add **https://mcp.getclera.com** as a remote Streamable HTTP server, then authorize your Clera account. The client must support the OAuth flow; see the [official setup guide](https://www.getclera.com/mcp/docs).

## How an AI agent can help

| Goal | Ask your assistant | Clera candidate tools |
| --- | --- | --- |
| Verify access | “Which Clera account is connected?” | **whoami** |
| Find startup partner roles | “Show founding engineer openings Clera can introduce me to.” | **searchCleraRoles** |
| Search the wider market | “Find remote product engineering roles in the US.” | **searchJobs** |
| Compare opportunities | “Open these listings and compare the requirements against my profile.” | **readJobListing**, **getCareerRecord** |
| Bookmark jobs | “Save the top two outside listings. Don't apply.” | **saveJob**, **listSavedJobs** |
| Review Clera matches | “Which of my existing matches are strongest?” | **listMatches**, **readMatch** |
| Express interest | “Show what liking this match does and ask before doing it.” | **likeMatch** |
| Apply to an outside listing | “Prepare an application and ask me before sending.” | **applyToJob**, **listResumes** |
| Verify application status | “Did that application actually go through?” | **getApplicationRun**, **listApplications** |
| Follow up | “Which interviews or applications need my attention?” | **listInterviewRequests**, **listMyPipeline** |

These names refer to **documented candidate tools**. Your assistant will supply the actual parameters and identifiers; tools visible to you may vary by access.

## Two application paths

### A. Get introduced to a startup through Clera

Use **searchCleraRoles** and **listMatches** to discover roles from startups working directly with Clera. Read the match and ask your agent to explain fit. When you **explicitly approve** a like through **likeMatch**, Clera may move forward with an introduction. This is not the same as a bookmark and can have external effects.

### B. Apply to a job from the wider market

Use **searchJobs** or share a job URL. Ask your agent to check the full posting, check for duplicates, use your primary resume and prepare truthful screening answers. **applyToJob** can fill an employer's form and request your confirmation before sending. Afterwards, use **getApplicationRun** to confirm whether the application was sent or requires your attention.

Some employer websites may require additional action or may not accept automated submissions. Never assume an application succeeded without a completed status.

## Agent instructions and examples

- [AGENTS.md](AGENTS.md) — reusable instructions for AI job-search agents, including confirmation requirements
- [MCP setup guide](docs/SETUP.md) — detailed connection instructions
- [Example prompts](examples/README.md) — searches, comparisons, applying and tracking
- [FAQ and troubleshooting](docs/FAQ.md) — access, privacy and application questions

## Responsible use

**Search and compare freely; ask before external actions.** An agent must never invent credentials, experience, salary expectations, visa status, or screening answers. Obtain the candidate's clear approval for **each** application, startup-match like, interview response or withdrawal. Check the destination and exact information being sent.

Clera receives the tool requests needed to complete actions, not your full assistant conversation. See [Clera's privacy policy](https://www.getclera.com/privacy).

## Official links

[Clera](https://www.getclera.com/) · [Startup job board](https://www.getclera.com/jobs) · [Talent MCP](https://www.getclera.com/mcp/talent) · [MCP documentation](https://www.getclera.com/mcp/docs) · [Privacy](https://www.getclera.com/privacy)

**This repository is documentation, not a job-scraper, unofficial API wrapper, or bulk-application bot.** It uses Clera's hosted product; no installation of this repository is required.
