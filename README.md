Arkhitekton - Azure Demo Generator
==================
End to End Demo generator that orchestrates the provisioning, code deployment, data setup, and load testing that provides contextual and meaningful demonstrates of Azure's capabilites.  Each Scenario is meant to showcase a mixutre of Azure Service, configured based on best practices, working in concert to solve business problems.

Explore it at https://arkhitekton.azurewebsite.net.

| Scenario            | Description                  |                  Status          |
| -------------------- | ----------------------------|-------------------------------- | 
| [Contoso Travel Web](https://github.com/andywahr/contosotravel-web)     | Distributed web platform with supporting services |   Beta |

How to contribue
------------------
Scenarios are the greatest part of the Arkhitekton project, showcasing technical creativity that provides repeatable value.  Although Contoso Travel is pretty complex, Scenarios can be much smaller.  

_**Check out the Scenario's above to see if you would like to help with one of those or come up with your own!  The only limit is your imagination and what you can abuse Azure DevOps to do for you :smirk:.**_

### Each Scenario is made up of:
- **Scenario.json** ([Documentation](https://github.com/andywahr/arkhitekton/wiki)) - Configuration files that defines:
    - Reference to the repository and Azure DevOps Build YAML to execute to deploy the infrastructure (ARM, Terraform, etc..)
    - Service Categories with a list of services to support (Web, Data, Backend, etc..)
    - Each Service Category a list of Services that satisfy that category (individual Azure Services)
    - A Service definition can then have a list of Platforms defined describing the Repository and Azure DevOps Build YAML to execute
    - List of any needed Azure DevOps plugins
    - Reference to the repository and Build to execute for the Load Test
- A Repository of those infrastructure as code assets with an Azure DevOps Build YAML 
- Optionally a Repository for load testing artifacts with an Azure DevOps Build YAML 
- One to many Repositories for code assets that make up the end to end Scenario

### Propose a new Scenario
- Currently, Scenario's are managed centrally, submit a [Scenario Request](https://github.com/andywahr/arkhitekton/issues/new?assignees=&labels=&template=scenario-request.md&title=)
- First in [configuration-dev.json](https://github.com/andywahr/arkhitekton/blob/master/configuration-dev.json)
     - Can be viewed on the Dev site https://arkhitekton-dev.azurewebsites.net
- Then live [configuration.json](https://github.com/andywahr/arkhitekton/blob/master/configuration.json)
