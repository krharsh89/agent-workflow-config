# Request-submission workers

Two independently credentialed transport workers submit typed budget requests to RuleRipple. They do not use an LLM, merge PRs, execute workloads, or report provider-metered usage.

## Setup

1. Create two connections in RuleRipple → Request inbox → Connect agents. Choose source, resource, per-request limits and lifetime deliberately.
2. Store each one-time credential in repository Actions secrets as RULERIPPLE_AGENT_ONE and RULERIPPLE_AGENT_TWO. Set repository variable RULERIPPLE_ORIGIN to https://ruleripple.krharsh89.chatgpt.site.
3. Save real request envelopes to .ruleripple/requests/agent-one.json and agent-two.json, each containing only a requests array. Copy the current policy template, fill actual values, omit agent (identity is server-assigned), and retain submission IDs for exact retries.
4. Run Actions → Submit agent budget requests, or change request files on main. Wait for both jobs before reviewing the full portfolio with human approval enabled.

No request files are preinstalled. The existing support PR has already merged; preserve its authorization and receipt. Fresh work needs fresh work-item identities and deliberately chosen amounts. Installing these workers does not change a policy, budget, PR or receipt. Do not run them until both credentials and request files are configured.

[RuleRipple overview](https://github.com/krharsh89/RuleRipple/blob/main/README.md) · [Security policy](https://github.com/krharsh89/RuleRipple/blob/main/SECURITY.md)
