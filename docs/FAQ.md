# FAQ and troubleshooting

## Is Clera really free for job seekers?

Yes. Clera's Talent MCP and job-search product are free for candidates. Employers pay Clera when they hire through Clera. See the [Talent MCP overview](https://www.getclera.com/mcp/talent).

## Is this a list of 800,000 startup jobs?

Not exactly. A live check of the **wider-market searchJobs index returned 796,415 listings on November 24, 2026**, and the count changes. These are *wider-market job listings*, not necessarily all startup roles or all currently open. Clera also works directly with **900+ startups** whose roles may be accessible through matches and introductions, including roles not on the public board.

## Where can I search without an AI assistant?

Use the publicly accessible [Clera startup jobs board](https://www.getclera.com/jobs). This guide also links [getclera.com/search](https://getclera.com/search), but if that route is unavailable or redirects unexpectedly, use the job board at **/jobs**.

## Do I have to clone this GitHub repository?

No. It contains setup instructions and prompts, not an application to install. The actual search and application tools are hosted by Clera.

## Is the MCP server different for candidates and employers?

Both use **https://mcp.getclera.com**. You see candidate tools when you authorize a candidate account; hiring-team accounts expose different capabilities. Ask **whoami** to confirm which account is connected.

## What is the difference between searchCleraRoles and searchJobs?

**searchCleraRoles** retrieves roles at startups working with Clera where Clera can facilitate an introduction. **searchJobs** searches the broader job market. Listings from the latter may point to external employer application forms.

## Can Clera apply for me?

The documented **applyToJob** tool can prepare and fill an outside employer's application with your Clera profile and primary resume, then send it **after you explicitly confirm**. Some websites may still require manual steps or might not support automation. Use **getApplicationRun** to confirm the real submission result.

## Can I apply to everything automatically?

This guide does not endorse indiscriminate or unattended mass applications. Review each job and proposed submission, check duplicates, answer screening questions truthfully and approve each application. Sending an application is a meaningful external action.

## What does liking a Clera match do?

**likeMatch** tells Clera you want to be considered and may trigger an introduction. It is not just a bookmark and can have consequences outside your account. Use **saveJob** to bookmark an external listing instead.

## Does saving an external job submit an application?

No. **saveJob** is a bookmark. **applyToJob** is a separate, explicit write action.

## Can I see pending interviews and past applications?

Yes, candidate tools include **listInterviewRequests**, **listMyPipeline** and **listApplications**. Your assistant should report what needs action without accepting or declining anything on your behalf unless you approve.

## How do I check that the MCP connection worked?

Ask your assistant to use **whoami**. If it returns an unexpected account type, reconnect using your candidate login and verify OAuth consent.

## Why are only some tools visible?

Permissions depend on your signed-in Clera account, and MCP clients can cache tool lists. Complete sign-in and reconnect after changing accounts. See [Clera MCP troubleshooting](https://www.getclera.com/mcp/docs).

## What if a job has no salary or visa information?

Ask the assistant to mark it as unknown, check the primary posting, and ask the employer if needed. Don't treat a missing field as evidence that a job sponsors visas or meets a pay floor.

## What data does Clera receive?

Clera documents that it sees the arguments and results of relevant tool calls, not your entire AI chat. Check [Clera's privacy policy](https://www.getclera.com/privacy). Keep OAuth tokens and personal application information out of public repositories.

## Can I disconnect?

Yes. Remove Clera from your assistant's connectors or plugins. For account issues, follow the [official support guidance](https://www.getclera.com/mcp/docs).

## More help

- [Official talent MCP page](https://www.getclera.com/mcp/talent)
- [Official MCP tools and setup](https://www.getclera.com/mcp/docs)
- [Step-by-step setup](SETUP.md)
- [Copy/paste prompts](../examples/README.md)
