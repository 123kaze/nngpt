# chars = sorted(list(set(text)))
vocab_size = len(c
_Exported on 10/19/2026 at 02:30:10 GMT+8 from OpenAI Codex via WayLog_


**OpenAI Codex**

<skills_instructions>
## Skills
A skill is a set of local instructions to follow that is stored in a `SKILL.md` file. Below is the list of skills that can be used. Each entry includes a name, description, and a short path that can be expanded into an absolute path using the skill roots table.
### Skill roots
- `r0` = `C:/Users/hsx1231ol/.codex/skills`
- `r1` = `C:/Users/hsx1231ol/.codex/skills/.system`
- `r2` = `C:/Users/hsx1231ol/.codex/plugins/cache/openai-bundled`
- `r3` = `C:/Users/hsx1231ol/.codex/plugins/cache/openai-curated-remote/google-drive/0.1.22/skills`
- `r4` = `C:/Users/hsx1231ol/.codex/plugins/cache/openai-curated-remote`
- `r5` = `C:/Users/hsx1231ol/.codex/plugins/cache/openai-curated-remote/sites/1.0.2-remix-b.1/skills`
- `r6` = `C:/Users/hsx1231ol/.codex/plugins/cache/openai-curated-remote/work-pets/0.1.6/skills`
- `r7` = `C:/Users/hsx1231ol/.codex/plugins/cache/openai-primary-runtime`
- `r8` = `C:/Users/hsx1231ol/.codex/plugins/cache/openai-primary-runtime/spreadsheets/26.1015.12040/skills`
### Available skills
- imagegen: Generate or edit raster images when the task benefits from AI-created bitmap visuals such as photos, illustrations, textures, sprites, mockups, or transparent-background cutouts. Use when Codex should create a brand-new image, transform an existing image, or derive visual variants from references, and the output should be a bitmap asset rather than repo-native code or vector. Do not use when the task is better handled by editing existing SVG/vector/code-native assets, extending an established icon or logo system, or building the visual directly in HTML/CSS/canvas. (file: r1/imagegen/SKILL.md)
- openai-docs: Use for Codex models/pricing, scheduled tasks, skills, settings, setup, troubleshooting, customization, automations, and self-knowledge—including 'you,' 'your,' 'this app,' or 'this coding agent' when they refer to Codex—and for OpenAI APIs/products and ChatGPT Work. Also use for model choice/migration, prompting, SDKs, Responses, Realtime, agents, evals, and Chat/Work/Codex comparisons. Do not use for generic app/software tasks that merely mention Codex. (file: r1/openai-docs/SKILL.md)
- skill-creator: Create or update a Codex skill with appropriately scoped instructions and any needed supporting resources. (file: r1/skill-creator/SKILL.md)
- skill-installer: Install Codex skills into $CODEX_HOME/skills from a curated list or a GitHub repo path. Use when a user asks to list installable skills, install a curated skill, or install a skill from another repo (including private repos). (file: r1/skill-installer/SKILL.md)
- aspnet-core: Build, review, refactor, or architect ASP.NET Core web applications using current official guidance for .NET web development. Use when working on Blazor Web Apps, Razor Pages, MVC, Minimal APIs, controller-based Web APIs, SignalR, gRPC, middleware, dependency injection, configuration, authentication, authorization, testing, performance, deployment, or ASP.NET Core upgrades. (file: r0/aspnet-core/SKILL.md)
- brainstorming-research: Use before writing any paper - clarifies paper type, discipline, topic, methodology, and chapter structure through natural dialogue (file: r0/brainstorming-research/SKILL.md)
- chatgpt-apps: Build, scaffold, refactor, and troubleshoot ChatGPT Apps SDK applications that combine an MCP server and widget UI. Use when Codex needs to design tools, register UI resources, wire the MCP Apps bridge or ChatGPT compatibility APIs, apply Apps SDK metadata or CSP or domain settings, or produce a docs-aligned project scaffold. Prefer a docs-first workflow by invoking the openai-docs skill or OpenAI developer docs MCP tools before generating code. (file: r0/chatgpt-apps/SKILL.md)
- cli-creator: Build a composable CLI for Codex from API docs, an OpenAPI spec, existing curl examples, an SDK, a web app, an admin tool, or a local script. Use when the user wants Codex to create a command-line tool that can run from any repo, expose composable read/write commands, return stable JSON, manage auth, and pair with a companion skill. (file: r0/cli-creator/SKILL.md)
- cloudflare-deploy: Deploy applications and infrastructure to Cloudflare using Workers, Pages, and related platform services. Use when the user asks to deploy, host, publish, or set up a project on Cloudflare. (file: r0/cloudflare-deploy/SKILL.md)
- computer-use:computer-use: Control Windows apps from ChatGPT (file: r2/computer-use/26.1013.40934/skills/computer-use/SKILL.md)
- documents:documents: Create, edit, redline, and comment on `.docx`, Word, and Google Docs-targeted document artifacts inside the container, with a strict render-and-verify workflow. Use `render_docx.py` to generate page PNGs (and optional PDF) for visual QA, then iterate until layout is flawless before delivering the final document. (file: r7/documents/26.1015.12040/skills/documents/SKILL.md)
- environment-setup: Use when Python environment setup is needed for data visualization or conda installation is required (file: r0/environment-setup/SKILL.md)
- evidence-driven-writing: Use when writing or revising Introduction, Related Work, background, literature synthesis, or any section where references must drive claims (file: r0/evidence-driven-writing/SKILL.md)
- experiment-results-planning: Use when designing experiments, result tables, mock planning data, evaluation protocols, or results sections before real data are final (file: r0/experiment-results-planning/SKILL.md)
- figma: Use the Figma MCP server to fetch design context, screenshots, variables, and assets from Figma, and to translate Figma nodes into production code. Trigger when a task involves Figma URLs, node IDs, design-to-code implementation, or Figma MCP setup and troubleshooting. (file: r0/figma/SKILL.md)
- figma-code-connect-components: Connects Figma design components to code components using Code Connect mapping tools. Use when user says "code connect", "connect this component to code", "map this component", "link component to code", "create code connect mapping", or wants to establish mappings between Figma designs and code implementations. For canvas writes via `use_figma`, use `figma-use`. (file: r0/figma-code-connect-components/SKILL.md)
- figma-create-design-system-rules: Generates custom design system rules for the user's codebase. Use when user says "create design system rules", "generate rules for my project", "set up design rules", "customize design system guidelines", or wants to establish project-specific conventions for Figma-to-code workflows. Requires Figma MCP server connection. (file: r0/figma-create-design-system-rules/SKILL.md)
- figma-create-new-file: Create a new blank Figma file. Use when the user wants to create a new Figma design or FigJam file, or when you need a new file before calling use_figma. Handles plan resolution via whoami if needed. Usage — /figma-create-new-file [editorType] [fileName] (e.g. /figma-create-new-file figjam My Whiteboard) (file: r0/figma-create-new-file/SKILL.md)
- figma-generate-design: Use this skill alongside figma-use when the task involves translating an application page, view, or multi-section layout into Figma. Triggers: 'write to Figma', 'create in Figma from code', 'push page to Figma', 'take this app/page and build it in Figma', 'create a screen', 'build a landing page in Figma', 'update the Figma screen to match code'. This is the preferred workflow skill whenever the user wants to build or update a full page, screen, or view in Figma from code or a description. Discovers design system components, variables, and styles via search_design_system, imports them, and assembles screens incrementally section-by-section using design system tokens instead of hardcoded values. (file: r0/figma-generate-design/SKILL.md)
- figma-generate-library: Build or update a professional-grade design system in Figma from a codebase. Use when the user wants to create variables/tokens, build component libraries, set up theming (light/dark modes), document foundations, or reconcile gaps between code and Figma. This skill teaches WHAT to build and in WHAT ORDER — it complements the `figma-use` skill which teaches HOW to call the Plugin API. Both skills should be loaded together. (file: r0/figma-generate-library/SKILL.md)
- figma-implement-design: Translates Figma designs into production-ready application code with 1:1 visual fidelity. Use when implementing UI code from Figma files, when user mentions "implement design", "generate code", "implement component", provides Figma URLs, or asks to build components matching Figma specs. For Figma canvas writes via `use_figma`, use `figma-use`. (file: r0/figma-implement-design/SKILL.md)
- figma-use: **MANDATORY prerequisite** — you MUST invoke this skill BEFORE every `use_figma` tool call. NEVER call `use_figma` directly without loading this skill first. Skipping it causes common, hard-to-debug failures. Trigger whenever the user wants to perform a write action or a unique read action that requires JavaScript execution in the Figma file context — e.g. create/edit/delete nodes, set up variables or tokens, build components and variants, modify auto-layout or fills, bind variables to properties, or inspect file structure programmatically. (file: r0/figma-use/SKILL.md)
- figures-diagram: Use when creating flowcharts, architecture diagrams, or conceptual diagrams - generates prompts for image AI (file: r0/figures-diagram/SKILL.md)
- figures-python: Use when creating data visualizations for papers - generates publication-quality plots with top-journal color schemes (file: r0/figures-python/SKILL.md)
- gh-address-comments: Help address review/issue comments on the open GitHub PR for the current branch using gh CLI; verify gh auth first and prompt the user to authenticate if not logged in. (file: r0/gh-address-comments/SKILL.md)
- gh-fix-ci: Use when a user asks to debug or fix failing GitHub PR checks that run in GitHub Actions; use `gh` to inspect checks and logs, summarize failure context, draft a fix plan, and implement only after explicit approval. Treat external providers (for example Buildkite) as out of scope and report only the details URL. (file: r0/gh-fix-ci/SKILL.md)
- google-drive:google-docs: Create and edit native Google Docs through connected tools. (file: r3/google-docs/SKILL.md)
- google-drive:google-drive: Use connected Google Drive as the single entrypoint for Drive, Docs, Sheets, and Slides work. Use when the user wants to find, fetch, organize, share, export, copy, or delete Drive files, or summarize and edit Google Docs, Google Sheets, and Google Slides through one unified Google Drive plugin. (file: r3/google-drive/SKILL.md)
- google-drive:google-drive-comments: Write, reply to, and resolve Google Drive comments on Docs, Sheets, Slides, and Drive files with evidence-backed location context. Use when the user asks to leave comments, review a file with comments, respond to comment threads, or resolve Drive comments. (file: r3/google-drive-comments/SKILL.md)
- google-drive:google-sheets: Analyze and edit connected Google Sheets with range precision. Use when the user wants to create Google Sheets, find a spreadsheet, inspect tabs or ranges, search rows, plan formulas, create or repair charts, clean or restructure tables, write concise summaries, or make explicit cell-range updates. (file: r3/google-sheets/SKILL.md)
- google-drive:google-slides: Route Google Slides authoring requests and derive a design system from a native template or reference deck. Use this skill when the user provides an existing native Google Slides deck as a template, reference, or prior-period source, or asks to edit, update, repair, restyle, or clean up an existing native Google Slides deck. Use the Presentations skill instead for net-new presentation creation when no existing native Google Slides deck must be followed. (file: r3/google-slides/SKILL.md)
- guizang-social-card-skill: Generate Guizang-style social card image sets and WeChat official account cover pairs from articles, scripts, screenshots, product notes, subtitles, or photos. Use when the user asks for 小红书图文, Rednote/Xiaohongshu images, social cards, carousel images, 3:4 covers, 微信公众号封面, WeChat 21:9 + 1:1 covers, Swiss Style, or magazine-style social images. (file: r0/guizang-social-card-skill/SKILL.md)
- jupyter-notebook: Use when the user asks to create, scaffold, or edit Jupyter notebooks (`.ipynb`) for experiments, explorations, or tutorials; prefer the bundled templates and run the helper script `new_notebook.py` to generate a clean starting notebook. (file: r0/jupyter-notebook/SKILL.md)
- latex-output: Use when user requests LaTeX format output or has provided school/journal LaTeX templates (file: r0/latex-output/SKILL.md)
- linear: Manage issues, projects & team workflows in Linear. Use when the user wants to read, create or updates tickets in Linear. (file: r0/linear/SKILL.md)
- literature-review: Use when writing literature review sections - guides searching, organizing, and synthesizing academic sources (file: r0/literature-review/SKILL.md)
- migrate-to-codex: Migrate supported instruction files, skills, agents, and MCP config into Codex project and global files. (file: r0/migrate-to-codex/SKILL.md)
- nature-citation: Add strict Nature/CNS citations to manuscript text by splitting long passages into citable segments, searching only accepted flagship and subjournal titles from Nature Portfolio, the AAAS Science family, and Cell Press, filtering by publication time range, and exporting one reference-manager-ready output by default. Use this skill whenever the user asks to input text and automatically get references, add citations to a paragraph/manuscript, find Nature-series or CNS support for statements, create text-to-reference correspondence, "分段引用", "自动给出引用", "Nature系列引用", "CNS及子刊", "支撑文献", "补引用", "找引用", or export EndNote/RIS/ENW/Zotero RDF. (file: r0/nature-citation/SKILL.md)
- nature-data: Prepare, audit, or revise Nature-ready Data Availability statements, data repository plans, dataset citations, and FAIR metadata checklists for manuscripts. Use when the user asks about Nature data availability, research data sharing, repository selection, accession numbers, restricted or sensitive data, source data, supplementary datasets, DataCite-style dataset references, FAIR metadata for academic publication, or Chinese-to-English data availability wording for Chinese-speaking authors preparing Nature-family submissions. (file: r0/nature-data/SKILL.md)
- nature-figure: Submission-grade Nature/high-impact journal figure workflow for Python or R. Use whenever the user asks to create, revise, audit, or polish manuscript figures, multi-panel scientific plots, or journal-ready SVG/PDF/TIFF outputs, especially for Nature-family or other high-impact journals. Before plotting, define the figure's conclusion, evidence logic, export needs, and review risks. If the user has not chosen Python or R, ask "Python or R?" and stop. Use only the selected backend for figure generation, previewing, exporting, and QA. Supports matplotlib/seaborn and ggplot2/patchwork/ComplexHeatmap. Not for dashboards or Illustrator/Figma-first infographics. (file: r0/nature-figure/SKILL.md)
- nature-paper2ppt: Build a complete but efficient Nature-style Chinese PPTX presentation from a scientific paper, preprint, PDF, article text, abstract, figure legends, or reading notes. Use this skill whenever the user asks to make slides/PPT/PPTX for journal club, group meeting, paper sharing, thesis seminar, lab meeting, department report, or academic presentation from a research paper, not only medical papers. It identifies the paper type and argument, selects only the figures needed for the story, writes Chinese slide content and speaker notes, creates the actual .pptx deck, and performs lightweight verification with cross-platform Python tooling by default. (file: r0/nature-paper2ppt/SKILL.md)
- nature-polishing: Polish, restructure, or translate academic prose into Nature-leaning English using the paper-architecture and writing-strategy principles from Scientific English Writing & Communication, with phrase-level support from Academic Phrasebank. Use whenever the user asks to polish a manuscript paragraph, abstract, introduction, results, discussion, conclusion, title, methods section, or Chinese academic draft for publication-quality English. (file: r0/nature-polishing/SKILL.md)
- nature-reader: Build full-text bilingual, figure-aware, source-grounded Markdown reading files for journal or conference papers from PDF, DOI, arXiv, publisher HTML, or pasted text. Use whenever the user asks to translate an entire paper, make a complete markdown reader, preserve figure or table placement near the relevant prose, or keep exact source anchors for every block. Do not use this for summaries, bullet-keyword notes, or citation-only tasks. (file: r0/nature-reader/SKILL.md)
- nature-response: Draft, audit, or revise point-by-point reviewer response letters for Nature-family manuscript revisions. Use when the user provides reviewer comments, editor decision letters, revision notes, response drafts, or asks how to respond to major/minor revision requests, rebuttal letters, response to reviewers, peer-review reports, 审稿意见回复, 逐点回复, 修回信, 大修回复, 小修回复, or 如何回复 reviewer. (file: r0/nature-response/SKILL.md)
- netlify-deploy: Deploy web projects to Netlify using the Netlify CLI (`npx netlify`). Use when the user asks to deploy, host, publish, or link a site/repo on Netlify, including preview and production deploys. (file: r0/netlify-deploy/SKILL.md)
- notion-knowledge-capture: Capture conversations and decisions into structured Notion pages; use when turning chats/notes into wiki entries, how-tos, decisions, or FAQs with proper linking. (file: r0/notion-knowledge-capture/SKILL.md)
- notion-meeting-intelligence: Prepare meeting materials with Notion context and Codex research; use when gathering context, drafting agendas/pre-reads, and tailoring materials to attendees. (file: r0/notion-meeting-intelligence/SKILL.md)
- notion-research-documentation: Research across Notion and synthesize into structured documentation; use when gathering info from multiple Notion sources to produce briefs, comparisons, or reports with citations. (file: r0/notion-research-documentation/SKILL.md)
- notion-spec-to-implementation: Turn Notion specs into implementation plans, tasks, and progress tracking; use when implementing PRDs/feature specs and creating Notion plans + tasks from them. (file: r0/notion-spec-to-implementation/SKILL.md)
- paper-orchestration: Use when a research-writing task spans multiple sections, medium-sized revisions, full-paper drafting, or repeated quality failures (file: r0/paper-orchestration/SKILL.md)
- pdf: Use when tasks involve reading, creating, or reviewing PDF files where rendering and layout matter; prefer visual checks by rendering pages (Poppler) and use Python tools such as `reportlab`, `pdfplumber`, and `pypdf` for generation and extraction. (file: r0/pdf/SKILL.md)
- pdf:pdf: Read, create, inspect, render, and verify PDF files where visual layout matters, including fillable AcroForms. Use Poppler rendering plus Python tools such as reportlab, pdfplumber, and pypdf for generation and extraction. (file: r7/pdf/26.1015.12040/skills/pdf/SKILL.md)
- peer-review: Use before submission or when reviewing papers - provides evaluation checklists, bias detection, and self-review templates (file: r0/peer-review/SKILL.md)
- playwright: Use when the task requires automating a real browser from the terminal (navigation, form filling, snapshots, screenshots, data extraction, UI-flow debugging) via `playwright-cli` or the bundled wrapper script. (file: r0/playwright/SKILL.md)
- playwright-interactive: Persistent browser and Electron interaction through `js_repl` for fast iterative UI debugging. (file: r0/playwright-interactive/SKILL.md)
- plugin-management:plugin-management: Discover and suggest relevant plugins, inspect app permissions and dependencies, and manage plugin connections or removal. Use when the user asks about plugins or when a task would materially benefit from an external app, account, service, or data source that available tools cannot access. (file: r4/plugin-management/0.1.0/skills/plugin-management/SKILL.md)
- presentations:Presentations: Read, create or edit PowerPoint or Google Slides decks. Use for presentation, slide deck, PowerPoint, PPT, PPTX, or Google Slides requests. (file: r7/presentations/26.1015.12040/skills/presentations/SKILL.md)
- prompts-collection: Use for translation, polishing, or de-AI-ification of academic text - provides ready-to-use prompt templates (file: r0/prompts-collection/SKILL.md)
- render-deploy: Deploy applications to Render by analyzing codebases, generating render.yaml Blueprints, and providing Dashboard deeplinks. Use when the user wants to deploy, host, publish, or set up their application on Render's cloud platform. (file: r0/render-deploy/SKILL.md)
- research-writing-assistant:brainstorming-research: Use before writing any paper - clarifies paper type, discipline, topic, methodology, and chapter structure through natural dialogue (file: r0/research-writing-assistant/skills/brainstorming-research/SKILL.md)
- research-writing-assistant:environment-setup: Use when Python environment setup is needed for data visualization or conda installation is required (file: r0/research-writing-assistant/skills/environment-setup/SKILL.md)
- research-writing-assistant:evidence-driven-writing: Use when writing or revising Introduction, Related Work, background, literature synthesis, or any section where references must drive claims (file: r0/research-writing-assistant/skills/evidence-driven-writing/SKILL.md)
- research-writing-assistant:experiment-results-planning: Use when designing experiments, result tables, mock planning data, evaluation protocols, or results sections before real data are final (file: r0/research-writing-assistant/skills/experiment-results-planning/SKILL.md)
- research-writing-assistant:figures-diagram: Use when creating flowcharts, architecture diagrams, or conceptual diagrams - generates prompts for image AI (file: r0/research-writing-assistant/skills/figures-diagram/SKILL.md)
- research-writing-assistant:figures-python: Use when creating data visualizations for papers - generates publication-quality plots with top-journal color schemes (file: r0/research-writing-assistant/skills/figures-python/SKILL.md)
- research-writing-assistant:latex-output: Use when user requests LaTeX format output or has provided school/journal LaTeX templates (file: r0/research-writing-assistant/skills/latex-output/SKILL.md)
- research-writing-assistant:literature-review: Use when writing literature review sections - guides searching, organizing, and synthesizing academic sources (file: r0/research-writing-assistant/skills/literature-review/SKILL.md)
- research-writing-assistant:paper-orchestration: Use when a research-writing task spans multiple sections, medium-sized revisions, full-paper drafting, or repeated quality failures (file: r0/research-writing-assistant/skills/paper-orchestration/SKILL.md)
- research-writing-assistant:peer-review: Use before submission or when reviewing papers - provides evaluation checklists, bias detection, and self-review templates (file: r0/research-writing-assistant/skills/peer-review/SKILL.md)
- research-writing-assistant:prompts-collection: Use for translation, polishing, or de-AI-ification of academic text - provides ready-to-use prompt templates (file: r0/research-writing-assistant/skills/prompts-collection/SKILL.md)
- research-writing-assistant:research-writing-assistant: Use when writing academic papers, theses, or research articles - supports brainstorming, chapter writing, literature review, and LaTeX output (file: r0/research-writing-assistant/SKILL.md)
- research-writing-assistant:statistical-analysis: Use when planning or reporting statistical analysis - provides test selection, execution code, and APA format guidelines (file: r0/research-writing-assistant/skills/statistical-analysis/SKILL.md)
- research-writing-assistant:using-research-writing: Use when starting any research writing task - establishes workflow and routes to appropriate skills (file: r0/research-writing-assistant/skills/using-research-writing/SKILL.md)
- research-writing-assistant:verification: Use when about to claim work is complete, a chapter is finished, or references are verified - requires running verification commands and confirming output before making any success claims (file: r0/research-writing-assistant/skills/verification/SKILL.md)
- research-writing-assistant:writing-chapters: Use when writing paper chapters - requires completed brainstorming, writes one chapter at a time with user confirmation (file: r0/research-writing-assistant/skills/writing-chapters/SKILL.md)
- research-writing-assistant:writing-core: Use when writing or revising academic papers, especially Chinese journal manuscripts, that need natural prose, de-AI-ification, Markdown formatting, or quality checks (file: r0/research-writing-assistant/skills/writing-core/SKILL.md)
- research-writing-assistant:writing-humanities: Use when writing humanities or social science papers - provides discipline-specific writing guidance (file: r0/research-writing-assistant/skills/writing-humanities/SKILL.md)
- research-writing-assistant:writing-law: Use when writing law papers - provides legal writing conventions, citation formats, and argumentation guidance (file: r0/research-writing-assistant/skills/writing-law/SKILL.md)
- research-writing-assistant:writing-medical: Use when writing medical, biological, or clinical research papers - provides IMRaD structure and reporting guidelines (file: r0/research-writing-assistant/skills/writing-medical/SKILL.md)
- scrapling-official: Scrape web pages using Scrapling with anti-bot bypass (like Cloudflare Turnstile), stealth headless browsing, spiders framework, adaptive scraping, and JavaScript rendering. Use when asked to scrape, crawl, or extract data from websites; web_fetch fails; the site has anti-bot protections; write Python code to scrape/crawl; or write spiders. (file: r0/Scrapling-Skill/SKILL.md)
- screenshot: Use when the user explicitly asks for a desktop or system screenshot (full screen, specific app or window, or a pixel region), or when tool-specific capture capabilities are unavailable and an OS-level capture is needed. (file: r0/screenshot/SKILL.md)
- security-best-practices: Perform language and framework specific security best-practice reviews and suggest improvements. Trigger only when the user explicitly requests security best practices guidance, a security review/report, or secure-by-default coding help. Trigger only for supported languages (python, javascript/typescript, go). Do not trigger for general code review, debugging, or non-security tasks. (file: r0/security-best-practices/SKILL.md)
- security-ownership-map: Analyze git repositories to build a security ownership topology (people-to-file), compute bus factor and sensitive-code ownership, and export CSV/JSON for graph databases and visualization. Trigger only when the user explicitly wants a security-oriented ownership or bus-factor analysis grounded in git history (for example: orphaned sensitive code, security maintainers, CODEOWNERS reality checks for risk, sensitive hotspots, or ownership clusters). Do not trigger for general maintainer lists or non-security ownership questions. (file: r0/security-ownership-map/SKILL.md)
- security-threat-model: Repository-grounded threat modeling that enumerates trust boundaries, assets, attacker capabilities, abuse paths, and mitigations, and writes a concise Markdown threat model. Trigger only when the user explicitly asks to threat model a codebase or path, enumerate threats/abuse paths, or perform AppSec threat modeling. Do not trigger for general architecture summaries, code review, or non-security design work. (file: r0/security-threat-model/SKILL.md)
- sentry: Use when the user asks to inspect Sentry issues or events, summarize recent production errors, or pull basic Sentry health data via the Sentry CLI; perform read-only queries using the `sentry` command. (file: r0/sentry/SKILL.md)
- sites:sites: Use Sites when the user wants a website built for them (including a landing page, portfolio, dashboard, portal, tracker, hub, game, event registration, or tool), requests changes to a website already built with Sites, wants to publish a website with Sites, or wants to manage Sites hosting. (file: r5/sites/SKILL.md)
- sites:sites-remix: Remix a Site built with the Sites plugin into a new Site. Use when the user has identified the source Site and asks to remix it. (file: r5/sites-remix/SKILL.md)
- speech: Use when the user asks for text-to-speech narration or voiceover, accessibility reads, audio prompts, or batch speech generation via the OpenAI Audio API; run the bundled CLI (`scripts/text_to_speech.py`) with built-in voices and require `OPENAI_API_KEY` for live calls. Custom voice creation is out of scope. (file: r0/speech/SKILL.md)
- spreadsheets:Spreadsheets: Use skill when user requests to create, modify, analyze, visualize, or work with spreadsheet files (`.xlsx`, `.xls`, `.csv`, `.tsv`) or Google Sheets with formulas, formatting, charts, tables, and recalculation. Do not use for live controlling Microsoft Excel app or a live Excel session. (file: r8/spreadsheets/SKILL.md)
- spreadsheets:excel-live-control: Control an open or active Microsoft Excel workbook through the ChatGPT add-in or connected session. Use when the user tags the Microsoft Excel app in Codex or follows up on an established live Excel task. Do not use for standalone spreadsheet files or Google Sheets. (file: r8/excel-live-control/SKILL.md)
- statistical-analysis: Use when planning or reporting statistical analysis - provides test selection, execution code, and APA format guidelines (file: r0/statistical-analysis/SKILL.md)
- template-creator:template-creator: Create or update a reusable personal Codex artifact-template skill. Use when the user invokes $template-creator or asks in natural language to create a reusable template from a reference document, presentation, spreadsheet, Google Docs, Slides, or Sheets link, ImageGen or Product Design image, email, Slack message, or Site project, or explicitly asks to edit or update a passed artifact-template skill. Do not use for one-off creation from an existing template. (file: r7/template-creator/26.1015.12040/skills/template-creator/SKILL.md)
- transcribe: Transcribe audio files to text with optional diarization and known-speaker hints. Use when a user asks to transcribe speech from audio/video, extract text from recordings, or label speakers in interviews or meetings. (file: r0/transcribe/SKILL.md)
- using-research-writing: Use when starting any research writing task - establishes workflow and routes to appropriate skills (file: r0/using-research-writing/SKILL.md)
- vercel-deploy: Deploy applications and websites to Vercel. Use when the user requests deployment actions like "deploy my app", "deploy and give me the link", "push this live", or "create a preview deployment". (file: r0/vercel-deploy/SKILL.md)
- verification: Use when about to claim work is complete, a chapter is finished, or references are verified - requires running verification commands and confirming output before making any success claims (file: r0/verification/SKILL.md)
- visualize:visualize: Create visualizations and interactive tools directly in conversation. Proactively use to show how something works; explore 'what happens when', 'what changes', or 'help me understand'; compare or inspect; create simulations, maps, charts, graphs, and mockups. Use standard tools for static scientific figures. (file: r2/visualize/1.0.50/skills/visualize/SKILL.md)
- winui-app: Bootstrap, develop, and design modern WinUI 3 desktop applications with C# and the Windows App SDK using official Microsoft guidance, WinUI Gallery patterns, Windows App SDK samples, and CommunityToolkit components. Use when creating a brand new app, preparing a machine for WinUI, reviewing, refactoring, planning, troubleshooting, environment-checking, or setting up WinUI 3 XAML, controls, navigation, windowing, theming, accessibility, responsiveness, performance, deployment, or related Windows app design and development work. (file: r0/winui-app/SKILL.md)
- work-pets:create-pet: Create, repair, validate, preview, upload, or activate an animated v2 pet in ChatGPT Work mode from a character idea, brand cue, or reference image. Use for new ChatGPT Pets, custom mascots, non-pixel styles, and unattached sprite sheets requiring nine animation states plus sixteen look directions. Preserve Library artifacts and Pets MCP lifecycle behavior. Exclude real pets, standalone images, and other-app pets; clarify before invoking. (file: r6/create-pet/SKILL.md)
- work-pets:pets: List, inspect, select, download, or delete animated pets in ChatGPT Work mode. Use for an explicit pet in ChatGPT or established ChatGPT Pets context. Exclude real-world and other-app pets; clarify before invoking. (file: r6/pets/SKILL.md)
- work-pets:update-pet: Inspect, validate, preview, repair, or update a custom pet in ChatGPT Work mode, including its name, description, or sprite sheet. Use for a pet in ChatGPT or established ChatGPT Pets context. Exclude real-world and other-app pets; clarify before invoking. (file: r6/update-pet/SKILL.md)
- writing-chapters: Use when writing paper chapters - requires completed brainstorming, writes one chapter at a time with user confirmation (file: r0/writing-chapters/SKILL.md)
- writing-core: Use when writing or revising academic papers, especially Chinese journal manuscripts, that need natural prose, de-AI-ification, Markdown formatting, or quality checks (file: r0/writing-core/SKILL.md)
- writing-humanities: Use when writing humanities or social science papers - provides discipline-specific writing guidance (file: r0/writing-humanities/SKILL.md)
- writing-law: Use when writing law papers - provides legal writing conventions, citation formats, and argumentation guidance (file: r0/writing-law/SKILL.md)
- writing-medical: Use when writing medical, biological, or clinical research papers - provides IMRaD structure and reporting guidelines (file: r0/writing-medical/SKILL.md)
- yeet: Use only when the user explicitly asks to stage, commit, push, and open a GitHub pull request in one flow using the GitHub CLI (`gh`). (file: r0/yeet/SKILL.md)
</skills_instructions><permissions instructions>
Filesystem sandboxing defines which files can be read or written. `sandbox_mode` is `danger-full-access`: No filesystem sandboxing - all commands are permitted. Network access is enabled.
Approval policy is currently never. Do not provide the `sandbox_permissions` for any reason, commands will be rejected.
</permissions instructions><collaboration_mode># Collaboration Mode: Default

You are now in Default mode. Any previous instructions for other modes (e.g. Plan mode) are no longer active.

Your active mode changes only when new developer instructions with a different `<collaboration_mode>...</collaboration_mode>` change it; user requests or tool descriptions do not change mode by themselves. Known mode names are Default and Plan.

## request_user_input availability

Use the `request_user_input` tool only when it is listed in the available tools for this turn.

In Default mode, strongly prefer making reasonable assumptions and executing the user's request rather than stopping to ask questions.

Use the `request_user_input` tool only for optional questions where the answer would materially improve the quality of the work.

If `request_user_input` returns no answers, continue with best judgment instead of asking again or treating the turn as blocked.

Never use the `request_user_input` tool for permission requests or permission-related escalations.
</collaboration_mode>

---


**OpenAI Codex**

<multi_agent_role>You are `/root`, the primary agent in a team of agents collaborating to fulfill the user's goals.

At the start of your turn, you are the active agent.
You can spawn sub-agents to handle subtasks, and those sub-agents can spawn their own sub-agents.
All agents in the team, including the agents that you can assign tasks to, are equally intelligent and capable, and have access to the same set of tools.

You can use `spawn_agent` to create a new agent, `followup_task` to give an existing agent a new task and trigger a turn, and `send_message` to pass a message to a running agent without triggering a turn.
`send_message` calls may be read by a human, so ensure they are legible. Always put proper spaces between words and/or numbers.
Child agents can also spawn their own sub-agents.
You can decide how much context you want to propagate to your sub-agents with the `fork_turns` parameter.

You will receive messages in the analysis channel in the form:
```
Message Type: MESSAGE | FINAL_ANSWER
Task name: <recipient>
Sender: <author>
Payload:
<payload text>
```
They may be addressed as to=/root

Note that collaboration tools cannot be called from inside `functions.exec`. Call `spawn_agent`, `send_message`, `followup_task`, `wait_agent`, `interrupt_agent`, and `list_agents` only as direct tool calls using the recipient shown in their tool definitions, such as `to=functions.collaboration.spawn_agent`, since they are intentionally absent from the `functions.exec` `tools.*` namespace. Available tools in `functions.exec` are explicitly described with a `tools` namespace in the developer message.

All agents share the same directory. In detail:
- All agents have access to the same container and filesystem as you.
- All agents use the same current working directory.
- As a result, edits made by one agent are immediately visible to all other agents.

When calling `wait_agent`, prefer longer waits (minutes) to avoid busy polling.

There are 4 available concurrency slots, meaning that up to 4 agents can be active at once, including you.

Full-history forks (`fork_turns` omitted or `"all"`) inherit the parent model and reasoning effort and do not accept overrides. Only set `model` or `reasoning_effort` when explicitly requested by the user, applicable `AGENTS.md` instructions, or skill instructions; when doing so, set `fork_turns` to `"none"` or a positive integer string.</multi_agent_role>

---


**OpenAI Codex**

<multi_agent_mode>Any earlier instruction enabling proactive multi-agent delegation no longer applies. Do not spawn sub-agents unless the user or applicable AGENTS.md/skill instructions explicitly ask for sub-agents, delegation, or parallel agent work.</multi_agent_mode>

---


**User**

chars = sorted(list(set(text)))
vocab_size = len(chars)

stoi = {ch: i for i, ch in enumerate(chars)}
itos = {i: ch for i, ch in enumerate(chars)}

encode = lambda s: [stoi[c] for c in s]
decode = lambda ids: ''.join(itos[i] for i in ids)

data = torch.tensor(encode(text), dtype=torch.long)anogpt\gptdev.ipynb,创建一个副本。把里面的分词器改成chars = sorted(list(set(text)))
vocab_size = len(chars)

stoi = {ch: i for i, ch in enumerate(chars)}
itos = {i: ch for i, ch in enumerate(chars)}

encode = lambda s: [stoi[c] for c in s]
decode = lambda ids: ''.join(itos[i] for i in ids)

data = torch.tensor(encode(text), dtype=torch.long)这样的字符器编码，其他的不要动。e:\Projects\nanogpt\gptdev.ipynb创建一个副本，其他的不改

---


**OpenAI Codex**

我会先检查笔记本里的分词器代码，再创建副本，只替换字符编码相关部分，原文件保持不变。

---


**OpenAI Codex**

我会按 Jupyter Notebook 技能的流程做定点修改，副本命名为 `gptdev_char.ipynb`，只调整分词器相关代码。

---


**OpenAI Codex**

原笔记本还在使用 `tiktoken`，后面的一个单元格也调用了它的解码方法。我会同步改为你给出的 `encode`、`decode`，保留其余代码和已保存的输出。

---


**OpenAI Codex**

已创建副本：[gptdev_char.ipynb](E:/Projects/nanogpt/gptdev_char.ipynb)。

仅替换为你提供的字符编码，并同步修改对应解码调用；其他内容及原文件未改。编码解码验证通过，当前环境缺少 PyTorch，未运行完整笔记本。

---
