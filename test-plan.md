# Test Plan: KanbanFlow (Web)

Author: Barbara Larrosa
Version: 1.0, October 2026

## Objective

Check that the two core flows of KanbanFlow work as a user would expect, find defects in them, and document the results so anyone can repeat them.

## Application under test

KanbanFlow (kanbanflow.com), a web-based kanban board. Tested on the free plan with my own account.

## Test basis

KanbanFlow has no public requirements document. Expected results are based on:

1. KanbanFlow's official feature and help pages.
2. What the interface tells the user: labels, limits, and error messages.

When the expected behavior is unclear, I record it as an open question, not as a bug.

## Scope

In scope:

- Task management: create, edit, move, and complete a task, including subtasks.
- WIP limits: set a limit on a column and check behavior under, at, and over the limit.

Out of scope:

- Premium-only features, timers and Pomodoro statistics, integrations, and the API.
- Account sign-up, login, and billing.
- Mobile, other browsers, performance, security, and accessibility testing.
- Automation.

## Approach

- Functional testing, positive and negative.
- Field validation with equivalence partitioning and boundary value analysis.
- One timeboxed exploratory session on the same two flows.
- Retest of every bug I report.

All testing is manual, uses normal user actions on my own account, and stays within KanbanFlow's Terms of Service. Anything that looks like a security issue is reported privately to the vendor and kept out of this repository.

## Environment

- Google Chrome (latest stable) on desktop. The exact browser version and operating system are recorded in each bug report.
- Test data: invented task names and descriptions only, such as "Test task 01". No personal data in test data or screenshots.

## Entry criteria

- Free account active.
- KanbanFlow's Terms of Service reviewed.
- Test cases written, with expected results, before execution starts.

## Exit criteria

- Every test case executed and marked Pass, Fail, or Blocked.
- Every failed test case linked to a bug report.
- Every bug retested at least once.
- Numbers in the test summary match the test case files.

## Defect reporting

Each bug gets its own file in `bugs/` with steps, expected and actual results, environment, and evidence.

Severity (impact on the user):

- High: a core action cannot be completed.
- Medium: a core action works but gives a wrong result or needs a workaround.
- Low: a cosmetic issue or unclear message.

Priority (how soon it should be fixed) is High, Medium, or Low, with a one-line reason in each report.

## Deliverables

Test plan, test cases, exploratory session notes, bug reports with evidence, and a test summary.

## Risks

- No official requirements. Mitigation: expected results come only from the official pages and on-screen text, as described under Test basis.
- The app or free plan may change during the project. Mitigation: each execution and bug report records the date tested.
- Single tester. Mitigation: the exploratory session covers paths the scripted cases miss.
