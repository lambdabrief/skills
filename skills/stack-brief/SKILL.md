---
name: stack-brief
description: Write a developer newsletter covering recent news and releases from the projects behind a repository's stack, with a few short hints about opportunities for its codebase. Use when asked for a weekly brief or news about the project's stack.
---

# Stack Brief

Write a developer newsletter about the projects behind this repository's stack: what happened, what's interesting, and why a developer would care. The repository establishes which projects to follow. Cover the past seven days unless the request specifies another period.

## Understand the stack

Build a working list of the repository's direct dependencies, development tools, runtimes, and third-party services. Look across workspaces, source code, and build and infrastructure configuration as well as package files. Services called over HTTP or used for hosting, storage, and deployment may have no SDK dependency.

Include model providers and underlying services used through gateways or wrappers. Identify hosting and infrastructure providers from deployment configuration, CI workflows, source, and documentation; distinguish confirmed usage from examples or unused configuration.

For example, JavaScript projects describe packages in `package.json` and resolve versions in lockfiles; Python projects may use `pyproject.toml`, requirements files, and lockfiles. Follow the equivalent sources for any ecosystem. Record resolved versions where available, keeping them distinct from declared version ranges; leave unknown versions unknown.

Read enough of the code to understand what the project is building. This context can suggest a few useful connections when writing the brief.

## Find the sources

For each package, follow registry metadata and upstream documentation to its repository and release notes. Find the official project homepage and blog behind each repository and service, including product changelogs where useful. Small libraries may have only a repository; a service may have no public repository.

Research related packages together, while keeping their versions and changes distinct. In monorepos, the useful notes may be in a package's own changelog or a shared release; follow links from stub release pages and match notes to the actual package and version. An SDK's releases and its service's product news cover different things.

Use an authenticated GitHub connection when available. Group release lookups by upstream repository and reuse the results for its packages; batch reads where supported and avoid bursts of concurrent requests. When rate-limited, respect the server's retry/reset guidance and use official release pages or changelogs where practical.

Prefer official sources. A feed can help discover articles, but check it against the blog: a working feed can be stale or cover a different part of the site. Read the blog directly when needed, and check a shared vendor blog once.

If a source cannot be read with a simple fetch, try another suitable method, such as a browser for JavaScript-rendered pages.

## Read the week's developments

Check release activity and official article sources for every dependency, tool, service, and model provider in the inventory. Check shared sources once. A project may have no blog, but establish that through discovery rather than skipping it. Prioritization determines research order, not which sources get checked.

Find releases and articles published within the chosen period. Follow each project's broader news, including new products, research, engineering lessons, and changes of stewardship, even when they don't touch an API used here. Use publication dates rather than search-engine freshness or a page's last modification. Read the original notes and articles, following through to substantive content instead of summarizing titles or excerpts as though they were the full source.

Preserve concrete facts and qualifications: versions, affected APIs, deadlines, and whether something is experimental, in preview, or generally available. Don't infer breaking changes or security severity from version numbers. Claims about this repository being affected need evidence from both the source and the code.

Combine sources about the same development, including release notes and their announcement. Distinguish a newly published explanation of an older feature from a new capability. Keep prereleases clearly labeled and routine canary builds from dominating the brief.

## Compose the brief

Curate only after completing the source scan. Read the full sources behind candidate stories before selecting and writing them. If a source cannot be checked, report the unresolved gap; don't treat it as having no news.

Choose and order stories by how much a developer following these projects would be glad to hear about them: a substantial capability, surprising research result, revealing engineering lesson, or significant change to a project. Judge across the whole edition; source volume and an available upgrade don't make a story important. Skip promotion and routine maintenance.

Use this structure as a starting point, adapting it to the request and the week's material:

- **Opening:** the covered dates and a short preview of the biggest developments.
- **Top stories:** the few developments that deserve the most attention, with a linked headline and two or three sentences each.
- **Also:** smaller stories and worthwhile reads, usually a linked headline and one sentence each.
- **Releases:** compact package/version links with a short description of what shipped. An exceptional release can earn a top story; avoid repeating its details.

Write like a colleague who follows these projects closely: plain language, concrete changes, and a memorable source detail where it helps. Explain the news before considering its application here. Let the substance set the length and omit empty sections; don't fill a quota.

Add a few short codebase hints beside the relevant stories or releases when there's a concrete opportunity. For example, a new capability might replace custom code or simplify an integration. One sentence is usually enough, with a file or symbol only when it helps locate the opportunity. Keep upgrade procedures, compatibility checklists, and explanations of why unrelated features don't apply out of the brief.

Include a coverage note only for unresolved problems that materially limit the brief: name the source, what couldn't be checked, and the observed reason. Omit successful checks, recovered errors, and research narration.
