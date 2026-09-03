# Approved intake test inputs

These two request files are owner-approved test inputs, not product defaults or evidence of autonomous workload detection. Each asks for 400 credits, with a minimum useful amount of 400. The current workspace has 500 uncommitted credits and retains its existing requests and commitments.

Both have declared approval/readiness signals that satisfy the active eligibility gates. Support has criticality 5 and high urgency; research has criticality 3 and medium urgency. RuleRipple, not these files, calculates scores, rank, allocation and authorization. Declared `approved: true` is an eligibility input, not human approval of the resulting budget request.

Pushing these files to main triggers two separate GitHub Actions jobs. Each authenticates with its own scoped repository secret, submits its request through HTTPS and reads its own recorded decision. No execution binding is present. The workers do not approve, merge, call a model, consume credits or report measured usage.

Retry these unchanged files with the same submission IDs to check idempotency. Do not rename IDs to replay these same test work items. New real work needs new inputs and identifiers.
