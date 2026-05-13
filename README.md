# preflight-test-target

## Description

This repository is a demo target for validating Preflight supply chain security scanning in GitHub Actions.

Demo repository for [Preflight](https://github.com/Javeria-taj/preflight-ai) supply chain security scanning.

This repo demonstrates Preflight catching the axios supply chain attack (March 31, 2026) in a real CI/CD pipeline.

## How it works

Any PR that modifies `package-lock.json` triggers the Preflight GitHub Action, which:
1. Diffs the lockfile to find changed dependency versions
2. Sends each changed package to the Preflight analysis API
3. Posts a verdict (PASS / WARN / BLOCK) as a PR comment
4. Sets a GitHub commit status check
