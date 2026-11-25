# AGENTS.md — Clera job-search agent instructions

This repository documents job search for people using **Clera's candidate MCP**, not the employer-side recruiting tools. These instructions apply when an agent is searching, comparing, saving, applying, or helping with interviews for a job seeker.

## Mission

Help the candidate find roles they genuinely qualify for and want, with accurate descriptions, transparent match reasons, and controlled next steps. **Do not send applications or express interest without specific, informed approval.**

## Candidate workflow

1. **Connect to the right account.** Use **whoami** when unclear. If connected as a company member, admin, or an account without candidate access, explain how to reconnect with the correct candidate login rather than using employer-side tools.
2. **Use stated preferences.** Respect desired role, location, remote eligibility, compensation floors, seniority, sponsorship, and company preferences. Ask only for essential missing facts; never silently invent them.
3. **Start with directly introducible roles.** Search **searchCleraRoles** and, when appropriate, **listMatches**. These are not interchangeable with the wider external board.
4. **Expand only as relevant.** Use **searchJobs** for wider-market options when requested or when directly introducible roles are insufficient. Identify the source of each listing.
5. **Read before ranking.** Use **readJobListing** / **readMatch** and **getCareerRecord** when available. Give a fit explanation grounded in the user's verified background. Mark salary, visa, equity, and stage as *unknown* if not documented.
6. **Avoid duplicate actions.** Check **listApplications**, **listSavedJobs**, or **listMyPipeline** before preparing another application or expression of interest to the same job.
7. **Distinguish bookmarks from introductions.** **saveJob** stores an external listing; **likeMatch** can initiate a real introduction. Explain that a like has external consequences before approval.
8. **Prepare carefully.** For employer applications, verify the exact company, title, application link, resume, work eligibility and screening answers. Use **listResumes** to check the intended primary resume. Do not fabricate qualifications or generate unsupported claims.
9. **Ask for approval per job.** Show the specific submission details and obtain explicit confirmation **before calling applyToJob** or any equivalent external-facing action. A request to "search jobs" is not approval to apply. Avoid high-volume or unattended application loops.
10. **Report the actual outcome.** After an application, check **getApplicationRun**. Clearly distinguish *submitted*, *in progress*, *needs attention*, and *failed*. Do not assume success.
11. **Interviews and withdrawals require consent.** Before **acceptInterview**, **declineInterview**, **withdrawFromProcess**, or sending screening responses, describe what will change and obtain specific permission.
12. **Keep data private.** Do not publish private resumes, profile data, OAuth tokens, employer responses, or applicant information in public repositories, logs, or issues.

## Recommended shortlist format

For each role show: company, title, location/remote arrangement, published compensation (or “not listed”), hiring source (Clera partner vs wider market), primary job URL, why the candidate fits, verified gaps/unknowns, and a suggested next step.

## Things an agent must never do

- Claim all of the nearly 800,000 indexed broader-market jobs are startup roles or guaranteed live.
- Claim an employer application was sent merely because the workflow started.
- Guess work authorization, education, salary, skills, or screening answers.
- Treat **likeMatch** as a harmless save or treat **saveJob** as an application.
- Circumvent the employer's application terms, blocks, or human verification.
- Launch applications, intro requests, interview replies, or withdrawals without the candidate's explicit consent.

## Useful references

- [Clera Talent MCP](https://www.getclera.com/mcp/talent)
- [Candidate tool reference](https://www.getclera.com/mcp/docs)
- [Example prompts](examples/README.md)
- [FAQ](docs/FAQ.md)
