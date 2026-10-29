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

**Keep the sources you discover.** Discovery can be slow, and different runs can find different sources. Ask your agent to save a reviewed inventory of projects, repositories, blogs, feeds, and verification dates. Record when a project has no blog, too. Refresh stale entries and revisit the inventory when your stack changes. Cache where to look; still check for new content each run. [Lambda Brief MCP](#lambda-brief), currently in development, is another way to avoid repeating discovery.

**Give the agent previous editions.** Include recent briefs or a compact history of covered stories and links. Ask it to avoid repeating a story unless there's a meaningful development. Save that history and any source cache somewhere the next run can access; a fresh session may not retain either. If a run is missed, extend the next brief's date window.

**Help it read difficult sources.** Some sites need JavaScript or block simple requests. A browser MCP such as [Browserbase](https://www.browserbase.com/mcp) can help; its browser infrastructure supports [proxies and CAPTCHA solving](https://docs.browserbase.com/platform/identity/overview). Lambda Brief MCP is also intended to provide already collected content. Neither approach can supply a publication date a source doesn't establish. Keep the skill's short note about unresolved gaps so missing coverage stays visible.

**Review and refine.** The agent can miss a service, misread release notes, or choose stories you don't care about. Review the initial source inventory and a few editions, then feed those corrections back into your copy of the skill. You can ask it to check every source while still keeping the final brief short.

## Lambda Brief

Want the brief without maintaining the research workflow? [Lambda Brief](https://lambdabrief.dev) follows release notes and official blogs and delivers a brief about the tools you use by email or Slack. There's also a free newsletter for a broader selection of developer news.

We're building **Lambda Brief MCP** for people who want maintained source data and their own agent's writing and codebase context. It will let your agent use the content we collect while you control the brief. Check its project coverage against the stack your agent discovers, and add sources where needed.

## License

[MIT](LICENSE). Copy and adapt the skill to your needs.
