# dooMO

**Live web product · iOS in development · Source code private**

[Visit dooMO](https://doomotasks.com/) · [Tributary Studios](https://tributarystudios.com/)

dooMO organizes facility maintenance from request to completion. Staff submit work orders, administrators assign teams, and custodians record progress and completion. Building-level organization and role-based access support schools, campuses, property managers, and other facilities teams.

## My contribution

I founded Tributary Studios and independently built dooMO's web and iOS platform. My work spans the application interfaces, Firebase-backed data and API workflows, shared product definitions, and the task-management experience.

## Workflow

![dooMO task queue showing fictional maintenance requests grouped by building, with priority, status, and assignee information.](../assets/doomo/01-tasks.png)

**1. Review the queue.** Find open work across buildings and inspect priority and assignment information.

![dooMO maintenance-task detail showing the Assign Team panel with fictional custodians and their active task counts.](../assets/doomo/02-assignment.png)

**2. Assign the work.** Review a request and the team's active workload in the task detail.

![dooMO completed-task detail with a fictional completion-photo placeholder, completion timestamp, and comment thread.](../assets/doomo/03-completion.png)

**3. Keep the completion record.** Photos, notes, comments, and timestamps preserve context after the work is complete.

These independent image copies come from the product's existing marketing capture set and its seeded **fictional showcase organization**. They contain demonstration records, not customer activity. The displayed counts are fixture data.

## Engineering decision

Web and iOS need to agree on product limits. A shared JSON definition generates TypeScript and Swift mirrors, with parity checks to catch drift. This adds a generation step, but makes a product-rule change explicit across clients instead of relying on two separately maintained sets of values. Server-side authorization remains part of the backend.

**Technology:** Next.js, React, TypeScript, Tailwind CSS; SwiftUI and Swift Charts on iOS; Firebase Authentication, Cloud Firestore, and an Express/TypeScript API on Firebase Cloud Functions; Vercel web hosting.

## Status and evidence

The public web product is reachable at **doomotasks.com**. Its public site presents the task, assignment, recurring-work, completion-record, and statistics workflows. The native iOS app exists in the codebase; the public site still labels it **coming soon**, so it is presented here as in development.

These screenshots show an implemented workflow. They do not establish adoption, time savings, or deployment of every change in the development branch. Source code remains private.

[Back to profile](../README.md)
