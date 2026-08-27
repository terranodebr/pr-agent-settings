# pr-agent-settings

Org-wide global configuration for [PR-Agent](https://github.com/qodo-ai/pr-agent),
the AI code review bot used on pull requests across `terranodebr` repos.

`.pr_agent.toml` on this repo's default branch is auto-merged beneath every
repo's local config, per PR-Agent's
[global configuration file](https://docs.pr-agent.ai/usage-guide/configuration_options/#global-configuration-file)
feature. A repo-local `.pr_agent.toml` overrides these values where a repo
needs something different (e.g. `terranode-backend` overrides
`repo_context_files` to list its nested `AGENTS.md` files).

Each repo still needs its own `.github/workflows/ai-review-*.yml` (not
covered by this config — see `terranode-backend` for the reference
workflow pair) and its own `DEEPSEEK_API_KEY` secret.
