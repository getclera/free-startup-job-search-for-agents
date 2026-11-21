# Copy/paste prompts for AI job-search agents

Connect the [Clera Talent MCP](https://www.getclera.com/mcp/talent) to Claude, ChatGPT, Codex, Cursor or another supported assistant. Use the prompts below as starting points, adjusting location, compensation and role to your actual preferences.

## 1. Find the best startup roles

> Clera, find senior backend or full-stack engineering roles in New York City or remote in the US. Prefer seed to Series B startups and a base salary of at least $160,000 **where compensation is published**. Start with roles Clera can introduce me to, then search the wider market. Show the 10 best options with source links, fit rationale and missing information. Don't apply or like anything yet.

**Likely tools:** searchCleraRoles, searchJobs, readJobListing.

## 2. Explore jobs without connecting MCP

> Help me search https://www.getclera.com/jobs for founding engineer, product engineer and applied AI roles. Explain how to filter by location, stage, salary and remote work. For interesting roles, summarize the company, published requirements and next action. If the website cannot be accessed, don't invent search results.

**Route:** Clera website. You can also try https://getclera.com/search, with **/jobs** as the fallback.

## 3. Rank jobs using my actual background

> Use Clera to read the details of these five jobs and compare their requirements against my career record. Rank them by fit and explain where my experience is strong or missing. Keep unknown pay, visa, equity or stage details clearly labeled. Don't take any external actions.

**Likely tools:** readJobListing, getCareerRecord, readPreferences.

## 4. Save the strongest listings

> From the last shortlist, bookmark the two strongest external job-board roles in Clera. Do not like any partner-company matches and do not apply. Show me the jobs you saved.

**Likely tools:** saveJob, listSavedJobs.

## 5. Request a startup introduction

> Show me the full details of my top Clera match and explain whether I'm a strong fit. Tell me what will happen if I like this match. Ask me for explicit approval before telling Clera I'm interested.

**Likely tools:** listMatches, readMatch, likeMatch (only after confirmation).

## 6. Prepare an external job application

> Review this posting: [PASTE JOB URL]. Check whether I already applied. Use my primary resume and only verified facts from my Clera candidate profile to draft answers. Show me the employer, job, destination, resume and every screening answer **before sending anything**. Ask me to confirm this one application. After an approved submission, inspect the application-run status and report whether it was sent.

**Likely tools:** readJobListing, listApplications, listResumes, applyToJob, getApplicationRun.

## 7. Find roles with visa sponsorship

> Find senior software engineering roles in London or Berlin where visa sponsorship is explicitly supported. Start with Clera partner roles, then check wider-market postings. Do not infer sponsorship from location or missing data. Show which evidence supports each result.

**Likely tools:** searchCleraRoles, searchJobs, readJobListing.

## 8. Track applications and interviews

> Use Clera to show my saved jobs, tracked applications, pending interview requests, and anything needing follow-up. Group by next action. Do not accept interviews, withdraw from processes or contact companies without approval.

**Likely tools:** listSavedJobs, listApplications, listInterviewRequests, listMyPipeline.

## 9. Improve my profile before applying

> Use Clera to review my job-search preferences, career history, primary resume, and profile strength. Find information gaps that could make matching or application answers inaccurate. Suggest fixes but ask me before editing my profile or changing my resume.

**Likely tools:** readPreferences, getCareerRecord, listResumes, getProfileStrength.

## 10. Use an agent safely over a long search

> Search for suitable new jobs and keep a shortlist with title, company, work arrangement, listed pay, URL, source and reasons for fit. Do not repeat previously rejected or applied-to jobs. You may suggest applications, but **never apply, like matches, answer screening questions, or reply to interviews without my explicit approval for each action**. Verify results before reporting success.

## Notes

- Clera's candidate tool names and available workflows are listed in the [official documentation](https://www.getclera.com/mcp/docs).
- A Clera startup introduction (**likeMatch**) and an external application (**applyToJob**) are **different actions**.
- Job availability, compensation, work arrangement and sponsorship may change after an index update.
- Share only necessary candidate details with your connected agent and never publish private resumes or OAuth credentials in GitHub.
