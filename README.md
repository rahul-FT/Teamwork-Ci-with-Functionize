<h1 align="center">
  <br>
   <img src="https://app.functionize.com/views/images/logo/logo-small.png"/>
  <br>
</h1>
<p align="center">
<img src="https://circleci.com/gh/rahul-FT/Circle-CI-with-Functionize.svg?style=svg">
<p align="center">
  This repository contains Example Of Intregrating <strong>Functionize Smart Testing Tool </strong>with <strong>Circle CI</strong>
</p>

### Including Functionize TestsSuite in CodeBuild CI.

Requires Active Functionize.com Account.

Include This Snippet In any of the Stage/Phase, Where you want to run test-cases.
```bash
version: 2
jobs:
  build:
    docker:
      - image: node:9.11.1
    steps:
  - run:
      name: Running & Waiting Test-Cases
      command: |
        git clone https://functionize@bitbucket.org/functionize/functionizecli.git /opt/functionizecli
        cd /opt/functionizecli
        npm install
        npm install -g
        wget -O - https://bitbucket.org/functionize/functionizecli/raw/master/ThirdParty_run.sh | bash
```


## Parameters

You Need to Pass Some Parameters To make it work. Everything Can be get from app.functionize.com acccount.

| `Parameter`               | `Value`               |
|-------------------------|---------------------------|
| DEPLOYMENT_TIME | Timeout in Sec
| YOUR_SECRET_KEY | Client ID
| YOUR_API_KEY |  Client Secret
| PROJECT_DEPLOYMENT_ID | Orechestration_ID
