# Annex


**Topics**
- [Systems for Early Migration](#systems-for-early-migration)
- [Sandbox Testing Flow Details](#sandbox-testing-flow-details)
- [Migration Flow Details](#migration-flow-details)


## Systems for Early Migration  

We recommend that you consider non-CII/SII systems that are deployed to GCC Internet for early migration. Additionally, you can consider systems that have:

- DevOps resources available to support
- No major structural changes planned in the next 3 months
- May not need funding top-up required for migration to proceed


## Sandbox Testing Flow Details

1.	**Clone your Project Repository:** 
    1. Clone your Project Repository from Bitbucket to SHIP-HATS 2.0. 
    1.	Verify that the clone is successful.
1.	**Define success criteria for the CI/CD pipelines:**
    1. CI pipeline minimally checks out from source code repo, builds, performs SAST, Container scan (if applicable), SCA, DAST, and publishes packages to artifact repo.
    1. CD pipeline minimally extracts packages from artifact repo, performs SCA, connects to target environment directly and through a remote agent in DevOps zone for GCC intranet and deploys.
1.	**Configure and Test CI Pipeline:**
    1.	Configure dedicated agents.
    1.	Identify automated template from GovTech to set up CI pipeline and configured.
    1.	Test run CI Pipeline until success criteria is met.
1.	**Establish connectivity with your target environment:** 
    1. Whitelist relevant firewall.
    1. Create relevant service accounts/principles for SHIP-HATS to connect to GCC environments.
    1. Configure remote agents in DevOps zone for intranet deployments (if applicable).
1.	**Configure and Test CD Pipeline:**
    1. Use automated template from GovTech to set up CD pipeline and configure for your production environment.
    1. Test run CD Pipeline until success criteria is met. 

## Migration Flow Details

1. Verify that the source code is migrated.
1. Verify that the dedicated agents are operational.
1. Adapt and test CI/CD pipeline from Sandbox Testing: 
    1. Ensure pipeline requirements, variables, and secrets are configured.
    1. Adapt CI/CD pipeline configuration used in Sandbox Testing to your production environment.
    1. Test CI/CD pipeline until success criteria is met.
