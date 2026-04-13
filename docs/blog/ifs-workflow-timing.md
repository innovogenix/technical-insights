---
layout: default
title: IFS Workflow Timing
nav_order: 4
parent: Blog
---

# Choosing the Correct Timing: After vs. Asynchronous in IFS Cloud Workflow

In IFS Cloud workflows, timing is not just a technical setting — it's an architectural decision.

## After Execution

- Runs within the same transaction context.
- The action must succeed or fail with the transaction.
- Data consistency is critical.
- You need immediate, deterministic behavior.

## Asynchronous Execution

- Decouples execution from the main transaction.
- Performance matters more than immediacy.
- The action is heavy (notifications, integrations, external calls).
- You want resilience and scalability.

## The Real Question

It's not "Which one is better?" — but where should this logic live in the transaction lifecycle?

## Pro Tip

Consider a scenario where an inbound integration creates header and line records on a window, and you want to trigger an event action-configured workflow. Assume the workflow needs to fire when a new record is added at the line level to update a custom field — and you don't want a workflow failure to break the integration. In this case, the ideal approach is Asynchronous.

If you're designing workflows in IFS Cloud, this single decision can define the reliability of your entire process landscape.
