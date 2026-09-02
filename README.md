# Agent Workflow Config

Version-controlled operating limits and approval metadata for AI workflows.

## Purpose

This repository keeps consequential workflow settings reviewable in Git. Each workflow declares an owner, operating objective, credit limit, and execution controls. Changes are proposed through pull requests so policy systems and human reviewers can evaluate them before they become active.

## Current workflow

`workflows/customer-support-triage.yaml` configures an AI-assisted customer-support triage workflow. Its credit limit bounds the work it may perform during one operating window.

## Change contract

Pull requests declare the operational inputs needed for policy evaluation: business criticality, execution readiness, urgency, workflow type, approval state, requested credits, and minimum useful allocation. Those declarations are reviewed alongside the exact commit being proposed.
