# Agent Workflow Config

Version-controlled operating limits and approval metadata for AI workflows.

## Purpose

Each workflow declares an owner, operating objective, credit limit and execution controls. Changes are proposed through pull requests so policy systems and human reviewers can evaluate them before merge.

## Configuration

Workflow configurations live under `workflows/`. The support configuration is `workflows/customer-support-triage.json`. Its daily authorization is the numeric field `/workflow/credit_limit`.

## Change contract

Pull requests declare business criticality, execution readiness, urgency, workflow type, execution eligibility, requested credits and minimum useful allocation in a Policy intake section. For JSON budget binding, total mode authorizes the full proposed limit; increase mode authorizes only a verified numeric increase. A merge must be funded in full.

Declared execution eligibility is not the RuleRipple approval. The policy checkpoint authorizes the exact source head and amount separately.

## Execution boundary

Merging changes repository configuration. This repository does not launch an AI worker, enforce a provider account limit or measure token usage. A consuming runtime must load the approved configuration and report actual usage separately. Credits here are an internal authorization unit, not a GitHub charge.
