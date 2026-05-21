# AI Coding QA Workflow Kit

A small public resource for indie developers, QA engineers, and small technical teams using AI coding tools.

This repo helps you review AI coding tools safely and structure a rough feature idea into a QA workflow before asking an AI assistant to write tests.

## Start Here

Free resource:

- [AI Coding Tool Safety Gate Checklist](./AI-Coding-Tool-Safety-Gate-Checklist.md)
- [Simplified Chinese checklist](./AI-Coding-Tool-Safety-Gate-Checklist.zh-CN.md)

Preview:

- [PRD to Playwright QA Starter Pack preview](./prd-to-playwright-preview.md)
- [Simplified Chinese preview](./prd-to-playwright-preview.zh-CN.md)

Status:

- The full pack is temporarily unavailable while the payment route is being updated.

## What You Can Do With This Repo

- Review whether an AI coding tool, agent workflow, MCP server, or automation repo is safe enough to test.
- Decide whether to `Use`, `Use with isolation`, `Study only`, or `Reject` a tool before it touches real project data.
- Structure a feature idea into acceptance criteria, QA risks, and a Playwright automation plan before asking AI to write test code.
- Keep production credentials, customer data, cookies, payment accounts, and sensitive files out of AI-assisted workflows.

## Why This Exists

AI coding tools can write PRDs, test cases, and Playwright specs quickly.

The problem is that speed can hide weak assumptions:

- vague product scope
- missing acceptance criteria
- brittle selectors
- unsafe test data
- over-trusting generated code
- using real credentials or production data too early

This repo focuses on the workflow before automation:

```text
rough feature idea
  -> PRD clarification
  -> acceptance criteria
  -> risk discovery
  -> test case matrix
  -> test data policy
  -> Playwright automation plan
  -> test code review
  -> release smoke checklist
```

## Free Checklist

Use the checklist before you install, run, connect, or trust:

- AI coding tools
- GitHub repos
- agent workflows
- MCP servers
- browser automation scripts
- third-party templates

The checklist is designed as a 10-minute first gate. It does not replace a security review, but it helps you avoid obvious risks before trying a tool with dummy data.

Decision labels:

- `Use`
- `Use with isolation`
- `Study only`
- `Reject`

## Full Pack

The full `PRD to Playwright QA Starter Pack` includes:

- 10 sequenced prompts
- 5 reusable templates
- 1 fictional end-to-end SaaS feature example
- English and Simplified Chinese README files

Current status: temporarily unpublished until a stable payment route is confirmed.

## Safety Boundary

Do not paste real customer data, production tokens, cookies, browser profiles, bank details, payment account credentials, or sensitive information into any AI tool.

Use dummy data, sandbox environments, and human review first.

This repo does not guarantee security, bug-free software, or production-ready automation. It is a practical starting point.

## License

Content in this public repo is shared for learning and evaluation. Do not redistribute the full pack files unless you have permission.
