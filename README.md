# Awesome MCP Open [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> Model Context Protocol servers you can actually run yourself.

I kept running into the same thing: I'd find a promising MCP server, wire it up, and only then realize it was just a shell around some company's paid API. Cancel the subscription and it's a brick. Most of the big MCP lists are full of these.

So I started keeping my own list, and this is it — only servers you can actually run yourself. Open source, self-hosted, your data stays on your machine. If a tool only works by calling home to someone else's cloud, it's not here. That's the whole rule, and everything below has been checked against it by hand.

## Contents

<table>
<tr>
<td valign="top">

- [🔍 Search &amp; Web](#search-web)
- [🌐 Browser Automation](#browser-automation)
- [🗄️ Databases](#databases)
- [📊 Data &amp; Analytics](#data-analytics)
- [🛠️ Developer Tools](#developer-tools)

</td>
<td valign="top">

- [🚢 DevOps &amp; Infra](#devops-infra)
- [☁️ Cloud &amp; Deploy](#cloud-deploy)
- [💳 Payments &amp; Finance](#payments-finance)
- [🎨 Design &amp; Media](#design-media)
- [🧠 Memory](#memory)

</td>
<td valign="top">

- [📋 Productivity &amp; Tasks](#productivity-tasks)
- [💬 Communication](#communication)
- [📣 Social](#social)
- [🗺️ Maps &amp; Location](#maps-location)
- [🔒 Security](#security)

</td>
</tr>
</table>

---

### What earns a place

Three tests, all required. Miss one and it's off the list — no matter how good the tool is.

- **Self-hostable** — you run the server yourself, with no mandatory vendor endpoint in the loop.
- **Open source** — a real FOSS license; source you can audit before you hand it tool access.
- **No lock-in** — it doesn't die without a paid proprietary backend, and your data isn't stranded on someone else's servers.

**Cut on purpose:** cloud-only servers you can't run yourself, source-available-but-not-OSI projects (e.g. n8n's Sustainable Use License), and open clients that are useless without a paid API. Fine tools — just not open, so not here.

---

### Red flags

A note in $\textcolor{red}{\textsf{red}}$ marks friction you'll hit before the server earns its place — a fact you can verify on the repo page in seconds:

| flag | meaning |
|---|---|
| $\textcolor{red}{\textsf{fiddly setup}}$ | needs Docker, a database, or several services running before first use |
| $\textcolor{red}{\textsf{heavy}}$ | exposes dozens of tools, crowding your context window |

---

<a id="search-web"></a>
## 🔍 Search & Web

- **[Brave Search](https://github.com/brave/brave-search-mcp-server)** · Query Brave's Search, Summarizer, and Local APIs from an MCP server
- **[Crawl4AI](https://github.com/unclecode/crawl4ai)** · Self-hosted LLM-friendly web crawler and scraper with a built-in Docker MCP bridge exposing crawl, scrape, and markdown-extraction tools · $\textcolor{red}{\textsf{fiddly setup}}$
- **[DuckDuckGo](https://github.com/nickclyde/duckduckgo-mcp-server)** · Search DuckDuckGo and fetch/parse page content into clean text with no API key needed
- **[Fetch](https://github.com/modelcontextprotocol/servers/tree/main/src/fetch)** · Official reference MCP server that fetches a URL and converts its content to markdown for LLM consumption
- **[Meilisearch](https://github.com/meilisearch/meilisearch-mcp)** · Manage indexes, documents and settings and run searches on a self-hosted Meilisearch instance
- **[Open WebSearch](https://github.com/Aas-ee/open-webSearch)** · Multi-engine web search MCP server scraping Bing, DuckDuckGo, Brave, Startpage and more with no API keys required
- **[SearXNG](https://github.com/ihor-sokoliuk/mcp-searxng)** · Query a self-hosted or public SearXNG metasearch instance for private, ad-free web search results

<a id="browser-automation"></a>
## 🌐 Browser Automation

- **[Browser Use](https://github.com/browser-use/browser-use)** · Lets AI agents drive a locally running browser to complete multi-step web tasks, exposed as an MCP server
- **[BrowserTools](https://github.com/AgentDeskAI/browser-tools-mcp)** · Streams live browser console logs, network requests, and screenshots from a Chrome extension into an MCP-compatible IDE · $\textcolor{red}{\textsf{fiddly setup}}$
- **[Chrome DevTools](https://github.com/ChromeDevTools/chrome-devtools-mcp)** · Controls a local Chrome instance for performance tracing, network inspection, and DOM debugging via the Chrome DevTools Protocol
- **[Computer-Use Agent (CUA)](https://github.com/trycua/cua/tree/main/libs/python/mcp-server)** · Runs a full computer-use agent driving sandboxed macOS/Windows/Linux VMs for cross-OS desktop control · $\textcolor{red}{\textsf{fiddly setup}}$ · $\textcolor{red}{\textsf{heavy}}$
- **[Desktop Commander](https://github.com/wonderwhy-er/DesktopCommanderMCP)** · Gives an agent terminal control, filesystem search, and diff-based file editing on your local desktop
- **[Playwright](https://github.com/microsoft/playwright-mcp)** · Drives a real Chromium/Firefox/WebKit browser via Playwright's accessibility tree for navigation, form filling, and scraping
- **[Skyvern](https://github.com/Skyvern-AI/skyvern)** · Automate browser workflows with vision-and-LLM-driven agents instead of brittle selectors

<a id="databases"></a>
## 🗄️ Databases

- **[DBHub](https://github.com/bytebase/dbhub)** · Zero-dependency SQL gateway MCP server for Postgres, MySQL, MariaDB, SQL Server and SQLite with read-only mode and query guardrails
- **[FreePeak DB](https://github.com/FreePeak/db-mcp-server)** · Go-based multi-database MCP server supporting concurrent MySQL, PostgreSQL, SQLite, Oracle and TimescaleDB connections with schema and performance tools · $\textcolor{red}{\textsf{heavy}}$
- **[Milvus](https://github.com/zilliztech/mcp-server-milvus)** · Official MCP server exposing collection search, insert, and query tools for a self-hosted Milvus vector database · $\textcolor{red}{\textsf{fiddly setup}}$
- **[MindsDB](https://github.com/mindsdb/mindsdb)** · Query and federate data across many databases and sources through a self-hosted MCP-enabled server · $\textcolor{red}{\textsf{fiddly setup}}$
- **[MotherDuck / DuckDB](https://github.com/motherduckdb/mcp-server-motherduck)** · Runs SQL analytics over local, in-memory, or S3-hosted DuckDB files with no MotherDuck account required
- **[MySQL](https://github.com/designcomputer/mysql_mcp_server)** · Enables secure, configurable read/write SQL access to a self-hosted MySQL database
- **[Neo4j](https://github.com/neo4j-contrib/mcp-neo4j)** · Run Cypher queries and manage graph data and schema on a self-hosted Neo4j database
- **[Postgres MCP Pro](https://github.com/crystaldba/postgres-mcp)** · Runs against your own Postgres to give schema introspection, EXPLAIN-based query tuning, index advice, and configurable read/write SQL access
- **[Qdrant](https://github.com/qdrant/mcp-server-qdrant)** · Official MCP server for storing and semantically searching data in a self-hosted Qdrant vector database · $\textcolor{red}{\textsf{fiddly setup}}$
- **[Redis](https://github.com/redis/mcp-redis)** · Natural-language interface to manage, query, and inspect data in a Redis instance · $\textcolor{red}{\textsf{fiddly setup}}$
- **[Supabase](https://github.com/supabase/mcp)** · Manage Supabase projects, tables, and queries from an MCP server
- **[Toolbox for Databases](https://github.com/googleapis/mcp-toolbox)** · Connect an agent to Postgres, MySQL, Spanner, and other databases through a shared open toolbox
- **[Weaviate](https://github.com/weaviate/weaviate)** · Vector database with a native MCP endpoint you enable and self-host via a single environment variable · $\textcolor{red}{\textsf{fiddly setup}}$

<a id="data-analytics"></a>
## 📊 Data & Analytics

- **[Apache Superset](https://github.com/apache/superset/tree/master/superset/mcp_service)** · Built-in service letting AI agents query and manage dashboards, charts, and datasets on a self-hosted Superset instance · $\textcolor{red}{\textsf{fiddly setup}}$
- **[ClickHouse](https://github.com/ClickHouse/mcp-clickhouse)** · Official MCP server for running read/write SQL queries and browsing schema on a self-hosted ClickHouse cluster · $\textcolor{red}{\textsf{fiddly setup}}$
- **[dbt](https://github.com/dbt-labs/dbt-mcp)** · Official server running dbt Core CLI commands, codegen, and local lineage/manifest introspection for a dbt project
- **[Grafana](https://github.com/grafana/mcp-grafana)** · Query and manage self-hosted Grafana dashboards, datasources, alerts, and incidents via its API · $\textcolor{red}{\textsf{heavy}}$
- **[Grafana Loki](https://github.com/incu6us/loki-mcp-server)** · Discover labels and run LogQL queries against a self-hosted Grafana Loki instance
- **[OpenTelemetry (Traceloop)](https://github.com/traceloop/opentelemetry-mcp-server)** · Query and analyze OpenTelemetry traces from self-hosted Jaeger or Tempo backends for debugging and LLM observability
- **[Prometheus](https://github.com/pab1it0/prometheus-mcp-server)** · Query and analyze metrics from a self-hosted Prometheus server using PromQL

<a id="developer-tools"></a>
## 🛠️ Developer Tools

- **[ast-grep](https://github.com/ast-grep/ast-grep-mcp)** · Exposes ast-grep structural code search and codemod rewriting as MCP tools
- **[Commands](https://github.com/g0t4/mcp-server-commands)** · Run arbitrary shell commands or direct executables on the host machine via a runProcess tool
- **[DevDocs](https://github.com/cyberagiinc/DevDocs)** · Crawl and index any tech documentation site into a private, searchable MCP knowledge base · $\textcolor{red}{\textsf{fiddly setup}}$
- **[Filesystem](https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem)** · Read, write, edit, move, search, and manage files and directories on the local filesystem with configurable root access control
- **[Git](https://github.com/modelcontextprotocol/servers/tree/main/src/git)** · Official reference MCP server exposing local git operations like status, diff, commit, and log
- **[GitHub](https://github.com/github/github-mcp-server)** · Self-hosted server exposing GitHub repository, issue, PR, and code-search operations to MCP clients · $\textcolor{red}{\textsf{heavy}}$
- **[Language Server (LSP)](https://github.com/isaacphi/mcp-language-server)** · Wraps any language server to expose LSP definitions, references, rename, and diagnostics as MCP tools
- **[MarkItDown](https://github.com/microsoft/markitdown)** · Convert PDFs, Office docs, images, and more to markdown for LLM consumption
- **[OpenAPI](https://github.com/ivo-toby/mcp-openapi-server)** · Turn any local or remote OpenAPI specification into callable MCP tools, prompts, and resources
- **[Pandoc](https://github.com/vivekVells/mcp-pandoc)** · Convert documents between Markdown, HTML, PDF, DOCX, and other formats using local Pandoc · $\textcolor{red}{\textsf{fiddly setup}}$
- **[Sequential Thinking](https://github.com/modelcontextprotocol/servers/tree/main/src/sequentialthinking)** · Structures dynamic, revisable step-by-step reasoning for complex problem solving
- **[Serena](https://github.com/oraios/serena)** · Provides LSP-based semantic code retrieval and editing tools (find symbol, references, rename) across languages · $\textcolor{red}{\textsf{heavy}}$
- **[Shell Server](https://github.com/tumf/mcp-shell-server)** · Execute a whitelisted set of shell commands with stdin support through a secure argv-based MCP interface

<a id="devops-infra"></a>
## 🚢 DevOps & Infra

- **[Helm](https://github.com/zekker6/mcp-helm)** · Runs Helm CLI operations (install, upgrade, list, repo management) against a Kubernetes cluster · $\textcolor{red}{\textsf{fiddly setup}}$
- **[Kubernetes](https://github.com/containers/kubernetes-mcp-server)** · Native Go MCP server for Kubernetes and OpenShift cluster management with no external CLI dependency
- **[Kubernetes (Flux159)](https://github.com/Flux159/mcp-server-kubernetes)** · Manages Kubernetes clusters via kubectl/helm, covering pods, deployments, services, and manifests · $\textcolor{red}{\textsf{heavy}}$
- **[Terraform](https://github.com/hashicorp/terraform-mcp-server)** · Lets agents search Terraform registry providers/modules and run Terraform IaC workflows against your own infrastructure · $\textcolor{red}{\textsf{fiddly setup}}$

<a id="cloud-deploy"></a>
## ☁️ Cloud & Deploy

- **[AWS](https://github.com/awslabs/mcp)** · A collection of purpose-built MCP servers for AWS services like S3, Lambda, and CDK
- **[Cloudflare](https://github.com/cloudflare/mcp-server-cloudflare)** · Manage Cloudflare Workers, KV, R2, and DNS from an MCP server
- **[Google Cloud (gcloud)](https://github.com/googleapis/gcloud-mcp)** · Wraps the gcloud CLI so agents can inspect and manage Google Cloud resources with your own credentials · $\textcolor{red}{\textsf{fiddly setup}}$

<a id="payments-finance"></a>
## 💳 Payments & Finance

- **[Actual Budget](https://github.com/s-stefanov/actual-mcp)** · Query and manage accounts, transactions and budgets in a self-hosted Actual Budget instance via MCP
- **[CCXT (crypto exchanges)](https://github.com/lazy-dinosaur/ccxt-mcp)** · Bridge MCP clients to 100+ cryptocurrency exchanges via CCXT for market data and trading using your own exchange API keys
- **[Firefly III](https://github.com/fabianonetto/mcp-server-firefly-iii)** · Manage accounts, transactions, budgets and rules in a self-hosted Firefly III personal-finance instance through MCP · $\textcolor{red}{\textsf{fiddly setup}}$
- **[Ghostfolio](https://github.com/mhajder/ghostfolio-mcp)** · Read and manage portfolio holdings, performance and market data in a self-hosted Ghostfolio instance · $\textcolor{red}{\textsf{fiddly setup}}$
- **[Stripe Agent Toolkit](https://github.com/stripe/ai/tree/main/tools/modelcontextprotocol)** · Expose Stripe payments, invoices, subscriptions and customer operations as MCP tools against your own Stripe account

<a id="design-media"></a>
## 🎨 Design & Media

- **[Blender](https://github.com/ahujasid/blender-mcp)** · Connects an LLM to a running Blender instance for prompt-driven 3D scene creation, modeling, and scripting · $\textcolor{red}{\textsf{fiddly setup}}$
- **[Excalidraw](https://github.com/yctimlin/mcp_excalidraw)** · Gives AI agents programmatic tools to create, edit, and export diagrams on a synced Excalidraw canvas · $\textcolor{red}{\textsf{fiddly setup}}$
- **[Figma (Framelink)](https://github.com/GLips/Figma-Context-MCP)** · Fetches Figma file layout, styles, and component data as structured context for AI coding agents
- **[FreeCAD](https://github.com/neka-nat/freecad-mcp)** · Lets an LLM drive the open-source FreeCAD parametric CAD application to create and edit 3D models · $\textcolor{red}{\textsf{fiddly setup}}$
- **[ImageSorcery](https://github.com/sunriseapps/imagesorcery-mcp)** · Runs local computer-vision models to detect, crop, blur, OCR, and otherwise edit images without any cloud API
- **[Unity](https://github.com/CoplayDev/unity-mcp)** · Bridges AI assistants to the Unity Editor to manage assets, control scenes, edit scripts, and automate tasks · $\textcolor{red}{\textsf{fiddly setup}}$

<a id="memory"></a>
## 🧠 Memory

- **[Basic Memory](https://github.com/basicmachines-co/basic-memory)** · MCP server that builds a persistent, bidirectional knowledge base from local Markdown files so an AI can read and write durable memory
- **[Graphiti](https://github.com/getzep/graphiti/tree/main/mcp_server)** · Self-hosted temporal knowledge-graph memory engine for agents, running on your own Neo4j/FalkorDB instance via Docker · $\textcolor{red}{\textsf{fiddly setup}}$
- **[Joplin](https://github.com/alondmnt/joplin-mcp)** · Search, read and write notes in a Joplin instance through its local data API
- **[Knowledge Graph Memory](https://github.com/shaneholloman/mcp-knowledge-graph)** · Local-first fork of the reference memory server that stores a persistent knowledge graph in a configurable local JSONL file
- **[Logseq](https://github.com/ergut/mcp-logseq)** · Read, write and query a local Logseq knowledge graph via its Local HTTP API
- **[Memory (knowledge graph)](https://github.com/modelcontextprotocol/servers/tree/main/src/memory)** · Persistent knowledge-graph memory for an LLM backed by a local JSON file, with entities/relations/observations tools
- **[Neo4j Memory](https://github.com/neo4j-contrib/mcp-neo4j/tree/main/servers/mcp-neo4j-memory)** · Official Neo4j Labs MCP server that persists entities and relations as a knowledge graph in a self-run Neo4j database · $\textcolor{red}{\textsf{fiddly setup}}$
- **[Obsidian](https://github.com/MarkusPfundstein/mcp-obsidian)** · Read, search and edit notes in a local Obsidian vault via the Local REST API community plugin · $\textcolor{red}{\textsf{fiddly setup}}$
- **[OpenMemory](https://github.com/mem0ai/mem0/tree/main/openmemory)** · Self-hostable local memory layer with an MCP server, Postgres/Qdrant storage, and a UI for browsing stored memories across MCP clients · $\textcolor{red}{\textsf{fiddly setup}}$

<a id="productivity-tasks"></a>
## 📋 Productivity & Tasks

- **[Notion](https://github.com/makenotion/notion-mcp-server)** · Read and write Notion pages, databases, and blocks via the Notion API
- **[Plane](https://github.com/ZethicTech/plane-mcp-server)** · Manage issues, cycles and modules on a self-hosted Plane project-management instance · $\textcolor{red}{\textsf{fiddly setup}}$
- **[Taskwarrior](https://github.com/awwaiid/mcp-server-taskwarrior)** · Manage tasks in the local Taskwarrior CLI task manager
- **[Vikunja](https://github.com/democratize-technology/vikunja-mcp)** · Manage projects, tasks and labels on a self-hosted Vikunja instance · $\textcolor{red}{\textsf{fiddly setup}}$

<a id="communication"></a>
## 💬 Communication

- **[CalDAV](https://github.com/dominik1001/caldav-mcp)** · Manage CalDAV calendars and tasks (list, create, update, delete events and VTODOs) against any CalDAV server
- **[Chronos (CalDAV)](https://github.com/democratize-technology/chronos-mcp)** · Multi-account CalDAV calendar server with recurring events, tasks, journals, and bulk operations · $\textcolor{red}{\textsf{heavy}}$
- **[Discord](https://github.com/SaseQ/discord-mcp)** · MCP server that lets AI assistants send, read, and manage messages and channels on a Discord server via a bot
- **[Email (better-email)](https://github.com/n24q02m/better-email-mcp)** · Multi-account IMAP/SMTP email agent with auto-discovery, folder organization, attachments, and threaded send/reply
- **[Email (IMAP/SMTP)](https://github.com/Wh1isper/mcp-email-server)** · Read, search, organize, and send email over IMAP and SMTP for any account including self-hosted mail servers
- **[Matrix](https://github.com/mindroom-ai/matrix-mcp)** · Local-first MCP server giving MCP clients read/write access to Matrix rooms on any self-hosted homeserver · $\textcolor{red}{\textsf{fiddly setup}}$
- **[Mattermost](https://github.com/Knuckles-Team/mattermost-mcp)** · MCP server exposing Mattermost channels, messaging, users, and files as tools for self-hosted Mattermost instances · $\textcolor{red}{\textsf{fiddly setup}}$
- **[Slack](https://github.com/korotovsky/slack-mcp-server)** · Self-hosted MCP server for Slack workspaces supporting channels, DMs, group DMs, and history search without requiring bot app approval
- **[Telegram](https://github.com/chigwell/telegram-mcp)** · Telegram MCP server built on Telethon for reading chats, managing groups, and sending or modifying messages, media, and contacts · $\textcolor{red}{\textsf{fiddly setup}}$

<a id="social"></a>
## 📣 Social

- **[Bluesky](https://github.com/cyanheads/bluesky-mcp-server)** · MCP server exposing search, profile, feed, thread and trending-topic tools for the Bluesky/AT Protocol public AppView
- **[Mastodon](https://github.com/VitexSoftware/mastodon-mcp-server)** · MCP server for posting statuses, reading timelines, and managing accounts on any self-hosted Mastodon instance
- **[Postiz](https://github.com/gitroomhq/postiz-app)** · Self-hosted social media scheduler with a built-in MCP server for posting and scheduling across Mastodon, Bluesky, X, LinkedIn and 20+ other networks · $\textcolor{red}{\textsf{fiddly setup}}$

<a id="maps-location"></a>
## 🗺️ Maps & Location

- **[NWS Weather](https://github.com/cyanheads/nws-weather-mcp-server)** · Retrieves real-time US forecasts, alerts and observations from the free, no-auth National Weather Service API
- **[Open-Meteo](https://github.com/cyanheads/open-meteo-mcp-server)** · Fetches global weather forecasts, ERA5 historical climate, marine conditions, air quality and elevation from the free, key-free Open-Meteo API
- **[OpenStreetMap](https://github.com/cyanheads/openstreetmap-mcp-server)** · Geocodes, reverse-geocodes, and runs Overpass spatial queries against OpenStreetMap data over STDIO or Streamable HTTP
- **[OpenStreetMap (osmmcp)](https://github.com/NERVsystems/osmmcp)** · Provides geocoding, routing, nearby-places, neighborhood analysis and EV-charging lookups against free OpenStreetMap and OSRM data
- **[Time](https://github.com/modelcontextprotocol/servers/tree/main/src/time)** · Reference server that gets the current time and converts times between IANA timezones with no external dependency

<a id="security"></a>
## 🔒 Security

- **[Metasploit](https://github.com/rapid7/metasploit-framework)** · Built-in MCP server (msfmcpd) in the Metasploit Framework exposing module search, DB hosts/services/vulns/creds/loot for penetration testing · $\textcolor{red}{\textsf{fiddly setup}}$ · $\textcolor{red}{\textsf{heavy}}$
- **[Trivy](https://github.com/aquasecurity/trivy-mcp)** · Official Aqua Security plugin turning Trivy into an MCP server for local vulnerability, misconfiguration and secret scanning of code, containers and repos
- **[Vault](https://github.com/hashicorp/vault-mcp-server)** · Official HashiCorp MCP server exposing your self-hosted Vault instance's secrets, mounts and policies to AI clients · $\textcolor{red}{\textsf{fiddly setup}}$
- **[Wazuh](https://github.com/gbrigandi/mcp-server-wazuh)** · Rust MCP server bridging a self-hosted Wazuh SIEM/Indexer to AI clients for alert and threat-context queries · $\textcolor{red}{\textsf{fiddly setup}}$

---

*Last audited 2026-07-22 · 99 servers · open-source & self-hostable only · [Submit a server](contributing.md)*
