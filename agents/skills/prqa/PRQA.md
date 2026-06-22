---
name: prqa
description: Test a Budibase community GitHub PR
---

# My Skill

This skill is for QA testing a pull request.

The user will provide you with a PR link for the Budibase GitHub repo.
Explore this PR and make sure a linked issue is present. 
If no linked issue is present, comment on the PR, mentioning the original poster, that they need to link an issue. 

If/when an appropriate issue has been linked, explore the linked issue to understand the intent of the pull request. 

When starting a QA review, add the `qa-bot-started` label to the PR.

Next checkout their pull request and spin up Budibase. Test the the feature and ensure it meets the specification of the linked issue. 

If you find any discrepancies or bugs, comment on the PR. 

If the bug fix / feature implementation behaves as expected, then comment LGTM with a list of scenarios that you had tested.  


## Dev Instructions

These are the instructions for running Budibase after you have checked out the PR branch.

- Run `yarn` to install the dependencies
- Run `yarn dev` to spin up Budibase
- Access Budibase as `localhost:10000` 