# AI Coding Tool Safety Gate Checklist

Version: 0.1

## What This Is

A practical checklist for indie developers, QA engineers, and small technical teams before using an AI coding tool, GitHub repo, agent workflow, MCP server, browser automation script, or third-party template in a real project.

Use it before you install, run, connect, or trust a tool.

This checklist does not guarantee security. It helps you slow down, avoid obvious mistakes, and decide whether a tool is safe enough to test with dummy data.

## Quick Verdict

Use this table before doing anything else.

| Decision | Meaning |
| --- | --- |
| Use | Low-risk enough for local testing with dummy data. |
| Use with isolation | Useful, but only inside a sandbox, temporary folder, container, VM, or throwaway account. |
| Study only | Good ideas, but do not install or connect it. |
| Reject | Do not use it for this project. |

## Hard Reject Rules

Reject the tool if any of these are true:

- It requires your bank account, payout account, payment password, real cookies, browser profile, or production token to test.
- It asks you to paste secrets into a third-party web page or unknown script.
- It has no license, or the license clearly does not allow your target use.
- It downloads unknown binaries during installation.
- It has unclear `postinstall`, shell, PowerShell, or curl-pipe-bash behavior.
- It is heavily obfuscated without a clear reason.
- It forces telemetry or data upload with no opt-out.
- It requires write access to production systems before a local trial.
- It has unresolved issues about security, data loss, credential leakage, or malicious behavior.

## Sensitive Data Rule

Never give a new tool:

- Banking passwords
- Payment platform passwords
- Payout credentials
- Two-factor authentication codes
- Browser cookies
- Real browser profiles
- Production API tokens
- Customer data
- Private medical, financial, legal, or identity data
- Real user databases

First test with:

- Dummy data
- Temporary accounts
- Local folders
- Sample repos
- Least-privilege tokens
- Read-only permissions when possible

## 10-Minute Tool Review

Before installing a tool, check:

### 1. Source

- Is the project hosted in a public repo?
- Is the maintainer identifiable?
- Does the README clearly explain what the tool does?
- Does the tool have examples, docs, or screenshots?
- Are there recent commits or releases?

### 2. License

- Is there a license file?
- Does it allow commercial use?
- Does it require attribution?
- Does it impose copyleft obligations?
- Does the license match how you plan to use the tool?

If the license is missing, treat the tool as `Study only` at most.

### 3. Installation

Look for:

- `postinstall`
- shell scripts
- PowerShell scripts
- binary downloads
- install-time network calls
- native extensions
- unpinned dependencies

If you cannot explain what installation does, do not install it on your main machine.

### 4. Runtime Permissions

Ask:

- Does it read files?
- Does it write files?
- Does it run shell commands?
- Does it open a browser?
- Does it access the clipboard?
- Does it call external APIs?
- Does it upload code, logs, screenshots, or prompts?
- Does it ask for environment variables?

More permissions mean a higher isolation requirement.

### 5. Credential Handling

Check whether the tool:

- Reads `.env`
- Logs secrets
- Sends prompts or code to external services
- Stores tokens locally
- Requires broad OAuth scopes
- Reuses your real browser profile

If credential behavior is unclear, use `Use with isolation` or `Reject`.

### 6. Maintenance

Check:

- Recent commits
- Recent releases
- Open issues
- Maintainer responses
- Breaking changes
- Security-related reports

An abandoned tool is not always unsafe, but it should not enter an automated revenue system without extra review.

## Isolation Levels

| Level | Use when |
| --- | --- |
| Local dummy test | Tool is simple, licensed, documented, and does not need credentials. |
| Temporary folder | Tool writes files or generates code. |
| Throwaway repo | Tool changes project structure or commits files. |
| Temporary account | Tool connects to GitHub, AI platforms, email, storage, or social platforms. |
| Container / VM | Tool runs scripts, installs many dependencies, downloads binaries, or has unclear behavior. |
| Reject | Tool needs payment accounts, real cookies, production tokens, or sensitive data to test. |

## Safe Trial Plan

Before using a tool in a real workflow:

1. Create a temporary folder.
2. Use a small sample repo.
3. Disable access to real secrets.
4. Use dummy input data.
5. Run only documented commands.
6. Record what files changed.
7. Check whether it made network calls.
8. Review generated output before copying it into a real project.
9. Delete the trial folder if anything looks wrong.
10. Decide: Use, Use with isolation, Study only, or Reject.

## AI Coding Agent Specific Checks

Before giving an AI coding agent a task:

- Can it read only the folder it needs?
- Can it avoid payment, banking, tax, identity, or account actions?
- Can it work with fake data?
- Can it avoid production credentials?
- Can it explain what files it changed?
- Can it run tests without changing unrelated files?
- Can you review a diff before accepting changes?

Do not allow an agent to:

- Log in to payment platforms for you
- Move money
- Withdraw funds
- Submit tax or identity verification
- Use real customer data without a clear policy
- Run unknown third-party installers without review

## Simple Scoring

Score each item from 0 to 2.

| Factor | 0 | 1 | 2 |
| --- | --- | --- | --- |
| License | Missing or incompatible | Present but needs review | Clear and usable |
| Maintenance | Abandoned or unclear | Some activity | Active enough |
| Docs | Missing | Basic | Clear examples |
| Install safety | Suspicious | Needs isolation | Simple and explainable |
| Credential safety | Unsafe | Unclear | Least privilege |
| Reproducibility | Hard to repeat | Some steps unclear | Clear setup |
| Exit path | Lock-in | Partial export | Easy to remove |

Suggested result:

- 12-14: Use
- 9-11: Use with isolation
- 6-8: Study only
- 0-5: Reject

Hard reject rules override the score.

## Final Decision Note

Use this short note before you proceed:

```text
Tool:
Purpose:
Data used for trial:
Credentials required:
Install risk:
Runtime permissions:
License:
Decision:
Reason:
Next safe step:
```

## Closing Rule

No tool enters an automated revenue system until it has passed this checklist with dummy data.

