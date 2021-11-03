---
title: Issue Triage
description: Guidelines for triaging new issues
published: true
date: 2021-10-12T22:10:44.810Z
tags: 
editor: markdown
dateCreated: 2021-08-31T15:44:09.044Z
---

> This page is aimed at members of [the Mathesar team](/team), since only they have the access to triage issues.
{.is-info}

This guide describes how to properly triage new issues to work with Mathesar's development process.. It applies to both issues you're creating or issues that have been created by community members.

## What does it mean for an issue to be triaged?
All issues must:
- Have a standard set of labels,
- Have the appropriate fields set in our GitHub project.
- Be in a milestone.

New issues are automatically created with the `status: triage` label and are automatically added to our GitHub project.

## Who should triage issues?
Any member of [the Mathesar core or community team](/team) is encouraged to triage issues. If you're making an issue, please ensure that it is triaged as well.

## How should I triage issues?
Each step in the triage process is detailed below.

### Applying labels
All issues should have the following labels:
- One or more `work:` labels. These describe the kind of work involved in the issue (frontend, backend, documentation, design, etc.)
- One `type:` label. This describes the kind of problem that the issue is solving (bug, enhancement, etc.) This may be automatically present based on the issue template.
  - There's also a `question` label for issues that are questions and not problems.
  - `type: meta` issues collect other issues and are not meant to be worked on directly.
- One `status:` label describing the current status of the issue.  

There are also other labels you should consider applying:
- `priority` labels for issues that are either urgent or are for future consideration.
- `restricted:` labels for issues that are not open to the community.
  - All `work: design` issues should also be marked `restricted: design team` because only the design team can currently work on those.
  - Consider marking complicated issues or issues that touch the fundamental architecture of Mathesar as `restricted: maintainers`.
- `good first issue` and `help wanted` labels for issues that are particularly suitable for community contribution.
  - Ensure that `help wanted` is applied to all issues of this type, but only apply `good first issue` in addition to `help wanted` if the issue is approachable for new and inexperienced contributors.
- `affects:` labels for issues that touch technical debt, architecture, DX, or UX.
- Any other labels that apply from our [repository's configured labels](https://github.com/centerofci/mathesar/labels).

Applying the correct label should also sort the issue correctly in the Mathesar GitHub project.

### Ensure the issue is sorted correctly in the Mathesar project

The [Mathesar GitHub project](https://github.com/orgs/centerofci/projects/1) organizes our open issues. We need to ensure that the issue is in the project and the following fields are set correctly.
- Status
- Priority
- Work

This process should be fully automated based on setting the correct labels in the previous step.

> The project is only accessible to [Team](/team) members, but all relevant information (such as status, priority, and milestone) should be available on individual issues. We will make this project public as soon as GitHub supports it.
{.is-warning}

### Assigning milestones
All issues should have a milestone.

If an issue is directly associated with a feature, put it in the milestone for that feature. Otherwise, put it in a monthly improvement milestone (named like `YYYY-MD improvements`) according to priority. More urgent issues should go in this month's milestone, otherwise put it in a milestone in the next couple of months.

If you don't know what milestone to put something in, talk to Kriti.

**Do not create any new milestones.**

## I have a question
Talk to Kriti.