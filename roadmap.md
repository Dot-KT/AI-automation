# AI and Automation: A Practical Learning Roadmap

Prepared: 28 October 2026  
Format: 26 chapters, each with written material, video material, GitHub examples, practice tasks, and completion checks.  
Estimated effort: **422 hours**, including study, rebuilding examples, debugging, and project work.

## What you will be able to build

Work toward a **Business Knowledge and Operations Assistant** for a fictional small business. It will answer questions from documents, look up orders, qualify enquiries, prepare support replies, and route work for human review. You will gradually add a web interface, an API, workflow automation, retrieval, tools, MCP, evaluation, and deployment. A voice interface is a separate extension.

You will also finish smaller projects that make useful portfolio entries: a Python utility, a database-backed API, an automation pack, a document question-answering app, and an agent with controlled tools.

The roadmap follows both supplied brochures:

| Source | Curriculum pages used | Contribution |
| --- | --- | --- |
| [AI and Automation curriculum.pdf](https://chatgpt.com/library?file_id=libfile_b8090986d2a0819196f08c8a65d48e05&account_id=personal) | PDF pages 6-11; outcomes on page 4 | Automation planning, Zapier, Make, n8n, business workflows, chatbots, agents, AI-assisted coding, and voice agents. |
| [NG_AI-DevBootcamp.pdf](https://chatgpt.com/library?file_id=libfile_a31995a57a308191a5c489af1bd66be4&account_id=personal) | PDF pages 12-14; outcomes on page 11 | AI foundations, Git, web development, Python, FastAPI, SQL, prompting, RAG, MCP, testing, Docker, AWS, CI/CD, and monitoring. |

Page numbers above count from the first PDF page. The order, practice briefs, pass criteria, and time estimates below are my proposed self-study design. They are not the bootcamps' official lesson plans or a promise of job readiness.

## How to use this roadmap

For every chapter:

1. **Read** the assigned sections and write a short explanation in your own words.
2. **Watch** the assigned lesson, pausing to reproduce important steps. A course link specifies which lessons to select; you do not need to finish the entire course.
3. **Run the GitHub example** using its README. For a workflow, import the JSON into a new draft workflow and reconnect your own test credentials.
4. **Rebuild and change it.** The practice brief deliberately asks for changes beyond the supplied example.
5. **Demonstrate the completion checks** before moving on. Save your code, workflow exports, sample inputs, outputs, and notes.

Aim for roughly 25% reading/video, 60% building/debugging, and 15% review. Revisit a previous exercise after several days and explain it without looking at the tutorial. If you already know Git, backend development, or web basics, attempt the chapter's completion checks first and study only the gaps.

### Pace and milestones

| Weekly study time | Approximate duration for 422 hours |
| --- | --- |
| 12 hours | 36 weeks, approximately 8-9 months |
| 18 hours | 24 weeks, approximately 6 months |
| 25 hours | 17 weeks, approximately 4 months |

These estimates include the selected material and exercises, not every linked course in full. Add catch-up time if Python or web development is completely new.

| Phase | Chapters | Hours | Milestone |
| --- | --- | --- | --- |
| Foundations | 01-06 | 102 | Python tools and a working web API |
| Using language models | 07 | 16 | A structured AI feature |
| Workflow automation | 08-13 | 82 | Three business workflows |
| Chat and knowledge | 14-17 | 66 | A document assistant with retrieval |
| Agents and integrations | 18-21 | 64 | Tools, MCP, orchestration, and voice |
| Quality | 22-23 | 28 | Reviewed code and repeatable evaluations |
| Delivery | 24-26 | 64 | A packaged, deployed portfolio project |

### Tools and costs

Use **Python and FastAPI** for the backend; **HTML, CSS, Bootstrap, and JavaScript** for the initial interface; **SQLite**, then PostgreSQL where needed; **n8n** as your main automation platform; and **Qdrant** for vector-search practice. Learn Zapier and Make through smaller comparison projects.

The written guides and public videos are the learning materials. Academy courses may require free registration. **Running the exercises can have separate costs:** model APIs, hosted workflows, cloud services, telephony, and some platform features. Check the current service limits before an exercise; there is no need to subscribe to every platform mentioned in the brochures.

For model exercises, choose one route:

- **Local:** use Ollama and a model that fits your computer. Model downloads and memory requirements vary; begin with a small model and a small dataset. See the [Ollama Python examples and setup](https://github.com/ollama/ollama-python).
- **Hosted:** use a supported model API with a small spending budget. For OpenAI, follow the [official developer quickstart](https://developers.openai.com/api/docs/quickstart). Pick a currently available model with the capabilities required by the exercise.
- **During development:** mock model responses and external services so you can test application logic without paying for every test run. A mock checks your software; use real model calls separately to assess AI quality.

Keep private provider credentials on the server or in the automation platform's credential store. Keep `.env` files out of Git and provide `.env.example` with placeholders. Begin with fictional customers, orders, and documents. Configure messaging exercises to create drafts or write to a test destination.

**Version rule:** follow the current repository README and lockfile when reproducing an example. Some videos use older interfaces, model names, or SDK methods. Use the linked current documentation when adapting it. Record your Python version, package versions, model identifier, and the sample's commit in your notes. In particular, the Microsoft course flags its older GitHub Models route as retired; choose one of its supported alternatives.

### Keep one learning repository

Create your own repository, for example `ai-automation-lab`. Use folders such as `chapter-02-python`, `chapter-06-api`, `workflows/n8n`, `workflows/make`, `prompts`, `evals`, and `capstone`. Keep imported example repositories separate so their dependencies do not conflict. Respect their licenses and credit the examples you adapt.

For each chapter, save a short `README.md` containing the problem, setup, source project, your changes, sample input/output, what failed, and how you verified the result. For Zapier, document the steps and Code-step scripts; for Make and n8n, also save sanitized JSON exports. Remove credentials and private information before publishing.

## Chapter index

The prerequisite column lists the main dependencies. Following the numbered order satisfies them.

| Chapter | Topic | Hours | Main prerequisites |
| --- | --- | --- | --- |
| [01](#chapter-01) | Environment, Git, and GitHub | 10 | None |
| [02](#chapter-02) | Python programming and data structures | 24 | 01 |
| [03](#chapter-03) | AI, ML, LLMs, ethics, and product thinking | 10 | 02 |
| [04](#chapter-04) | Web foundations and interactive interfaces | 20 | 01 |
| [05](#chapter-05) | HTTP APIs, JSON, and asynchronous Python | 18 | 02-03 |
| [06](#chapter-06) | FastAPI, SQL, and backend architecture | 20 | 04-05 |
| [07](#chapter-07) | Prompting, model APIs, and structured output | 16 | 03, 05-06 |
| [08](#chapter-08) | Planning and designing automations | 10 | 05-07 |
| [09](#chapter-09) | Zapier workflows | 12 | 08 |
| [10](#chapter-10) | Make scenarios | 12 | 08-09 |
| [11](#chapter-11) | n8n foundations | 12 | 08 |
| [12](#chapter-12) | n8n core nodes, data flow, and recovery | 18 | 11 |
| [13](#chapter-13) | Lead, order, and support workflows | 18 | 06-07, 12 |
| [14](#chapter-14) | Chatbots and conversational interfaces | 16 | 04, 06-07, 11 |
| [15](#chapter-15) | Embeddings and vector search | 16 | 05-07 |
| [16](#chapter-16) | RAG and long-document processing | 20 | 14-15 |
| [17](#chapter-17) | LangChain and LangGraph orchestration | 14 | 16 |
| [18](#chapter-18) | Agents, tools, memory, and approval | 20 | 13, 17 |
| [19](#chapter-19) | Multi-agent systems | 14 | 18 |
| [20](#chapter-20) | MCP clients, servers, and security | 18 | 06, 18 |
| [21](#chapter-21) | Voice agents | 12 | 14, 18 |
| [22](#chapter-22) | AI-assisted development and software tests | 12 | 06, 18 |
| [23](#chapter-23) | AI evaluation, safety, and cost | 16 | 16, 18, 22 |
| [24](#chapter-24) | Linux, Docker, and local deployment | 14 | 06, 23 |
| [25](#chapter-25) | CI/CD, AWS, and observability | 20 | 24 |
| [26](#chapter-26) | Capstone and portfolio | 30 | 01-25 |

<a id="chapter-01"></a>

## Chapter 01: Prepare your environment and learn Git

**Effort:** 10 hours. **Outcome:** a reproducible workspace and a repository you can change confidently.

### Learn

- Terminal navigation, paths, files, processes, and environment variables.
- Repositories, branches, commits, forks, pull requests, and merge conflicts.
- Python virtual environments, dependency files, editor debugging, and Markdown.

### Read

- [GitHub: Hello World](https://docs.github.com/en/get-started/using-github/hello-world) - complete the repository, branch, commit, and pull request steps.
- [Python: Virtual environments and packages](https://docs.python.org/3/tutorial/venv.html) - create an isolated environment and understand how packages belong to it.

### Watch

- [Harvard CS50 Web: Git](https://cs50.harvard.edu/web/weeks/1/) - the lecture page includes the video player and notes. Focus on branches, conflicts, and pull requests.

### GitHub example and practice

Start with [GitHub Skills: Introduction to GitHub](https://github.com/skills/introduction-to-github). This is a guided repository exercise rather than an AI application; it teaches the workflow you will use throughout the roadmap.

1. Complete the exercise in your own copy, then create your learning repository.
2. Add a Python hello-world program, `.gitignore`, setup instructions, and a dependency file.
3. Change the README on two branches, create a small conflict, and resolve it. Document what Git preserved.

### Complete when

- [ ] You can clone your repository into a fresh folder, set up its environment, and run the program from its README.
- [ ] You can explain a commit, a branch, a fork, and a pull request, and show one merged practice PR.

<a id="chapter-02"></a>

## Chapter 02: Learn Python for AI and automation

**Effort:** 24 hours. **Outcome:** a command-line utility that reads, validates, transforms, and saves data.

### Learn

- Variables, strings, numeric types, conditions, loops, functions, and imports.
- Lists, tuples, sets, dictionaries, and nested combinations of these structures.
- Files, CSV/JSON, exceptions, type hints, and small classes or data models.
- Separate reusable functions from input/output code so you can test them later.

### Read

- [The official Python tutorial](https://docs.python.org/3/tutorial/) - concentrate on sections 3-8: syntax, control flow, data structures, modules, input/output, and errors. Skim classes after these.

### Watch

- [Harvard CS50P](https://cs50.harvard.edu/python/) - select Functions/Variables, Conditionals, Loops, Exceptions, and File I/O. If you already program, use the lecture examples to identify Python-specific differences rather than watching every minute.

### GitHub example and practice

Use [Al Sweigart's small Python projects](https://github.com/asweigart/the-big-book-of-small-python-projects), starting with `bagels.py` and `calendarmaker.py`. These are complete, small programs that make control flow, functions, and file output visible.

1. Run both, explain their main functions, and change one behaviour in each.
2. Build a **Lead File Cleaner**: read a CSV of fictional enquiries, trim strings, normalize emails, reject missing fields, and remove duplicates.
3. Export valid leads to JSON and rejected rows to a separate file with reasons. Handle missing files and malformed input explicitly.

### Complete when

- [ ] Your cleaner processes 20 sample rows, including duplicates and invalid entries, without silently losing a row.
- [ ] You can explain a nested dictionary and handle an expected exception without a blanket `except` hiding the problem.

<a id="chapter-03"></a>

## Chapter 03: Understand AI, machine learning, and language models

**Effort:** 10 hours. **Outcome:** you can identify a useful AI task and describe its limitations.

### Learn

- AI, machine learning, deep learning, generative AI, and LLMs; training versus inference.
- Tokens, context windows, model inputs, generated outputs, and hallucinations.
- Choosing a rule, a model call, retrieval, or an agent for a business problem.
- Bias, privacy, appropriate data use, and how a person should check a result.

### Read

- [Microsoft: Introduction to generative AI and LLMs](https://github.com/microsoft/generative-ai-for-beginners/blob/main/01-introduction-to-genai/README.md).
- [Microsoft: Using generative AI responsibly](https://github.com/microsoft/generative-ai-for-beginners/blob/main/03-using-generative-ai-responsibly/README.md).

### Watch

- [Microsoft: Introduction to Generative AI and LLMs](https://learn.microsoft.com/en-us/shows/generative-ai-for-beginners/introduction-to-generative-ai-and-llms-generative-ai-for-beginners).

### GitHub example and practice

Run the [Ollama Python chat example](https://github.com/ollama/ollama-python/blob/main/examples/chat.py), following the [repository setup](https://github.com/ollama/ollama-python). It is a minimal executable example of inference, not model training. If a local model will not fit your computer, reproduce this small chat call using your chosen hosted provider's quickstart.

1. Ask the model to summarize a paragraph, classify an enquiry, and extract three fields.
2. Ask a question about fictional information you have not supplied, then provide the information and repeat it. Record the difference.
3. Write a one-page assistant brief: intended users, one useful task, success measure, source data, and three failure cases.

### Complete when

- [ ] You can explain why a fluent answer can be wrong and why the model cannot reliably know your private order records without access to them.
- [ ] Your brief identifies a measurable task and which decisions remain with a person.

<a id="chapter-04"></a>

## Chapter 04: Build a web interface

**Effort:** 20 hours. **Outcome:** a responsive enquiry form and a simple chat interface using mock responses.

### Learn

- Client/server architecture, URLs, browser requests, and developer tools.
- Semantic HTML, forms, CSS layouts, responsive design, and Bootstrap components.
- JavaScript variables, functions, events, DOM updates, `fetch`, and loading/error states.
- Treat user and model text as untrusted content when displaying it.

### Read

- [MDN core learning modules](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core) - select HTML, CSS layout, JavaScript fundamentals, DOM scripting, and network requests.
- [Bootstrap introduction](https://getbootstrap.com/docs/5.3/getting-started/introduction/) - then use its linked grid and form documentation as a reference.

### Watch

- [CS50 Web: HTML and CSS](https://cs50.harvard.edu/web/weeks/0/).
- [CS50 Web: JavaScript](https://cs50.harvard.edu/web/weeks/5/) - focus on events, DOM manipulation, and API requests.

### GitHub example and practice

Build [Microsoft's Terrarium project](https://github.com/microsoft/Web-Dev-For-Beginners/tree/main/3-terrarium). Study its HTML, CSS, and DOM lessons before inspecting the solution. The project demonstrates interactive browser behaviour; adapt those techniques for your assistant.

1. Add an enquiry form with name, email, and message fields, plus clear validation messages.
2. Create a chat panel with a mock response function, a loading indicator, and an error state.
3. Make both usable on a narrow screen and from the keyboard. Render messages as text instead of inserting arbitrary HTML.

### Complete when

- [ ] A user can submit the form, see validation errors, and recover from a simulated network failure.
- [ ] You can trace a button click through its handler to a DOM update without asking AI to explain every line.

<a id="chapter-05"></a>

## Chapter 05: Connect Python to HTTP APIs

**Effort:** 18 hours. **Outcome:** a reliable API client with synchronous and asynchronous versions.

### Learn

- HTTP methods, status codes, headers, query parameters, request bodies, and JSON.
- API keys, bearer tokens, and the purpose of OAuth; pagination and webhook payloads.
- Timeouts, connection failures, rate limits, and limited retries for suitable operations.
- `async`, `await`, concurrent I/O, and the difference between concurrency and CPU parallelism.

### Read

- [HTTPX quickstart](https://www.python-httpx.org/quickstart/) - requests, JSON, status codes, timeouts, and exceptions.
- [HTTPX asynchronous support](https://www.python-httpx.org/async/) - `AsyncClient`, client lifetime, and asynchronous requests.

### Watch

- [CS50P: Libraries](https://cs50.harvard.edu/python/weeks/4/) - focus on packages, APIs, and JSON. It provides the API-client foundation; use the HTTPX async guide for the concurrency extension.

### GitHub example and practice

Compare the [Ollama synchronous chat example](https://github.com/ollama/ollama-python/blob/main/examples/chat.py) and [asynchronous chat example](https://github.com/ollama/ollama-python/blob/main/examples/async-chat.py). They are small, runnable clients for the model service already introduced in Chapter 03.

1. Call an API through HTTPX directly and inspect its raw request and response instead of relying only on the SDK.
2. Build an **Enquiry Enrichment Client** that fetches mock company records for your cleaned leads and saves combined JSON. Reuse local fixtures when offline.
3. Add explicit timeouts and a concurrency limit. Simulate an invalid response, timeout, and `429` response; define when a retry is appropriate.

### Complete when

- [ ] Your client reports which records succeeded or failed and does not wait forever for an unavailable service.
- [ ] You can compare sequential and concurrent runs and explain why concurrency may help network calls but may overload a service.

<a id="chapter-06"></a>

## Chapter 06: Build a FastAPI backend with SQL

**Effort:** 20 hours. **Outcome:** a database-backed API that your form and workflows can call.

### Learn

- FastAPI routes, request/response models, validation, dependencies, and OpenAPI docs.
- SQL tables, keys, `SELECT`, `INSERT`, `UPDATE`, `DELETE`, joins, and relationships.
- SQLite for initial practice; SQLModel sessions and the path to PostgreSQL and migrations.
- Appropriate async boundaries, authentication versus authorization, and CORS configuration.

### Read

- [FastAPI tutorial](https://fastapi.tiangolo.com/tutorial/) - First Steps, Request Body, Response Model, Handling Errors, Dependencies, CORS, SQL Databases, and Testing.
- [SQLModel tutorial](https://sqlmodel.tiangolo.com/tutorial/) - create/read/update/delete rows, then connect tables.
- [FastAPI concurrency guide](https://fastapi.tiangolo.com/async/) - distinguish blocking calls from awaitable operations.

### Watch

- [Intro to FastAPI, by its creator Sebastián Ramírez](https://www.youtube.com/watch?v=YTYHgtniikw) - use current documentation for syntax that has changed since the talk.

### GitHub example and practice

Run the [official FastAPI SQL database example](https://github.com/fastapi/fastapi/blob/master/docs_src/sql_databases/tutorial002_an_py310.py). Its small API demonstrates persistence and separate data models. The [SQLModel tutorial source](https://github.com/fastapi/sqlmodel/tree/main/docs_src/tutorial) supplies additional relationship examples.

1. Adapt the example into an **Enquiries API** with create, list, detail, and status-update endpoints.
2. Store customers and enquiries in related tables; validate input and return appropriate errors.
3. Connect Chapter 04's form. Add a protected staff endpoint and verify that an ordinary user cannot access another user's records.

### Complete when

- [ ] Data survives an application restart, and your OpenAPI documentation accurately describes the endpoints.
- [ ] You can demonstrate valid input, invalid input, a missing record, and unauthorized access with reproducible requests.

<a id="chapter-07"></a>

## Chapter 07: Prompt effectively and obtain structured outputs

**Effort:** 16 hours. **Outcome:** a model-powered enquiry classifier with a validated response contract.

### Learn

- Clear tasks, context, examples, delimiters, output requirements, and prompt iteration.
- System/developer instructions versus user input; separating instructions from supplied data.
- Classification, extraction, summarization, and breaking a task into smaller stages.
- JSON Schema and Pydantic validation; schema correctness versus factual correctness.
- Handling refusals, incomplete outputs, timeouts, and unsupported model capabilities.

### Read

- [Microsoft: Prompt engineering fundamentals](https://github.com/microsoft/generative-ai-for-beginners/blob/main/04-prompt-engineering-fundamentals/README.md).
- [Microsoft: Advanced prompts](https://github.com/microsoft/generative-ai-for-beginners/blob/main/05-advanced-prompts/README.md) - focus on examples, task decomposition, and comparing results.
- [OpenAI: Structured model outputs](https://developers.openai.com/api/docs/guides/structured-outputs) - study the schema and error-handling concepts if using OpenAI. With another provider, use its supported structured-output mechanism and keep application validation.

### Watch

- [Microsoft: Prompt Engineering Fundamentals](https://learn.microsoft.com/en-us/shows/generative-ai-for-beginners/understanding-prompt-engineering-fundamentals-generative-ai-for-beginners).

### GitHub example and practice

Run [Ollama's structured-output example](https://github.com/ollama/ollama-python/blob/main/examples/structured-outputs.py). For a hosted-API alternative, study [Microsoft's text-generation application examples](https://github.com/microsoft/generative-ai-for-beginners/tree/main/06-text-generation-apps).

1. Define a response with `category`, `urgency`, `summary`, and `needs_human_review` fields.
2. Build a `/classify` endpoint around the model call. Validate the response before saving or using it.
3. Compare a vague prompt, a clear prompt, and a prompt with examples against the same 20 labelled enquiries. Save your results, including mistakes.

### Complete when

- [ ] Every response is either validated successfully or becomes an explicit handled failure; malformed output never silently reaches downstream steps.
- [ ] You can show whether your revised prompt improved classification accuracy on the fixed examples. A valid schema alone does not count as a correct classification.

<a id="chapter-08"></a>

## Chapter 08: Plan an automation project

**Effort:** 10 hours. **Outcome:** an implementable workflow specification with clear success and failure paths.

### Learn

- Triggers, actions, schedules, polling, webhooks, conditions, and data mappings.
- Choosing deterministic logic for fixed rules and model calls for suitable language tasks.
- Inputs/outputs, ownership, duplicate events, idempotency, retries, and manual review.
- Estimating time saved alongside maintenance, failure, and operating costs.

### Read

- [n8n: Understand workflows](https://docs.n8n.io/build/understand-workflows.md).
- [n8n: Flow logic](https://docs.n8n.io/build/flow-logic.md) - conditionals, merging, loops, execution order, sub-workflows, and errors.

### Watch

- [n8n Beginner Course: Introduction to Automation](https://www.youtube.com/watch?v=4BVTkqbn_tY).

### GitHub example and practice

Inspect the [official n8n tutorial workflow JSON](https://github.com/n8n-io/n8n-docs/blob/main/docs/_workflows/try-it-out/quickstart/tutorial.json). This older example uses a schedule, NASA data, an IF branch, and PostBin destinations. Use it as a concrete architecture specimen; the current written quickstart in Chapter 11 uses a different example.

1. Trace an input through each node and explain the data sent down each branch.
2. Specify **enquiry intake → validation → classification → storage → staff review** for your project. Name the fields and the owner of each step.
3. Add separate handling for a duplicate event, invalid input, a model failure, and an unavailable storage service. Define which operations may be retried safely.

### Complete when

- [ ] Another developer could implement your workflow from the specification without guessing its fields, routing rules, or expected responses.
- [ ] You can estimate monthly runs and explain how a repeated delivery will avoid creating duplicate work.

<a id="chapter-09"></a>

## Chapter 09: Automate with Zapier

**Effort:** 12 hours. **Outcome:** an enquiry workflow that connects a form or webhook to business tools.

### Learn

- Triggers, actions, filters, Paths, Formatter, Delay, and run history.
- Google Workspace connections, webhooks, and small Code by Zapier steps.
- The distinction between building a Zap and developing an app integration for Zapier.

### Read

- [Zapier's workflow quick-start guide](https://help.zapier.com/hc/en-us/articles/22234847450893-Zap-workflows-quick-start-guide) - create a Zap and understand its trigger/action model.
- [Zapier Platform example apps](https://github.com/zapier/zapier-platform/tree/main/example-apps) - use the minimal and trigger examples to see how integration code represents events and actions.

### Watch

- [Zapier Academy: Automate](https://learn.zapier.com/5f4736f9-f024-454d-9433-245c53512ee9) - the video course requires a Zapier account. Focus on reading a generated workflow, testing it, and choosing deterministic versus AI steps.

### GitHub example and practice

Use [Zapier's minimal example app](https://github.com/zapier/zapier-platform/tree/main/example-apps/minimal). Follow its README to run its tests and inspect `index.js`.

**Scope note:** this repository is an integration SDK example, not an importable finished Zap. Pair it with the editor workflow below to cover both the code and visual sides of this chapter.

1. Build a Zap that receives an enquiry, formats its fields, stores a test row in Google Sheets, and prepares an acknowledgement draft.
2. Add a condition for urgent enquiries and a delayed follow-up. Call Chapter 06's API through a webhook where your plan supports it.
3. Write a small Code step to normalize input, and document the Zap's configuration and sample run.

### Complete when

- [ ] Normal, urgent, and invalid enquiries follow the intended routes, and you can investigate a failed run.
- [ ] Your repository contains the Code-step script and enough setup detail to rebuild the Zap. If a feature is unavailable on your plan, implement that branch in n8n and record the difference.

<a id="chapter-10"></a>

## Chapter 10: Build Make scenarios

**Effort:** 12 hours. **Outcome:** an importable scenario with mapping, routing, and an external API call.

### Learn

- Scenarios, modules, bundles, mappings, scheduling, routers, and filters.
- Webhooks, HTTP integrations, iterators, aggregators, and data stores.
- Error handlers and how processing order and concurrent runs affect duplicate records.

### Read

- [Make: Webhooks](https://help.make.com/webhooks).
- [Make: Scenario blueprints](https://help.make.com/blueprints) - learn import/export and which account connections you must recreate.

### Watch

- [Make Academy: Foundation](https://academy.make.com/bundles/foundation) - select Setting Up My First Scenario and Expanding My First Scenario. Free registration may be required.
- [Make Academy: Advanced Webhooks](https://academy.make.com/courses/AdvancedC05) - select the webhook-response and error-handling lessons after the foundation work.

### GitHub example and practice

Import the community [Make webhook-to-Google-Sheets project](https://github.com/Sahilingale45/make-webhook-google-sheets). The actual blueprint is named `Add webhook data to a Google Sheet.blueprint.json` at the repository root. It supplies a small working pattern: receive a webhook and map its fields into a sheet.

1. Reconnect the webhook and sheet to your own test resources; submit fictional enquiry payloads.
2. Extend it with an API call to `/classify`, a router for urgent/normal cases, and an explicit error route.
3. Add a data-store lookup for processed event IDs, then export your sanitized blueprint. Compare this with the Zapier version using the same inputs.

### Complete when

- [ ] A fresh import can be configured from your README, and invalid data reaches a deliberate failure path.
- [ ] You can explain what the sample already implemented and which routing, storage, and error-handling features you added yourself.

<a id="chapter-11"></a>

## Chapter 11: Learn the n8n interface and workflow model

**Effort:** 12 hours. **Outcome:** your first n8n workflow, built manually and exported to Git.

### Learn

- The canvas, nodes, connections, triggers, credentials, expressions, items, and executions.
- Manual runs, test webhook URLs, published workflows, and production webhook URLs.
- Viewing input/output data, pinning sample data, and debugging one node at a time.

### Read

- [n8n: Build your first workflow](https://docs.n8n.io/build-your-first-workflow.md) - follow the current weather-report example.
- [n8n: Understand workflows](https://docs.n8n.io/build/understand-workflows.md) - follow the links for credentials and executions when needed.

### Watch

- [n8n Beginner video course](https://www.youtube.com/playlist?list=PLlET0GsrLUL59YbxstZE71WszP3pVnZfI) - select Introduction to APIs and Webhooks, What Are Nodes?, How Does n8n Handle Data?, and Core Workflow Concepts.

### GitHub example and practice

Run the [official tutorial JSON](https://github.com/n8n-io/n8n-docs/blob/main/docs/_workflows/try-it-out/quickstart/tutorial.json) examined in Chapter 08. This is the older NASA/PostBin workflow, so configure its required services or replace those calls with your own mock HTTP service and logging destination. Do not expect it to match the current weather tutorial screen-for-screen.

1. Build the current written quickstart first, then import the GitHub example into a separate draft.
2. Build a three-step workflow: webhook intake, normalize fields, and store or return the result.
3. Send sample requests from Python, inspect each node's items, and export the result. Only enable a schedule when its destinations are your test resources.

### Complete when

- [ ] You can recreate the three-step workflow without copying an exported JSON file.
- [ ] You can explain a test URL versus a production URL and identify the exact node where a deliberately broken request failed.

<a id="chapter-12"></a>

## Chapter 12: Master n8n's core nodes and failure handling

**Effort:** 18 hours. **Outcome:** workflows that transform batches, route items, and recover visibly from failures.

### Learn

Learn the ten building blocks named in the automation brochure. Current documentation labels some nodes differently:

| Brochure name | Current documentation name | Practice use |
| --- | --- | --- |
| If | IF | Route valid versus invalid input |
| Switch | Switch | Route several enquiry categories |
| Merge | Merge | Join related results by a stable ID |
| Set | Edit Fields (Set) | Rename and normalize fields |
| Split in Batches | Loop Over Items (Split in Batches) | Control batch size |
| Aggregate | Aggregate | Produce one summary from many items |
| HTTP Request | HTTP Request | Call your backend |
| Code | Code | Perform a small custom transformation |
| Wait | Wait | Pause before continuing |
| Error Trigger | Error Trigger | Start a separate error workflow |

Also learn item linking, null values, execution order, bounded retries, and when normal item processing already handles a list without an explicit loop.

### Read

- [n8n flow logic](https://docs.n8n.io/build/flow-logic.md).
- [Edit Fields](https://docs.n8n.io/integrations/builtin/core-nodes/n8n-nodes-base.set), [Loop Over Items](https://docs.n8n.io/integrations/builtin/core-nodes/n8n-nodes-base.splitinbatches), and [handling errors](https://docs.n8n.io/build/flow-logic/handle-errors-gracefully.md). Use the [core-node reference](https://docs.n8n.io/integrations/builtin/core-nodes.md) for the remaining nodes.

### Watch

- [n8n: Useful Nodes](https://www.youtube.com/watch?v=Rmi-ckbMOQE).
- [n8n: Error Handling](https://www.youtube.com/watch?v=XEUVl3bbMhI).

### GitHub example and practice

Import the [official RSS batching workflow](https://github.com/n8n-io/n8n-docs/blob/main/docs/_workflows/integrations/builtin/core-nodes/n8n-nodes-base.splitinbatches/rss-feed-example.json). It demonstrates Code, Loop Over Items, and reading multiple feeds. Your extension supplies the other building blocks.

1. Replace feed inputs with 25 fictional orders and process them in batches of five.
2. Normalize fields, route cases, call your backend, merge by order ID, and aggregate a final report. Add a wait where you simulate a rate-limited service.
3. Configure a separate Error Trigger workflow in the main workflow's settings. Cause an unattended execution to fail and confirm the error is recorded. Also handle expected per-item failures deliberately.

**Key correction to the brochure's pipeline shorthand:** Error Trigger begins an error workflow; it is not an ordinary final node appended after Aggregate. Separate branches on a canvas also do not by themselves prove simultaneous execution; check execution order.

### Complete when

- [ ] All 25 items are accounted for exactly once in success or failure output, with no mismatched IDs after merging.
- [ ] You can demonstrate every node in the table and a working error workflow, rather than just a successful manual run.

<a id="chapter-13"></a>

## Chapter 13: Build complete business workflows

**Effort:** 18 hours. **Outcome:** an automation pack for lead qualification, order processing, and support routing.

### Learn

- Divide a business process into reusable sub-workflows with explicit input/output contracts.
- Combine validation, deterministic decisions, AI extraction, API calls, and storage.
- Distinguish a retryable technical failure from a rejected business request.
- Track event IDs, processed state, and an audit trail across several services.

### Read

- [n8n: Break workflows into smaller parts](https://docs.n8n.io/build/flow-logic/break-workflows-into-smaller-parts.md).
- [n8n: Handle errors gracefully](https://docs.n8n.io/build/flow-logic/handle-errors-gracefully.md) - apply the error-workflow pattern across the pack.

### Watch

- [n8n Advanced Course: Build a Full Example](https://www.youtube.com/watch?v=wOKLEfeJLVE) - focus on assembling and debugging a workflow, using your own test services for the exercise.

### GitHub example and practice

Study the community [AI Lead Follow-Up System](https://github.com/jeremylongshore/lead-followup-system-n8n). It includes a workflow export and setup documentation for form intake, qualification, and CRM storage. Inspect imported nodes and endpoints first; reconnect them to your test resources. The original uses Tally, Airtable, and a hosted model; your own form, API, and database can replace them.

Build three small workflows using a shared validation and error-handling approach:

1. **Lead qualification:** intake, clean fields, classify the message, apply a documented score, and save a follow-up draft. Keep fixed score calculations in code.
2. **Order processing:** validate a batch, check mock stock, write accepted orders, and aggregate a status report. Replaying an event must not create a second order.
3. **Support routing:** classify a ticket into billing, technical, or general; record the destination queue and escalate uncertain cases.

### Complete when

- [ ] Each workflow has valid, invalid, duplicate, and downstream-failure examples with expected results.
- [ ] Your exported pack contains three workflows, reusable pieces, and a README explaining where AI helps and how a person can review the result.

<a id="chapter-14"></a>

## Chapter 14: Build chatbots and conversational interfaces

**Effort:** 16 hours. **Outcome:** a customer-support chat interface with isolated conversations and human handoff.

### Learn

- Rule-based conversations, model-driven chat, intent, context, session IDs, and fallback behaviour.
- A chat UI, backend endpoint, model call, message history, and business tools as separate components.
- Streaming responses, conversation limits, clear error messages, and escalation.
- The roles of n8n, Voiceflow, Chatbase, and ManyChat in a chatbot solution. Select one visual platform for implementation; use the platform comparison later in this file for the others.

### Read

- [Microsoft: Building chat applications](https://github.com/microsoft/generative-ai-for-beginners/blob/main/07-building-chat-applications/README.md).
- [n8n: Chat Trigger](https://docs.n8n.io/integrations/builtin/core-nodes/n8n-nodes-langchain.chattrigger/) - study sessions, access, and connection to an agent or chain.
- [Voiceflow documentation](https://www.voiceflow.com/docs) - use the chat-agent quickstart and handoff guides if you choose Voiceflow for your visual version.

### Watch

- [Microsoft: Building Chat Applications](https://learn.microsoft.com/en-us/shows/generative-ai-for-beginners/building-chat-applications-generative-ai-for-beginners).
- [n8n: Chat Trigger, Memory, and System/User Messages](https://www.youtube.com/watch?v=yzvLfHb0nqE) - focus on the chat interface and conversation configuration. Chapter 18 develops tool-using agents in more depth.

### GitHub example and practice

Use [Microsoft's chat-application examples](https://github.com/microsoft/generative-ai-for-beginners/tree/main/07-building-chat-applications). Select one Python example from its current README and follow that example's provider setup.

1. Connect your Chapter 04 interface to a `/chat` endpoint and keep provider credentials in the backend.
2. Supply a short fictional FAQ directly as context. Add a maximum conversation length and an explicit fallback when the FAQ does not answer the question.
3. Recreate a small version in n8n Chat Trigger or Voiceflow. Use the same FAQ and ten conversation scripts to compare behaviour.

### Complete when

- [ ] Two simultaneous users cannot see each other's message history, and a failed model call produces a usable error state.
- [ ] A user can request a person, and an unanswered question becomes a recorded support handoff with relevant context.

<a id="chapter-15"></a>

## Chapter 15: Understand embeddings and vector search

**Effort:** 16 hours. **Outcome:** a semantic search service over a small collection you understand.

### Learn

- Embeddings as numerical representations; similarity, ranking, and vector dimensions.
- Keyword versus semantic search; metadata filters and the role of hybrid search.
- Collections, document IDs, payloads, upserts, deletion, and persistence.
- Use the same compatible embedding model for indexing and queries. A similarity score is not a calibrated probability that an answer is correct.

### Read

- [Qdrant local quickstart](https://qdrant.tech/documentation/quickstart/) - create a collection, add points, query it, and filter results.
- [Qdrant semantic-search tutorial](https://qdrant.tech/documentation/tutorials-basics/search-beginners/) - relate embeddings to a small real search task.

### Watch

- [Microsoft: Building Search Apps with Vector Databases](https://learn.microsoft.com/en-us/shows/generative-ai-for-beginners/building-search-apps-vector-databases-generative-ai-for-beginners) - concentrate on embeddings, indexing, and semantic versus keyword search.

### GitHub example and practice

Run [Qdrant's semantic-search notebook](https://github.com/qdrant/examples/blob/master/semantic-search-in-5-minutes/semantic_search_in_5_minutes.ipynb). The current example uses Qdrant Cloud and cloud inference; follow the local quickstart if you prefer a local database, and replace the embedding step explicitly rather than assuming the notebook runs offline unchanged.

1. Reproduce the book-search example, then replace the books with 30 fictional product descriptions or FAQ entries.
2. Add category and source metadata; expose a `/search` endpoint that returns IDs, passages, and scores.
3. Write ten queries with expected relevant entries. Compare keyword matching with top-three vector results, including a query that has no relevant answer.

### Complete when

- [ ] You can inspect the retrieved passages before generating an answer and explain why a result was selected.
- [ ] Updating or deleting an entry changes search results as expected; you can compute retrieval recall@3 on your labelled queries.

<a id="chapter-16"></a>

## Chapter 16: Build a RAG document assistant

**Effort:** 20 hours. **Outcome:** a question-answering application grounded in a small document collection.

### Learn

- Retrieval-augmented generation: ingest, parse, chunk, embed, retrieve, assemble context, and answer.
- Document/page metadata, chunk size and overlap, duplicates, document updates, and context limits.
- Grounded answers, source citations, abstention, and document permissions.
- Long-document processing: compare direct context, retrieval, and chunk-by-chunk summarization with a final synthesis. Scanned PDFs may require OCR before useful text extraction.

### Read

- [Microsoft: RAG and vector databases](https://github.com/microsoft/generative-ai-for-beginners/blob/main/15-rag-and-vector-databases/README.md).
- [LangChain: Retrieval](https://docs.langchain.com/oss/python/deepagents/retrieval) - concentrate on the retrieval pipeline and two-step RAG; leave the more elaborate agent architectures for later chapters.

### Watch

- [LangChain: RAG from Scratch video playlist](https://www.youtube.com/playlist?list=PLfaIDFEXuae2LXbO1_PKyVJiQ23ZztA0x) - select parts 1-4 on indexing, retrieval, and generation.
- [Microsoft: RAG and Vector Databases](https://learn.microsoft.com/en-us/shows/generative-ai-for-beginners/retrieval-augmented-generation-rag-and-vector-databases-generative-ai-for-beginners) - an additional conceptual walkthrough.

### GitHub example and practice

Work through [LangChain's RAG-from-scratch notebook, parts 1-4](https://github.com/langchain-ai/rag-from-scratch/blob/main/rag_from_scratch_1_to_4.ipynb). It uses framework components to illustrate the pipeline; Chapter 17 examines those abstractions more deliberately. Use its declared setup and adapt older imports through current docs where necessary.

1. Build a **Bootcamp Brochure Assistant** over the two supplied PDFs. Preserve the filename and physical PDF page number for every passage.
2. Return an answer plus supporting passages. Ask about curriculum topics and also questions that the brochures do not answer; the latter should trigger an explicit lack-of-evidence response.
3. Compare two chunking settings on ten labelled questions. Add a summary mode for a whole brochure and document how it differs from answering one retrieved question.

### Complete when

- [ ] You can follow each answer back to a supporting page, and unknown questions do not become invented brochure claims.
- [ ] You can diagnose extraction failure, retrieval failure, and answer-generation failure separately.

<a id="chapter-17"></a>

## Chapter 17: Orchestrate model workflows with LangChain and LangGraph

**Effort:** 14 hours. **Outcome:** an explicit, inspectable workflow around your model and retrieval calls.

### Learn

- Model adapters, messages, prompt templates, parsers, retrievers, and tool interfaces.
- Compose predictable stages and validate each stage's output.
- Graph nodes, edges, state, routing, and checkpoints; distinguish graph state from a model's context.
- Understand which parts of your earlier RAG pipeline a framework replaces and which remain your responsibility.

### Read

- [LangChain overview](https://docs.langchain.com/oss/python/langchain/overview) - understand the model/tool abstraction and the relationship to LangGraph.
- [LangGraph overview](https://docs.langchain.com/oss/python/langgraph/overview) - read its simple graph example and orchestration explanation.

### Watch

- [LangChain Academy: Introduction to LangGraph](https://academy.langchain.com/courses/intro-to-langgraph) - select Module 1's Simple Graph, Chain, and Router lessons. The free video course requires registration. Save Agent and Agent with Memory for the next chapter.

### GitHub example and practice

Use [LangChain Academy, Module 1](https://github.com/langchain-ai/langchain-academy/tree/main/module-1), specifically `simple-graph.ipynb`, `chain.ipynb`, and `router.ipynb`. These executable examples align with the assigned videos.

1. Build a graph that routes a question to document retrieval, a mock order lookup, or human handoff.
2. Give every node an explicit input/output shape. Keep the SQL lookup as a normal function, not generated SQL executed without checks.
3. Add a failed-state outcome, log transitions, and compare the implementation with your earlier plain Python version.

### Complete when

- [ ] You can draw the possible routes and predict which nodes run for five example inputs.
- [ ] A reviewer can inspect intermediate state and identify whether an error arose in routing, retrieval, the model, or a tool.

<a id="chapter-18"></a>

## Chapter 18: Build agents with tools, memory, and human review

**Effort:** 20 hours. **Outcome:** a narrowly scoped assistant that can choose and use business tools.

### Learn

- An agent loop: receive a task, choose a tool, validate the call, execute it, observe the result, and stop or continue.
- Tool names, descriptions, schemas, authorization, and useful error responses.
- Conversation history, persistent memory, session isolation, and memory deletion.
- Step limits, time limits, budget limits, and approval before meaningful external changes.
- Compare no-code agent platforms such as n8n and Relevance AI with code-first orchestration. Flowise, Lindy, and Voiceflow are optional alternatives to survey.

### Read

- [LangChain quickstart](https://docs.langchain.com/oss/python/langchain/quickstart) - model setup, tools, and the agent call.
- [n8n: Integrate AI](https://docs.n8n.io/build/integrate-ai.md) - agents, chains, tools, and memory.
- [Agents from Scratch project guide](https://github.com/langchain-ai/agents-from-scratch) - read the Agent and Human-in-the-Loop sections.

### Watch

- [n8n: App Tools, Guardrails, and a Draft Assistant](https://www.youtube.com/watch?v=lkudvrC3AOU).
- [LangChain Academy](https://academy.langchain.com/courses/intro-to-langgraph) - select Module 1's Agent and Agent with Memory, then Module 3's human-feedback lessons.

### GitHub example and practice

Run [LangChain's Agents from Scratch](https://github.com/langchain-ai/agents-from-scratch), starting with `notebooks/agent.ipynb`, then `notebooks/hitl.ipynb`. The notebooks use mock email/calendar tools; the real Gmail integration is a separate later setup, so you can learn the agent loop with test data first.

For a visual counterpart, inspect [n8n's Google Sheets agent workflow](https://github.com/n8n-io/n8n-docs/blob/main/docs/_workflows/advanced-ai/examples/chat_with_google_sheets_docs_version.json).

1. Add `search_knowledge`, `get_order_status`, and `prepare_support_reply` tools backed by your earlier work.
2. Let the agent choose tools, while the application checks arguments and permissions. Make replies drafts; add a review step before any simulated final send.
3. Add separate session history, a maximum tool-call count, and an explicit exit when the tool fails or the task cannot be completed.

### Complete when

- [ ] You can inspect a trace showing the selected tool, validated arguments, result, and final answer.
- [ ] An unapproved change is blocked by application logic even when the model asks for it, and one user's state never becomes another user's memory.

<a id="chapter-19"></a>

## Chapter 19: Learn multi-agent patterns

**Effort:** 14 hours. **Outcome:** a small team of specialized agents and evidence about whether it improves your task.

### Learn

- Supervisor, handoff, parallel work, subgraphs, and map/reduce patterns.
- Give each component a narrow responsibility and only the context it needs.
- Combine outputs, preserve source attribution, handle conflicting findings, and stop repeated delegation.
- Compare a multi-agent design against a single agent or fixed workflow on quality, latency, and cost.

### Read

- [LangChain: Multi-agent systems](https://docs.langchain.com/oss/python/langchain/multi-agent) - focus on context boundaries and selecting a coordination pattern.
- [LangGraph overview](https://docs.langchain.com/oss/python/langgraph/overview) - revisit state, persistence, and explicit control flow.

### Watch

- [LangChain Academy](https://academy.langchain.com/courses/intro-to-langgraph) - select Module 4's Parallelization, Sub-graphs, Map-reduce, and Research Assistant lessons.

### GitHub example and practice

Run the [Academy Research Assistant notebook](https://github.com/langchain-ai/langchain-academy/blob/main/module-4/research-assistant.ipynb). Its accompanying [Research Assistant video lesson](https://academy.langchain.com/courses/take/intro-to-langgraph/lessons/58239974-lesson-4-research-assistant) is a direct link to the assigned project walkthrough. The original can use external search tools; begin with a fixed collection of documents to control costs and make comparisons reproducible.

1. Build a **Brochure Comparison Team** with a curriculum analyst, a project/practice analyst, and a synthesizer.
2. Require each analyst to return findings with source pages. The synthesizer must flag unsupported claims and disagreements.
3. Compare the team against one well-prompted assistant on the same five comparison questions. Record elapsed time, number of model calls, and errors.

### Complete when

- [ ] Each agent has a distinct role, a defined output schema, and a bounded number of steps.
- [ ] You can justify keeping the multi-agent version based on measured benefits, or document why a simpler version is sufficient.

<a id="chapter-20"></a>

## Chapter 20: Connect tools through Model Context Protocol

**Effort:** 18 hours. **Outcome:** an MCP server that exposes a small, permission-checked business capability.

### Learn

- Host, client, and server roles; tools, resources, and prompts.
- Capability discovery, request schemas, transport selection, and protocol/SDK compatibility.
- Local stdio versus remote HTTP operation; keep protocol messages separate from diagnostic output.
- Validate inputs, enforce permissions in the tool implementation, protect credentials, and control outbound access.

### Read

- [MCP: Build a server](https://modelcontextprotocol.io/docs/develop/build-server) - choose the Python example.
- [MCP security best practices](https://modelcontextprotocol.io/docs/tutorials/security/security_best_practices) - focus on scope minimization, token handling, local-server trust, and SSRF.
- [Microsoft: First MCP server](https://github.com/microsoft/mcp-for-beginners/blob/main/03-GettingStarted/01-first-server/README.md) - read its compatibility notes before copying transport examples.

### Watch

- [Microsoft Developer: Build Your First MCP Server](https://www.youtube.com/watch?v=sNDZO9N4m9Y). The video introduces the development workflow; use the current protocol documentation for version-specific details.

### GitHub example and practice

Run [Microsoft's Python MCP calculator sample](https://github.com/microsoft/mcp-for-beginners/tree/main/03-GettingStarted/samples/python). It includes a server, requirements, README, and tests, giving you a small example you can understand before exposing your own backend.

1. Inspect its tools using an MCP client or Inspector, then call them directly and through an AI host.
2. Build `lookup_order` and `search_faq` tools backed by your existing API. Add a resource containing a fictional support policy.
3. Add `prepare_reply` as a draft-producing action. Test unknown orders, invalid arguments, unauthenticated requests where applicable, and cross-user access.

**Compatibility note:** the official documentation and older videos can target different MCP revisions. Record the revision and SDK used by your sample. Keep an older sample isolated when reproducing it, then use current transport and security guidance for your own server.

### Complete when

- [ ] Two compatible clients can discover and call your tools, and you can explain what MCP adds to the existing HTTP API.
- [ ] Forbidden records remain inaccessible regardless of prompt wording, and the tool schema cannot grant permission the implementation has not checked.

<a id="chapter-21"></a>

## Chapter 21: Build a voice assistant

**Effort:** 12 hours. **Outcome:** a browser-tested voice support assistant connected to one controlled tool.

### Learn

- Speech recognition, model responses, speech synthesis, turn-taking, interruptions, and latency.
- Voice prompts: short responses, confirmation of important details, and one question at a time.
- Tool calls, end-of-conversation summaries, handoff, and handling transcription mistakes.
- Vapi as the main exercise platform; Retell AI and ElevenLabs as alternatives to compare.

### Read

- [Vapi introduction](https://docs.vapi.ai/quickstart/introduction) - understand the speech-to-text, model, and text-to-speech components.
- [Vapi web calls](https://docs.vapi.ai/quickstart/web) - use browser calling for initial testing.
- [Vapi phone calls](https://docs.vapi.ai/quickstart/phone) - optional extension after the browser version works; check current regional availability and charges.

### Watch

- [Vapi-hosted video: Build a Voice Assistant with n8n and Vapi](https://vapi.ai/library/create-your-own-ai-voice-assistantagent-with-n8n-vapi-in-10-mins-no-code-tutorial-for-beginners) - a community tutorial hosted in Vapi's resource collection. Follow current docs when its older UI differs.

### GitHub example and practice

Adapt [Vapi's Multi-Intent Handler example](https://github.com/VapiAI/examples/tree/main/assistants/multi_intent_handler). It supplies assistant configuration and an instruction-fetching tool for a fictional service company. Its instruction lookup is a routing example; do not assume it already implements the vector-search pipeline from Chapter 16.

1. Change the assistant to your fictional business and expose a read-only order-status tool or FAQ lookup.
2. Test short browser conversations, including interruptions, an unclear order number, an unavailable tool, and a request for a person.
3. Produce a transcript and a structured call summary that can enter your support workflow. Use a synthetic or provider-supplied voice for this exercise.

### Complete when

- [ ] The assistant repeats critical details for confirmation and recovers sensibly from a transcription error or failed tool.
- [ ] You have five recorded test outcomes and measurements of response delay and usage cost, even if no phone number is configured.

<a id="chapter-22"></a>

## Chapter 22: Develop with AI assistance and verify the code

**Effort:** 12 hours. **Outcome:** a reviewed feature implemented with AI and supported by useful tests.

### Learn

- Translate a requirement into acceptance criteria, a plan, small changes, and reviewable diffs.
- Ask an assistant to explain unfamiliar code, suggest alternatives, generate tests, and diagnose failures.
- IDE assistants and visual builders such as Bolt: understand generated code, dependency choices, and export options.
- Unit, integration, and end-to-end tests; mock external calls while separately checking real AI behaviour.

### Read

- [GitHub Copilot tutorials](https://docs.github.com/en/copilot/tutorials) - select the task-development and code-review material relevant to your editor.
- [FastAPI testing guide](https://fastapi.tiangolo.com/tutorial/testing/) - test endpoint behaviour with controlled dependencies.
- [Bolt support and building guides](https://support.bolt.new/) - optional survey of the visual-builder workflow named in the brochure.

### Watch

- [GitHub: The complete beginner's guide to Copilot](https://www.youtube.com/watch?v=SJqGYwRq0uc) - focus on the REST API, test-driven development, and code-review segments listed in the video chapters.

### GitHub example and practice

Complete [GitHub Skills: Getting Started with Copilot](https://github.com/skills/getting-started-with-github-copilot). It provides a small application and a guided development exercise. Use the same plan, edit, test, and review process in your assistant project afterward.

1. Ask AI to help add an enquiry-status filter to your API, starting from acceptance criteria you wrote yourself.
2. Write tests for the public behaviour, including invalid status values, empty results, and access restrictions. Check that at least one test fails before the corresponding fix.
3. Inspect every diff, run the tests, and explain the final implementation. Keep a brief note of one incorrect or unnecessary suggestion you rejected.

### Complete when

- [ ] The feature meets its acceptance criteria, and tests would detect a meaningful regression rather than simply repeating the implementation.
- [ ] You can maintain the generated code and describe its dependencies and failure paths without relying on the original chat.

<a id="chapter-23"></a>

## Chapter 23: Evaluate AI quality, safety, and operating cost

**Effort:** 16 hours. **Outcome:** a repeatable evaluation report for your assistant.

### Learn

- Software correctness versus model quality; offline datasets versus production monitoring.
- Classification accuracy, retrieval recall@k, answer support, citation correctness, and tool-call correctness.
- Human rubrics, code-based checks, and the limitations of model-based judging.
- Prompt injection through users or retrieved documents, data leakage, unauthorized tools, and excessive loops.
- Latency, token usage, model calls, retries, and cost per completed task.

### Read

- [LangSmith evaluation guide](https://docs.langchain.com/langsmith/evaluation) - datasets, evaluators, experiments, and human review.
- [Microsoft: Securing generative AI applications](https://github.com/microsoft/generative-ai-for-beginners/blob/main/13-securing-ai-applications/README.md).

### Watch

- [Microsoft: The Generative AI Application Lifecycle](https://learn.microsoft.com/en-us/shows/generative-ai-for-beginners/the-generative-ai-application-lifecycle-generative-ai-for-beginners).
- [Microsoft: Securing Your Generative AI Applications](https://learn.microsoft.com/en-us/shows/generative-ai-for-beginners/securing-your-generative-ai-applications-generative-ai-for-beginners).

### GitHub example and practice

Use [Agents from Scratch: Evaluation notebook](https://github.com/langchain-ai/agents-from-scratch/blob/main/notebooks/evaluation.ipynb), together with the [project's evaluation data and tests](https://github.com/langchain-ai/agents-from-scratch). It demonstrates evaluating decisions, responses, and tools. You may implement your own initial report with Python/pytest and CSV before adding a hosted tracing service.

1. Assemble 50 labelled cases: 20 answerable questions, 10 unanswerable questions, 10 adversarial inputs, and 10 tool-use/permission cases. Hold some cases back from prompt tuning.
2. Compare two prompt or retrieval configurations. Report retrieval quality separately from answer quality and review citations against actual source text.
3. Record latency, usage, errors, and unauthorized-action attempts. Add a malicious instruction inside a retrieved document and verify that it cannot authorize a protected tool.

### Complete when

- [ ] You can rerun the dataset, compare versions, and show the failures alongside aggregate scores.
- [ ] Your report has explicit pass criteria, such as all permission checks passing, plus task-specific quality targets you chose. These are learning-project targets, not universal production standards.

<a id="chapter-24"></a>

## Chapter 24: Package services with Linux and Docker

**Effort:** 14 hours. **Outcome:** your assistant's services start reproducibly from container configuration.

### Learn

- Linux paths, permissions, environment variables, ports, processes, and logs.
- Images, containers, Dockerfiles, layers, build context, and dependency installation.
- Compose services, internal networking, volumes, health checks, and persistent data.
- Keep credentials out of images; use an appropriate runtime user and separate development from deployment settings.

### Read

- [Docker: Build and share a containerized application](https://docs.docker.com/get-started/tutorials/run-an-app/).
- [FastAPI in containers](https://fastapi.tiangolo.com/deployment/docker/) - package your API and understand startup behaviour.

### Watch

- [Docker: Getting Started with Docker workshop](https://www.youtube.com/watch?v=gAGEar5HQoU) - focus on the Python example, volumes, and Compose.

### GitHub example and practice

Run [Docker's FastAPI Compose sample](https://github.com/docker/awesome-compose/tree/master/fastapi). It is a compact application with a Dockerfile and Compose file. Replace legacy `docker-compose` commands in older notes with the current `docker compose` command when using Compose v2.

For an integrated AI example, inspect [n8n's self-hosted AI starter kit](https://github.com/n8n-io/self-hosted-ai-starter-kit). It assembles n8n, Ollama, Qdrant, and PostgreSQL. Its included demo is a simple chat chain; add your own RAG and agent workflows. The kit is a starting point, not a completed production deployment.

1. Containerize your API, then add the database and vector database to Compose. Add n8n once those services work.
2. Configure volumes and service-to-service URLs; do not use `localhost` to refer to another container.
3. Restart services and verify data persistence. Test startup when a dependency is unavailable and inspect the relevant logs.

### Complete when

- [ ] A fresh setup can start the documented services and pass a health check.
- [ ] You can rebuild an image, identify a failed container, and show which data survives a restart or container replacement.

<a id="chapter-25"></a>

## Chapter 25: Add CI/CD, AWS deployment, and monitoring

**Effort:** 20 hours. **Outcome:** a repeatable deployment with meaningful logs and a rollback procedure.

### Learn

- CI stages: install dependencies, check code, run tests, build an image, and retain useful results.
- CD stages: publish an image, deploy to a test environment, verify health, and release a known version.
- AWS ECR, ECS/Fargate, IAM, networking, secrets, and CloudWatch.
- Logs, metrics, traces, correlation IDs, alerts, budgets, and resource cleanup.

### Read

- [GitHub Actions: Build and test Python](https://docs.github.com/en/actions/tutorials/build-and-test-code/python).
- [AWS: Get started with ECS](https://docs.aws.amazon.com/AmazonECS/latest/developerguide/getting-started.html) - choose the Linux/Fargate path.
- [AWS Fargate learning resources](https://aws.amazon.com/fargate/getting-started/) - use the linked observability material for logs, metrics, and traces.

### Watch

- [AWS: Amazon ECS and Fargate overview](https://www.youtube.com/watch?v=yi22xrvPnPk) - the video is linked from AWS's Fargate learning page.
- [CS50 Web: Testing and CI/CD](https://cs50.harvard.edu/web/weeks/7/) - focus on test automation and deployment pipelines; adapt its framework-specific examples to FastAPI.

### GitHub example and practice

Use the community [FastAPI on AWS ECS Fargate starter](https://github.com/gemanepa/fastapi-aws-ecs). It includes FastAPI, tests, Docker, Terraform, GitHub Actions with OIDC, and CloudWatch configuration.

**Understand its boundaries:** its sample data is in memory, and its documented omissions include authentication, TLS, a database, and private-subnet production architecture. Run the local example first. Extend the deployment for your project; avoid presenting the unchanged starter as a complete secure AI product.

1. Add CI to your own project. Run deterministic tests on PRs; make paid model evaluations a deliberately controlled job with a small dataset.
2. Deploy a small test service to ECS/Fargate, then adapt it to your assistant. Add HTTPS and authentication before exposing any private data or privileged tools.
3. Attach request IDs to API and workflow logs; record failures, response time, and model usage. Deploy a broken version in the test environment and practise restoring a previous image.

### Complete when

- [ ] A failing test blocks release, the deployed version is identifiable, and a documented rollback works.
- [ ] You can find a failed request across logs and explain current operating costs and cleanup steps. If you defer paid AWS use, label the result **deployment prepared, cloud deployment unverified**.

<a id="chapter-26"></a>

## Chapter 26: Finish the capstone and portfolio

**Effort:** 30 hours. **Outcome:** a coherent Business Knowledge and Operations Assistant with evidence that it works.

### Read

- [FastAPI deployment guide](https://fastapi.tiangolo.com/deployment/) - revisit deployment concepts, HTTPS, containers, and process management.
- [LangSmith evaluation guide](https://docs.langchain.com/langsmith/evaluation) - use its dataset/experiment approach to write your release report.

### Watch

- [Microsoft: The Generative AI Application Lifecycle](https://learn.microsoft.com/en-us/shows/generative-ai-for-beginners/the-generative-ai-application-lifecycle-generative-ai-for-beginners) - revisit the lifecycle after building; identify the evidence your project still lacks.

### GitHub example and practice

Study the [Full Stack FastAPI Template](https://github.com/fastapi/full-stack-fastapi-template), particularly its backend organization, database integration, tests, containers, and workflows. It uses React and additional tooling, so keep your existing plain JavaScript interface unless adopting React serves a specific need.

Use [n8n's AI starter kit](https://github.com/n8n-io/self-hosted-ai-starter-kit) as a second infrastructure reference. Neither reference supplies your finished capstone: combine the features you already built and make their contracts consistent.

### Required scope

1. **Web and API:** a working interface with authenticated staff access and a FastAPI backend.
2. **Knowledge:** ingest a fictional business's FAQ, product information, and policies; answer with source citations and an explicit lack-of-evidence response.
3. **Tools:** authenticated order lookup plus a support-reply draft tool. Validate arguments and enforce record access outside the model.
4. **Automation:** one n8n workflow that receives enquiries, enriches/classifies them, stores the result, and queues a draft for review. Reuse your other workflows as separate portfolio examples.
5. **MCP:** expose at least one read-only business tool through a compatible MCP server and demonstrate a client calling it.
6. **Quality and operations:** repeatable tests, the 50-case evaluation, container configuration, CI, logs, and a deployment/rollback runbook.

Keep voice and multi-agent orchestration as demonstrated extensions unless your chosen use case needs them in the main application. Their chapter exercises remain part of the complete roadmap.

### Suggested 30-hour finish

| Work | Hours |
| --- | --- |
| Define one business scenario, freeze scope, and review contracts | 3 |
| Integrate UI, API, RAG, tools, workflow, and MCP | 12 |
| Fix defects and rerun tests/evaluations | 6 |
| Verify deployment, monitoring, and rollback | 4 |
| Write documentation and record the demonstration | 5 |

### Complete when

- [ ] A new user can follow your README and run the project with test data.
- [ ] Your demo includes a grounded answer, an unanswered question, an order lookup, a proposed draft awaiting approval, and a handled service failure.
- [ ] The repository contains architecture notes, setup, placeholder configuration, example requests, evaluation results, limitations, source-project credits, and a short demo video.
- [ ] You can explain why each major component exists and identify the next improvement using measured evidence.

## Brochure coverage map

Use this table to check that the combined roadmap retains both brochures' learning content.

| Brochure section | Roadmap coverage |
| --- | --- |
| TS Module 1: AI, prompting, automation types/platforms, data structures | 02-03, 07-08; relational data in 06 |
| TS Module 2: planning, best practices, workflow design, use cases | 08, 13, 23 |
| TS Module 3: Zapier, Paths, Formatter, Delay, webhooks, code, Google Workspace | 09 |
| TS Module 4: Make modules, mapping, routers, filters, webhooks, data stores, APIs | 10 |
| TS Module 5: n8n setup, nodes, triggers, transformations, APIs, errors | 11-12 |
| TS Module 6: ten essential n8n nodes | 12, including name changes and error-workflow behaviour |
| TS Module 7: lead qualification, order processing, ticket routing, debugging | 12-13 |
| TS Module 8: chatbot use cases, platforms, advanced capabilities | 14, 16, 18 |
| TS Module 9: agent types/platforms, LangChain, multi-agent systems, governance | 17-20, 23 |
| TS Module 10: n8n AI, model integrations, Sheets/Airtable, multichannel work | 09-10, 13-14, 18, 21 |
| TS Module 11: AI-assisted development, IDEs, visual builders, limitations | 22 |
| TS Module 12: voice agents, Vapi, Retell AI, ElevenLabs | 21 and the platform survey below |
| GOMYCODE: AI engineering foundations, ethics, Git, web ecosystem | 01, 03-04, 23 |
| GOMYCODE: HTML, CSS, Bootstrap, JavaScript, DOM | 04 |
| GOMYCODE: Python, files, APIs, errors, FastAPI, SQL, asynchronous programming | 02, 05-07 |
| GOMYCODE: prompting, chains, structured formats, long documents, RAG, agents, MCP | 07, 15-20 |
| GOMYCODE: Zapier/n8n, AI-assisted coding, testing AI outputs | 08-13, 22-23 |
| GOMYCODE: Linux, Docker, CI/CD, AWS, logs/metrics, final assistant | 24-26 |

## Optional platform survey from the brochures

The brochures name several products that serve overlapping purposes. To understand the landscape without multiplying subscriptions, inspect the official introduction, try one small demonstration where practical, and write down when you would choose it. The main practice path above is n8n plus Python, with separate Zapier, Make, and Vapi exercises.

| Platform/material | What to inspect | Related chapter |
| --- | --- | --- |
| [Voiceflow documentation](https://www.voiceflow.com/docs) | Conversation design, knowledge sources, integrations, and handoff | 14, 18 |
| [Chatbase documentation](https://www.chatbase.co/docs) | A hosted assistant built around supplied knowledge | 14, 16 |
| [ManyChat help](https://help.manychat.com/) | Channel-specific messaging flows and integration requirements | 14, 18 |
| [Relevance AI documentation](https://relevanceai.com/docs) | Visual tools, agents, and tool access | 18-19 |
| [Flowise documentation](https://docs.flowiseai.com/) | Visual composition of AI workflows | 17-18 |
| [Lindy documentation](https://docs.lindy.ai/) | Agent triggers, actions, and approval options | 18 |
| [Bolt support](https://support.bolt.new/) | Generating, reviewing, and exporting an application | 22 |
| [Retell AI documentation](https://docs.retellai.com/) | Voice-agent setup, tools, and conversation behaviour | 21 |
| [ElevenLabs documentation](https://elevenlabs.io/docs/overview) | Speech generation and conversational agents | 21 |

For multichannel practice, reuse the same normalized enquiry schema for a web form and a chat channel, then optionally add email intake or voice summaries. Keep a channel adapter around the shared backend/workflow so the business logic stays consistent. Use Google Sheets or Airtable for a small integration exercise, and keep the SQL database as your application's durable system of record.

## Portfolio checkpoints

| After chapter | Publishable learning project | Evidence to retain |
| --- | --- | --- |
| 02 | Lead File Cleaner | Sample CSV/JSON, validation report, reproducible run |
| 07 | AI Enquiries API | API examples, schema, labelled prompt comparison |
| 13 | Business Automation Pack | Three workflow exports, failure cases, setup instructions |
| 16 | Bootcamp Brochure Assistant | Source-aware answers and retrieval comparison |
| 20 | Business Tools Agent and MCP Server | Tool traces, access checks, compatible client demonstration |
| 21 | Voice Support Prototype | Conversation scripts, transcripts, delay/usage notes |
| 26 | Business Knowledge and Operations Assistant | Demo, release evaluation, deployment and rollback notes |

Publish only data you are entitled to share. You can demonstrate the brochure assistant without redistributing the brochures in a public repository; document where authorized users supply their own files.

## Your first three study sessions

1. **Session 1:** complete the GitHub exercise, create the learning repository, and write your study goal in the README.
2. **Session 2:** run a small Python example and modify its behaviour; keep a short explanation of the changes.
3. **Session 3:** create a fictional enquiry CSV and begin the Lead File Cleaner. End with a visible input-to-output result.

After each session, record what you built, what remains confusing, and the next smallest task. Use the chapter completion checks to decide when to move on.

## Resource verification and maintenance

Resources were researched against official documentation, original course pages, and source repositories on **28 October 2026**. GitHub sample paths and representative contents were inspected. Repository examples and paid services were **not executed as part of preparing this roadmap**. Video resources were checked through publisher/course pages or indexed video metadata; playback and account-specific access can vary.

Links intentionally point to specific lessons, notebooks, projects, or documentation rather than search results. Course pages identify the lessons to select. When a link moves, start from the named publisher or repository and locate the same lesson title. Keep the learning objective and replace obsolete APIs through current documentation; record any adaptation in your chapter notes.
