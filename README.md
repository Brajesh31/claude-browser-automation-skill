# Claude Browser Automation Skill

A practical skill for reliable browser automation across testing, scraping, and agent-driven interactions. It covers Playwright, Puppeteer, selector strategy, synchronization, browser contexts, and debugging patterns.

## What It Covers

- **Playwright and Puppeteer:** Choose an automation framework based on project needs, with Playwright as the default recommendation for most modern workflows.
- **Reliable selectors:** Prefer user-facing locators and stable element identification over brittle CSS or XPath selectors.
- **Synchronization:** Use Playwright's auto-wait behavior and condition-based waits instead of arbitrary timeouts.
- **Test isolation:** Use independent browser contexts and clean state for reproducible tests.
- **Web scraping:** Structure extraction workflows with appropriate delays and robust page handling.
- **Popup and navigation handling:** Register expectations before triggering new windows or page transitions.
- **Debugging:** Capture traces and inspect failures to identify flaky automation.

## Installation

Clone the repository into your Claude skills directory:

```bash
git clone https://github.com/Brajesh31/claude-browser-automation-skill.git ~/.claude/skills/browser-automation
```

Install Playwright in your project when needed:

```bash
npm install -D playwright
npx playwright install
```

## Using the Skill

Example request:

```text
Use the browser-automation skill to create a reliable Playwright flow
that logs in, navigates to a dashboard, and verifies the page content.
```

See [SKILL.md](SKILL.md) for the full patterns, anti-patterns, and troubleshooting guidance.

## Recommended Practices

Prefer role, label, text, and other user-facing locators. Avoid fixed sleeps such as `waitForTimeout`, isolate each test, configure a consistent viewport, and capture traces when tests fail. Use browser automation only on sites and accounts where you have permission.
