# OpenSAMM Public Database Schema
This is the database schema for the public OpenSAMM data repository.
## Format
The data format is currently being maintained in MySQL Workbench (cross-platform downloads available from: https://www.mysql.com/products/workbench/) Its file format is essentially a ZIP with some XML in it so it is a little messy to be versioning a binary, but it should be that large and hopefully won't require too many revisions so we'll live (for the moment).
## Notes
Here are a couple of comments intended to help navigate the data structure:
* Overall, it is assumed that Assessors will maintain a private database with additional metadata that will link (via the OrganizationId and TeamIds) to the public database. This will allow them to maintain additional, non-public information for additional in-house analysis and tracking.
* Sector refers to the general industry of the Assessed organization. Values will include: Financial Services, Software, Technology, Telecommunications, Government, Business Services, Education, Healthcare, Entertainment and Media, and Other
* Region refers to the region where the organization has its primary base of operations. Values will include: North America, South America, Europer, Middle East, Asia
* Method refers to the type of assessment that was performed. Values will include "Self-Assessment" and "Third-Party Assessment"
* Granularity refers to the level at which the assessment was performed - are results assuemd to be representative for the entire Organization, or only for a specific Team. If the Assessment was performed at a Team level of granularity, then there will be an assocaited Team record reflecting the size of the Team assessed.
* BusinessFunction maps to the four SAMM Business Functions: Governance, Construction, Verification, Deployment
* SecurityPractice maps to the twelve SAMM Security Practices: (Governance) Strategy & Metrics, Policy & Compliance, Education & Guidance, (Construction) Threat Assessment, Security Requirements, Secure Architecture, (Verification) Design Review, Code Review, Security Testing, and (Deployment) Vulnerability Management, Environment Hardening, Operational Enablement.
