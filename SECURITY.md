# Security policy

## Supported version

Security fixes target the latest official release. Include the affected version or commit when reporting a problem.

## Reporting a vulnerability

Use [GitHub private vulnerability reporting](https://github.com/KSAGlory/KSA-Free-Bot/security/advisories/new). Do not disclose an unreported vulnerability in a public issue or pull request.

Include:

- The affected version or commit
- A clear description of the problem
- Minimal reproduction steps
- The potential impact
- A suggested fix, if you have one

Do not include passwords, tokens, private documents, or unrelated personal information. Use a non-confidential example whenever possible.

## Project-specific guidance

Keep the bot token in the local `.env` file and grant only the permissions documented in the README. If a token is exposed, reset it immediately in the Discord Developer Portal. Never attach a real token to a report. Review third-party code before adding it to the bot.

## Disclosure

Allow time for investigation and a fix before publishing technical details. The maintainer will coordinate disclosure through the private report.

For installation help, usage questions, and ordinary bug reports, use [GitHub Issues](https://github.com/KSAGlory/KSA-Free-Bot/issues).
