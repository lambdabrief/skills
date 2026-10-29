# A developer brief for your stack

A skill that reads your codebase, discovers the projects and services behind it, and writes a brief about their latest news and releases—with a few suggestions for how your code could benefit.

It follows dependencies, development tools, model providers, and infrastructure. By default, it covers the past seven days, organized into top stories, shorter reads, and releases. It checks the sources first, then chooses what's worth your attention.

These are the research and editorial practices we developed while building [Lambda Brief](https://lambdabrief.dev). The skill is a short, editable recipe. Read it, copy it, and ask your agent to make it yours.

## Try it

Give your agent [the stack-brief skill](skills/stack-brief/SKILL.md) and access to your repository:

> Read this skill and use it to write a brief for this repository, covering the past seven days.

The agent needs to read your source code and research the web. The recipe works across languages and ecosystems; what it can actually check depends on the tools available to your agent.

Run it once, review the result, and tell the agent what you'd change. To keep using it, ask your agent to install an editable copy in your project's skills directory, or keep the file somewhere you can reference in your prompts.

## Make it a regular brief

Choose when to run it and where you want the result. Put those instructions in your agent's routine or scheduled task:

> Every Monday at 9am Europe/London, use the stack-brief skill for this repository. Cover the past seven days and send the brief to our #engineering Slack channel.

You could use [Claude Code routines](https://claude.com/resources/articles/introducing-routines-in-claude-code), [scheduled tasks with Codex](https://learn.chatgpt.com/docs/automations), or another agent you already use. Connect the repository, research tools, and delivery destination in that environment. Check the first scheduled run: it may have different access from your interactive session.

## Make it yours

Ask your agent to adapt the skill to your interests: a shorter brief, another language, more engineering articles, or a different audience. Add projects you follow even if they aren't in your codebase. Explain where the application runs and which services matter when that isn't clear from the repository.

The codebase hints are useful when a new capability could simplify an integration or replace custom code. Tune how many you want and how specific they should be.

## Improve repeat runs

**Help it read difficult sources.** Some sites need JavaScript or block simple requests. A browser MCP with proxies and CAPTCHA solving can help; Browserbase, Browser Use, and Bright Data are examples. Lambda Brief MCP provides collected content instead.

**Keep the sources you discover.** Discovery can be slow and vary between runs. Cache the projects, repositories, blogs, and feeds your agent finds, and refresh them as your stack changes. Keep the cache somewhere future runs can access. Lambda Brief MCP saves repeating this discovery.

**Give the agent previous editions.** Include recent briefs or a short history of covered stories so it can avoid repetition and recognize meaningful follow-ups. Make that history available to each run; fresh sessions may not remember it.

## Lambda Brief

Want the brief without maintaining the research workflow? [Lambda Brief](https://lambdabrief.dev) follows release notes and official blogs and delivers a brief about the tools you use by email or Slack. There's also a free newsletter for a broader selection of developer news.

For maintained source data with your own agent's writing and codebase context, use **Lambda Brief MCP**. Your agent uses the content we collect while you control the brief. Check its project coverage against your stack, and add sources where needed.

## License

[MIT](LICENSE). Copy and adapt the skill to your needs.
