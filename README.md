# Workflow Scratchpad

This repo is intended to show GitHub action workflow patterns.

## Summary

Name | Summary | Descrption / Typical Use Case
---|---|---
[Fork Validate](.github/workflows/ForkValidate.yml) | Shows checking for a forked PR, and conditionally taking actions such as adding a comment to the PR. | Forked PR's cannot access Repo secrets when they run - so this leads into handling Pull Requests from forks differently where your workflow actions leverage secrets as part of the process to validate PR's
[Matrix-iterate](.github/workflows/matrix-iterate.yml) | Shows dymamically building an array which then feeds a Matrix Strategy. | Taking multiple files and validating their contents. Each files pass/fail needs to be respresented in the GitHub workflow step log.
[Issue Form](.github/workflows/ReuseableExample.yml) | On creation of a new issue form, trigger a workflow which parses issue form data and does something with it. | This could be used to provision a test AKS cluster, for example. 
[Reusable Workflows](.github/workflows/ReuseableExample.yml) | Shows how to call another workflow in the same repo | Inputs to the calling workflow are passed to the called workflow.