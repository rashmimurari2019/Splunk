# SplunkGitHub App Webhook Test with Jenkins Multibranch
This repo is used to test GitHub webhook integration with Jenkins Multibranch Pipeline using a GitHub App from a personal GitHub account.

Setup Summary
Create a GitHub App in personal account:

Homepage URL: your Jenkins base URL

Webhook URL: your Jenkins base URL + /github-webhook

Permissions:

Contents: Read-only

Pull requests: Read-only

Commit statuses: Read and write

Events:

Push

Pull request

Generate private key (PEM)

Install app on this repository

Configure Jenkins:

Install plugins:

GitHub Branch Source

Pipeline

Add GitHub App credentials:

App ID

Owner (GitHub username)

Private key (PEM content)

Create a Multibranch Pipeline job:

Branch source: GitHub

Select this repository

Enable branch and PR discovery

URL Examples
Public Jenkins

Homepage URL: https://jenkins.example.com

Webhook URL: https://jenkins.example.com/github-webhook

Local Jenkins with ngrok

Homepage URL: https://abc123.ngrok-free.app

Webhook URL: https://abc123.ngrok-free.app/github-webhook

Validation Steps
Push commit to main
Create branch and push
Open pull request
Check GitHub App Recent Deliveries shows 200
Check Jenkins created branch or PR build

Webhook test update

This is a test commit to verify GitHub App webhook delivery to Jenkins Multibranch Pipeline.
Timestamp: 2026-07-08
