# Apex Code Coverage Demo with Codecov
This project demonstrates using GitHub Actions, the Salesforce DX CLI, and Codecov to track code coverage for a Salesforce Apex Application. The sample code and GitHub Action are derived from [Jeferson Chaves' repository here](https://github.com/jefersonchaves/sfdxgithubactions).

## Prerequisites
Before you begin, you should have:

- [Salesforce DX account](https://developer.salesforce.com/promotions/orgs/dx-signup)
- [Salesforce DX CLI](https://developer.salesforce.com/tools/sfdxcli)
- [Codecov account](https://about.codecov.io/sign-up/)

## Usage
- Clone this repository locally (don't fork it as GitHub secrets won't work in forked repositories)
- Create a [new GitHub repository](https://github.com/new)
- Authorize the Salesforce CLI locally: `sfdx auth:web:login --setdefaultdevhubusername`
- Get the `Sfdx Auth Url`: `sfdx force:org:display -u <YOUR_USERNAME> --verbose`
  - Note: read about [other authentication methods here](https://medium.com/@medben/sfdx-org-authorization-%EF%B8%8F-a75b54861b54)
- Link your new GitHub repository to Codecov and get your Codecov token
- Add the following Secrets to your GitHub repository:
  - `SALESFORCE_AUTH_URL`
  - `CODECOV_TOKEN`
- Push the local code to your new GitHub repository and watch for the passing build

![Build passing in GitHub actions](https://i.imgur.com/DPc4wUY.png)

- Codecov will show you the results of your coverage on the project's dashboard

![Codecov coverage report](https://i.imgur.com/BgoyAuy.png)

## Sources
- [Salesforce DX with GitHub Actions by Jeferson Spencer Chaves](https://medium.com/@jefersonchaves/salesforce-dx-with-github-actions-563356e9434e)
- [Salesforce DX demo app using GitHub Actions and Codecov](https://github.com/trailheadapps/ebikes-lwc)
