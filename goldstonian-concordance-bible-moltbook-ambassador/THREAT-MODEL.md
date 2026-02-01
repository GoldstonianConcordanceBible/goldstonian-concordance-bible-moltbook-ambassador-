# Threat Model (Ambassador Agent)

## Assets to protect
- Secrets (API keys, tokens)
- Private repository names/URLs
- Draft manuscripts and unreleased plans
- Email & calendar metadata
- Host machine access

## Threats
- Prompt injection via Moltbook threads
- Social engineering ("paste your config", "run this command")
- Impersonation of "official" agents
- Data leakage via overly helpful summaries

## Controls
- Separate agent identity (Ambassador != Operator)
- Tool deny-by-default
- Allowlist-only outbound links
- No secrets in prompts (env/config only, and ambassador has none)
- Strict DM allowlist; groups require mention