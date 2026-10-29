# A developer brief for your stack

A skill that reads your codebase, discovers the projects and services behind it, and writes a brief about their latest news and releases. It adds a few suggestions for how your code could benefit.

It follows dependencies, development tools, model providers, and infrastructure. By default, it covers the past seven days, organized into top stories, shorter reads, and releases. It checks the sources first, then chooses what's worth your attention.

The skill draws on the research and editorial practices we developed while building [Lambda Brief](https://lambdabrief.dev). Copy the recipe and ask your agent to adapt it.

## Try it

Give your agent [the stack-brief skill](skills/stack-brief/SKILL.md) and access to your repository:

> Read this skill and use it to write a brief for this repository, covering the past seven days.

The recipe works across languages and ecosystems. Your agent needs access to your source code and tools for researching the web.

Run it once, review the result, and tell the agent what you'd change. Ask it to install an editable copy in your project's skills directory, or reference the file in your prompts.

## Make it a regular brief

Choose a schedule and delivery destination in your agent's routine or scheduled task:

> Every Monday at 9am Europe/London, use the stack-brief skill for this repository. Cover the past seven days and send the brief to our #engineering Slack channel.

You could use [Claude Code routines](https://claude.com/resources/articles/introducing-routines-in-claude-code), [scheduled tasks with Codex](https://learn.chatgpt.com/docs/automations), or another agent. Give the scheduled task access to the repository, research tools, and delivery destination. Check the first run because its access may differ from your interactive session.

## Make it yours

Ask for a shorter brief, another language, more engineering articles, or a different audience. Add projects you follow that aren't in your codebase. Explain where the application runs and which services matter when the repository doesn't make that clear.

The codebase hints can highlight opportunities to simplify an integration or replace custom code. Tell the agent how much detail you want.

## Improve repeat runs

**Help it read difficult sources.** Some sites need JavaScript or block simple requests. Browser tools such as [Browserbase](https://www.browserbase.com/mcp), [Browser Use](https://browser-use.com/mcp), and [Bright Data](https://github.com/brightdata/brightdata-mcp) offer proxies and CAPTCHA solving to help your agent read them. Keep the skill's short note about any sources it couldn't check. [Lambda Brief MCP](https://lambdabrief.dev/user/agents) provides the content we collect, so your agent can focus on composing the brief.

**Keep the sources you discover.** Discovery can be slow, and different runs can find different sources. Ask your agent to save the projects, repositories, blogs, and feeds it finds, along with when it checked them. Reuse that inventory and refresh it when entries grow stale or your stack changes. The agent should still check those sources for new content each run. [Lambda Brief MCP](https://lambdabrief.dev/user/agents) handles discovery for the projects it covers.

**Give the agent previous editions.** Include recent briefs or a short history of covered stories and links. Ask it to avoid repeating a story unless there's a meaningful development. Save the history and source inventory somewhere each scheduled run can access, since a fresh session may not retain them. If you miss a run, extend the next brief's date window.

## Lambda Brief

Want the brief without maintaining the research workflow? [Lambda Brief](https://lambdabrief.dev) follows release notes and official blogs and delivers a brief about the tools you use by email or Slack. There's also a free newsletter for a broader selection of developer news.

If you want your own agent to write the brief, [Lambda Brief MCP](https://lambdabrief.dev/user/agents) supplies the content we collect. Your agent brings the codebase context, and you control the writing and delivery. Check its project coverage against your stack and add any missing sources.

## License

[MIT](LICENSE). Copy and adapt the skill to your needs.
