---
name: tool-router
description: Picks the right connected tool or skill for a job-search or content task and finds one when none is connected. Use whenever the user wants something done that needs an outside tool (find openings, read or send email, calendar, files, research, contact lookup, tracker, documents, images, slides), asks "which tool should I use", "can you connect to...", or says a connector or plugin is missing, even if they never name a tool.
---

# Tool Router

Never ask the user to attach a tool by hand. Check what is available, use it, and say plainly what was and was not used.

## Steps
1. **Check what is connected.** Use the tools listed in the session; if the right one is not loaded, search deferred tools (ToolSearch), then the connector registry (SearchMcpRegistry / SuggestConnectors) if available.
2. **Pick by task** (first available wins):
   - Open roles on employer career sites: Firecrawl, then Tavily, Exa, TinyFish. Never job boards.
   - Read/write the user's files and the private `Job-Search` folder: Google Drive.
   - Email replies and interview invites: Gmail (read and draft only). Calendar for follow-up dates.
   - Resume keywords: ResumeNext check/find skills tools.
   - Contacts: only names found on the posting, the company site, or a connected contact tool; label verified or unverified.
   - Documents, decks, images: the installed design skills (visual-document-designer, presentation-designer, image-prompt-director) plus Canva/Adobe/Gamma if connected.
3. **If nothing fits**, say which connector would fix it and where to connect it (claude.ai connector settings). Do not guess or invent results.
4. **Report honestly**: tools used, tools that failed (with the error), pages that could not be read.

## Rules
- Never apply, sign up, log in, send email, or message anyone for the user. Drafts only.
- Use only confirmed facts about the user. No invented numbers, titles, or credentials.
- Scheduled tasks can only use connectors attached to that task; if one is missing, say so instead of working around it.
- Keep personal data out of public repositories.
