# Write-up Template

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

#### Chosen Solution
- App Service

*The solution that would best fit the requirement would be an App Service solution. Being a PaaS, it helps us avoid the cost and complexity of running and maintaining the infrastructure for the solution.

##### Cost Analysis

- Virtual Machines are typically more expensive to set up and maintain than App Services due to additional work needed to set up and manage the Virtual Machine. This labor intensiveness, as compared to App Services' simple tier-based pricing of resources makes App Services a better choice than Virtual Machines for this project*

#### Scalability Analysis
- The simplicity of App Services fits well with the project's scaling requirements. App Service solutions auto scale while Virtual Machines will need to be manually configured to find the "sweet spot" for the desired performance and price. This can be time consuming and needs skilled personnel to properly implement. This built in feature makes App Services a better choice over Virtual Machines for this project.

#### High Availability
- In terms of Availability, App Services have built in back up and load balancing while Vitual Machines will require one to set up their own back up solution. This simplicity makes App Services a better choice over Virtual Machines for this project.

#### Workflow Analysis
- Virtual Machines offer more customization but is also more complex to deploy. App Services, on the other hand, have more limited customization options but are typically a lot simpler to deploy. This comparable ease of deployment makes App Services a better choice over Virtual Machines for this project.

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

- Changes that would affect my decision would be new features that would require custom software to be used or if  more complex security or networking requirements arise that require more control of the solution's network and security set up. Basically, any additional requirement that requires a VM's flexibility will make me reconsider
