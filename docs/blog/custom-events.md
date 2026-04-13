---
layout: default
title: Custom Events
nav_order: 3
parent: Blog
---

# Custom Events in IFS Cloud: Automate the Moments That Matter

In any business, timing is everything. A purchase order gets approved — does the right person know? A customer record changes — should a downstream process kick off? An asset status flips — does your team get notified?

In IFS Cloud, Custom Events are how you make the system respond intelligently to these moments — automatically, consistently, and without manual intervention.

## What Are Custom Events?

Events in IFS Cloud are used as triggers to call standard or configured processes based on conditions.

There are two kinds: Application Defined Events (built into IFS by default) and Custom Defined Events — the ones you create. The difference is that Application Defined Events are defined in the business logic delivered by IFS, while Custom Defined Events are configured in Solution Manager and are technically executed by database triggers.

Think of a Custom Event as a "watch" you place on a specific record or action in IFS. When something happens — a field changes, a record is created, a status is updated — the event fires, and a configured action follows automatically.

## What Can a Custom Event Actually Do?

Once an event fires, it needs to do something. That's where Event Actions come in. The same event can have several actions, and the action can be an Email, Execute Online SQL, Application Message, Task, Start Workflow, or Streams Message.

In practice, this means you can:

- Send an email to a team or individual the moment something changes
- Trigger a workflow to kick off a structured approval or escalation process
- Create a task assigned to a specific user that appears in their My Tasks page
- Fire a REST call to integrate with an external system in real time
- Execute business logic to update related records automatically

The Event Action must be enabled in order to be triggered — enabling an Event Action implicitly also enables the Event itself.

## Why Use Custom Events?

### React in Real Time, Not After the Fact

Most ERP systems capture data well. Fewer help you act on it at the right moment. Custom Events close that gap — turning IFS Cloud from a record-keeping system into a responsive, intelligent platform that keeps your teams moving.

### Automate Without Customizing the Core

Custom Events sit in the configuration layer of IFS Cloud — not the core application code. This means they are upgrade-safe, transportable between environments, and won't be overwritten when IFS releases a new version. Custom Events can be added to Application Configuration Packages, making them easy to export, import, and version-control across environments.

### No Developer Required (For Most Scenarios)

A new event can be added by selecting New Custom Event and filling the details in the New Custom Event assistant in Solution Manager — a guided, form-based interface accessible to functional consultants and system administrators alike.

## Real-World Use Cases

- **Finance:** Trigger an email notification when an invoice exceeds a threshold amount
- **Procurement:** Auto-create a task for a buyer when a supplier delivery is marked late
- **Manufacturing:** Fire a workflow when a work order moves to a specific status, initiating quality checks
- **Field Service:** Notify a service manager when a high-priority work order is created
- **HR/Admin:** Send an alert when a new customer or supplier record is added to the system

## A Word on the Future: BPA Workflows

It's worth noting that IFS is evolving how event-based automation works. Custom Events with Execute Online SQL will be deprecated in a future update — the replacement is the BPA Workflow functionality. BPA Workflows offer a more structured, visual approach to automation and are the recommended path for complex logic. Custom Events with email, task, and workflow actions remain fully supported and are the right starting point for most automation needs today.

## The Bottom Line

Custom Events transform IFS Cloud from a passive system of record into an active participant in your business processes. Whether you need a simple email alert or a multi-step automated workflow, the Events framework gives you the building blocks — no heavy development required.

If your team is still manually chasing updates, sending reminder emails, or triggering processes by hand, Custom Events are worth exploring. The system can do that work for you.