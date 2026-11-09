# WhatJobs Job Search: MCP server

Search live jobs from [WhatJobs](https://www.whatjobs.com) in 58 countries, right from your AI assistant: job listings, salary ranges and comparisons in local currency, the companies hiring most, job counts across places, newly posted jobs, and jobs that fit your skills.

- **Server URL:** `https://mcp.whatjobs.com/mcp` (Streamable HTTP)
- **No sign-in:** public and read-only, nothing to set up
- **Every result links to the full job on WhatJobs**, where you apply

This repository holds documentation only. The server is hosted and maintained by WhatJobs; its source code is not public.

## Tools

| Tool | What it does |
|---|---|
| **Search jobs** (`search_jobs`) | Job listings for a role and place, with paging for more results. |
| **Latest jobs** (`search_latest_jobs`) | Only recently posted jobs: today, this week, or up to 30 days. |
| **Match jobs to profile** (`match_jobs_to_profile`) | Jobs ranked by how well they fit the job titles and skills you give. |
| **Salary insights** (`get_salary_insights`) | Typical salary range, median, lowest and highest for a role and place, in local currency. |
| **Compare salaries** (`compare_salaries`) | Pay for a role across places, or for several roles in one place, side by side. |
| **Top hiring companies** (`get_top_hiring_companies`) | The companies posting the most jobs for a role and place. |
| **Compare job counts** (`compare_job_counts`) | How many jobs are open across places or roles. |

All tools are read-only. In assistants that support [MCP Apps](https://modelcontextprotocol.io/extensions/apps/overview), results appear in an interactive view; elsewhere they come back as text with links.

## Connect

### VS Code (GitHub Copilot)

Add this to your `mcp.json`:

```json
{
  "servers": {
    "whatjobs": {
      "type": "http",
      "url": "https://mcp.whatjobs.com/mcp"
    }
  }
}
```

### ChatGPT

Install the WhatJobs app: <https://chatgpt.com/plugins/plugin_asdk_app_6a34f8f6261c8191aac9bc8d7db3502f>

### Claude

Settings > Connectors > **Add custom connector**, then enter `https://mcp.whatjobs.com/mcp`.

### Cursor

Add this to your MCP settings:

```json
{
  "mcpServers": {
    "whatjobs": {
      "url": "https://mcp.whatjobs.com/mcp"
    }
  }
}
```

### Any other MCP client

Connect to `https://mcp.whatjobs.com/mcp` over Streamable HTTP. No API key or authentication is needed.

## Try it

- "Find nurse jobs in London on WhatJobs"
- "How much does a data analyst earn in Berlin? Use WhatJobs"
- "Compare nurse salaries in London, Manchester and Leeds"
- "Who is hiring software engineers in Toronto?"
- "Show electrician jobs posted this week in Manchester"
- "I'm a data analyst with SQL and Power BI. Which jobs in London fit me?"

## Countries

United Kingdom, United States, Canada, Germany, India, Pakistan, Brazil, Spain, United Arab Emirates, Mexico, Argentina, South Africa, Austria, Australia, Belgium, Bahrain, Chile, Colombia, Costa Rica, Switzerland, Dominican Republic, Algeria, Nigeria, Netherlands, France, Denmark, Egypt, Indonesia, Malaysia, Oman, Philippines, Qatar, Saudi Arabia, Singapore, Tanzania, Uganda, Finland, Greece, Guatemala, Hong Kong, Ireland, Italy, Kuwait, Lithuania, Luxembourg, Morocco, Norway, New Zealand, Panama, Peru, Poland, Puerto Rico, Portugal, Russia, Sweden, Thailand, Turkey and Venezuela.

## More

- **Documentation:** <https://mcp.whatjobs.com/docs>
- **Official MCP Registry:** `com.whatjobs.mcp/job-search`
- **Privacy policy:** <https://www.whatjobs.com/info/legal/whatjobs-privacy-policy/>
- **Support:** helpdesk@whatjobs.com

© WhatJobs Ltd
