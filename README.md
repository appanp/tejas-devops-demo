
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

## References for GoCD 

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

## Value Stream Mapping (VSM) - What Is?

1. [What is VSM - Teamcity](https://www.jetbrains.com/teamcity/ci-cd-guide/concepts/value-stream-mapping/)
1. [VSM, Plutora blog](https://www.plutora.com/blog/value-stream-mapping)
1. [Value Stream Mapping (VSM) Metrics]()
1, [Ch.4 in Cont. Delivery with Windows & .NET Book](https://www.oreilly.com/library/view/continuous-delivery-with/9781492042327/ch04.html)
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

