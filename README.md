
## GoCD Essentials

GoCD pipeline model as UML class diagram is available [here](./docs/). Description of the classes in the model are given below:

1. [Pipeline]() is the central concept which has:
    * [Stages]() which are run sequentially.
    * Each stage has one or more [jobs]() which can be run parallely.
    * Each job has one or more [tasks]() which run sequentially.
1. [Material]() is the trigger that runs a pipeline.
    * Trigger can be change in repo detected thru polling
    * Webhook sent by the git repo - [webhook with Bitbucket server](https://github.com/gocd/gocd/issues/9087)
1. [Agent]() is the ones which does the work allocated by the server.
    * Agents can be *static* (have a fixed number of them running or *elastic* - start whenever required.
    * [Agent can't connect to the server](https://github.com/gocd/gocd/issues/7038)

## Frequently Asked Questions

1. Which entity monitors the git repo - server or agent?
    * The answer to this means where we need to generate ssh keys for private git repo access
1. Which entity checks out the git repo - server or agent?
    * Again required to setup ssh keys for password-less repo access.
1. How to set the repo polling interval?
1. How to trigger a pipeline only when the latest commit has a version tag or label?
    * This could also be achieved by having the first stage check for presence of git label.

## TO DOs

- [ ] Installation of GoCD server & agent
    * [x] Local installation in laptop *without* PostgreSQL.  
          *Did not work* since [Java16 has some issues](https://github.com/gocd/gocd/issues/9469).
          Installed Oracle Java15 & configured the Java path in `wrapper-config/wrapper-properties.conf` file.
    * [ ] Remote installation in Azure *without* PostgreSQL
    * [ ] Remote installation in Azure *with* PostgreSQL
- [ ] Explore how [Azure Elastic Agent Plugin](https://github.com/gocd/azure-elastic-agent-plugin) can be used for pipelines.
- [ ] Update this file with the .Net Core apps short-listed from github.
    * Explain why we chose the specific app.
    * Identify anything that we add - angular testing, back-end unit-tests, etc.
- [ ] Deploy the selected app in step above in Azure.
    * This should include steps for database server.
- [ ] Check how to configure [Percy](https://github.com/marketplace/percy) with Browserstack login.
    * Make changes to the UI & see how it works.

## GoCD Compared to Jenkins

1. [Wny GoCD over Jenkins](https://www.gocd.org/2017/04/25/gocd-over-jenkins.html)

## References for GoCD 

1. [Agent 008: Chaining Vulnerabilities to Compromise GoCD](https://blog.sonarsource.com/gocd-vulnerability-chain)
1. [Installation from zip file](https://docs.gocd.org/current/installation/install/server/zip.html)
1. [Concepts in GoCD](https://docs.gocd.org/current/introduction/concepts_in_go.html)
1. [Quick pipeline setup](https://docs.gocd.org/current/configuration/quick_pipeline_setup.html)
    * [Pipeline as Code](https://docs.gocd.org/current/advanced_usage/pipelines_as_code.html)
1. [Enabling GoCD to use PostgreSQL](https://docs.gocd.org/current/installation/configuring_database/postgres.html)
1. [Effect of licensing changes on GoCD](https://www.gocd.org/2019/05/21/official-stance-on-java/), should not be affected.
1. [Configuring GoCD server details](https://docs.gocd.org/current/installation/configuring_server_details.html)
1. [GoCD Getting Started - Parts 1,2,3](https://www.gocd.org/getting-started/)
1. [.Net  Core & GoCD](https://www.gocd.org/2016/07/13/DotNet-Core-and-GoCD/)
1. [Building An Automated Testing Pipeline with GoCD [Tutorial]](https://www.lambdatest.com/blog/building-an-automated-testing-pipeline-with-gocd/)
1. [Jenkins Vs. GoCD: Battle Of CI/CD Tools](https://www.lambdatest.com/blog/jenkins-vs-gocd-battle-of-ci-cd-tools/)
1. [Codefresh CI Vs GoCD](https://www.knapsackpro.com/ci_comparisons/codefresh-ci/vs/gocd)

## Value Stream Mapping (VSM) - What Is?

1. [What is VSM - Teamcity](https://www.jetbrains.com/teamcity/ci-cd-guide/concepts/value-stream-mapping/)
1. [VSM, Plutora blog](https://www.plutora.com/blog/value-stream-mapping)
1. [Value Stream Mapping (VSM) Metrics]()
1. [Ch.4 in Cont. Delivery with Windows & .NET Book](https://www.oreilly.com/library/view/continuous-delivery-with/9781492042327/ch04.html)
    * Has references to tools for Deployment Pipelines
    * [BuildMaster](https://inedo.com/buildmaster), [Octopus](https://octopus.com/pricing/overview), Teamcity, etc. 
1. [Plutora VSM Book](https://go.plutora.com/mastering-software-delivery-with-value-stream-management)
1. [Copado VSM use-cases & limits](https://docs.copado.com/article/5zf0fd4lar-value-stream-mapping-use-case-and-limits)
1. [Plandek for DevOps managers](https://plandek.com/platform/devops-managers/)

## Runbook Automation

1. [What's runbook (Pagerduty)](https://www.pagerduty.com/resources/learn/what-is-a-runbook/) and how to automate it?

## Database Migration Tools

1. [Fluentmigrator](https://github.com/fluentmigrator/fluentmigrator)

## Microsoft .NET Links

1. [.NET Fundamentals](https://docs.microsoft.com/en-us/dotnet/fundamentals/) - PDF file of the whole docs turns out to 5000 pages!!
1. [.NET Core Command-Line Interface](https://www.tutorialsteacher.com/core/net-core-command-line-interface)
    * [.NET Core Application Types](https://www.tutorialsteacher.com/core/dotnet-core-application-types) - portable, self-contained.
    * More explanation of these types in [this deployment page](https://docs.microsoft.com/en-us/dotnet/core/deploying/)
    * `.csproj`, `project.json`, `.sln` files - which one to use & what is the difference?
1. [Learn dotnet CLI(Command Line Interface for .Net Core) in 10 Minutes](http://www.codedigest.com/quick-start/6/learn-dotnet-clicommand-line-interface-for-net-core-in-10-minutes)
1. [10 commands you don't want to be without in .Net Core](https://softchris.github.io/pages/dotnet-10-commands.html#_4-dotnet-run)

