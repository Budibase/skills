---
name: prqa
description: Test a Budibase community GitHub PR
---

# PR QA Skill

This skill is for QA testing a pull request.

The user will provide you with a PR link for the Budibase GitHub repo.
Explore this PR and make sure a linked issue is present. 
If no linked issue is present, comment on the PR, mentioning the original poster, that they need to link an issue. 

If/when an appropriate issue has been linked, explore the linked issue to understand the intent of the pull request. 

When starting a QA review, add the `qa-bot-started` label to the PR.

Next checkout their pull request and spin up Budibase. Be sure to use a separate git worktree so it does not interfere with my local dev work. 

Test the the feature and ensure it meets the specification of the linked issue. 

**Important**: If you are unable to test the UI (if it's a UI feature/bug fix) then do not post any messages and halt.

If you find any discrepancies or bugs, comment on the PR. Ideally provide screenshots or a recording if there is a visual problem.

If there is a lint issue via `yarn lint` or 'This branch is out-of-date with the base branch' on the PR, then let the original poster know that the lint or out-of-date branch issue needs addressed. 

If the bug fix / feature implementation behaves as expected, and there are no other issues, then comment LGTM with a list of scenarios that you had tested. Add the `qa-bot-lgtm` label to the PR.

If the feature is front-end, provide a screenshot or recording showing the functionality being tested. 


## Dev Instructions

These are the instructions for running Budibase after you have checked out the PR branch.

- Check the ports in `.env` file of the worktree are available. If not, then change the ports as needed.
- Run `yarn` to install the dependencies
- Run `yarn dev` to spin up Budibase
- Access Budibase as `localhost:10000` 