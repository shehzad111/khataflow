# Security Policy

Do not publish sensitive vulnerability details in public issues. Use GitHub's private security reporting mechanism when available.

Never commit:
- passwords
- API keys
- private tokens
- real customer financial data
- production database dumps
- private business documents

MVP financial data is stored locally in IndexedDB. Exported backup files may contain sensitive financial information and should be protected.

When cloud sync is introduced, authentication, authorization, encryption in transit, server-side validation, rate limiting, and secure backup handling must be implemented before production use.
