# Jira Workflow & Risk Automation

## Overview

A Jira-based workflow automation project designed to identify high-priority work items, flag potential delivery risks, and automatically notify stakeholders.

## Objective

The objective was to automate risk communication within an engineering workflow instead of relying on manual monitoring of high-priority work items.

## Tools Used

- Jira
- Jira Automation
- JQL
- Outlook

## Automation Workflow

The automation is triggered when a work item is transitioned.

### Workflow

1. **Trigger:** Work item transitioned
2. **Action:** Add a comment to the work item
3. **Condition:** Check whether the work item matches:
   `priority in (Highest, High)`
4. **Action:** Send a customized email risk alert to the initiator

## Risk Alert

The automated email includes:

- Issue key
- Issue summary
- Priority
- Status
- Assignee
- Delivery-risk message

## Testing

The automation was tested using Jira work item `SCRUM-12`.

The work item was transitioned through different statuses, triggering the configured automation.

The test successfully demonstrated:

- Automated Jira comments
- High-priority filtering using JQL
- Automated email notification
- Dynamic issue information in the email

## Business Value

This automation helps reduce manual follow-up on high-priority work items and provides faster visibility into potential delivery risks, blockers, and dependencies.

## Project Outcome

The project demonstrates how Jira Automation and JQL can be used to create a lightweight risk-monitoring workflow for engineering teams.
