# How to use the ABC Guide

## General Guidance

**It is recommended to open the guide using the desktop version of Excel.** If the file is slow to open or navigate consider saving the guide to a location outside of OneDrive (or turn off AutoSave) since this will cause Excel to pause frequently when writing the file.

![Turn off AutoSave](media/autosave.png)

### Navigation

<img src="media/navigation-buttons.png" alt="Navigation Buttons" width="90"/>

In each page of the guide, you will find quick access navigation buttons at the top left. These buttons will take you to the main sections of the guide.

<img src="media/home-button.png" alt="Home Button" width="32"/>Navigate to Business Continuity and Disaster Recovery Framework (Home)

<img src="media/personas-button.png" alt="Personas Button" width="32"/>Navigate to Personas: Business Continuity and Disaster Recovery by Role and Task

<img src="media/glossary-button.png" alt="Glossary Button" width="32"/>Navigate to Glossary

<img src="media/references-button.png" alt="References Button" width="32"/>Navigate to References

### Collapsible Sections

Many of the pages include sections that have been collapsed or expanded by default. Look for the **[+]** and **[-]** buttons to expand or collapse sections.

![Collapse Button](media/collapse-button.png)Collapse this section

![Expand Button](media/expand-button.png)Expand this section

### Filters

Some of the pages in the guide have built-in filters you can leverage by simply clicking on the desired button 

![Category Filter On](media/category-filter-on.png)<br>
(Show items in the Availability, Deployment and General categories)

![Category Filter Off](media/category-filter-off.png)<br>
(Show only items in the General category)

### Footnotes

Many of the templates and examples will include a list of footnotes at the bottom of the worksheets. When first viewing the guide it is a good idea to check the footnotes and become familiar with the details. It will help you understand the templates better.

### Other tips

- Familiarize yourself with the sections of the guide and ensure you are using the latest version. For a high-level introduction you can refer back to the [read me](README.md) in this repo, which gives an overview of each phase of the planning process.
- Be sure to review the Personas view to see how each role is involved (Application Owner, Architects, etc) and the steps in sequence they are responsible for in completing templates in the guide.

---

## Phase 1: Prepare

### Concepts

Building a Business Continuity and Disaster Recovery (BCDR) strategy is crucial for ensuring the resilience of a business in the face of unforeseen disruptions or disasters. This section is composed of important documentation that we recommend reading as you prepare and look back to for reference in later phases. In order to be ready for BCDR strategy discussions, it is strongly suggested to be aware of the concepts in this section.

The Prepare phase of the guide, as well as the other phases, includes numerous footnotes at the bottom of the "home" page. Be sure to look for the superscript numbers and review the footnotes to understand the details of the templates and examples. In some cases the footnotes will include a list of links that apply to a particular concept. For example, you will find 3 links related to Reliability Trade-Offs<sup>8</sup>:

![Reliability Trade-Offs Footnote](media/reliability-trade-offs-footnote.png)

### Supporting Artifacts

In this section you will find the main templates to be used during the BCDR strategy discussion. These templates are meant to be used as a starting point and can be modified to fit your organization's needs. The templates included are as follows:

#### Criticality Model (example)

Enterprise organizations typically have a large application portfolio, but not all applications are of equal importance. Applications should be classified based on a [criticality scale](https://learn.microsoft.com/azure/cloud-adoption-framework/manage/considerations/criticality#criticality-scale). The table should be customized as needed. More suggestions and insights can be found in this article:

**[Business criticality in cloud management](https://learn.microsoft.com/azure/cloud-adoption-framework/manage/considerations/criticality)**

The Criticality Model is a table to be used to summarize the different levels of criticality and the associated business view (what’s going to be impacted in case of outages). Criticality should be identified and classified to direct investment of business continuity, monitoring, support, and other resources appropriately. It should be noted that certain business functions within applications may also be more critical than others.

![Criticality Model (example)](media/Prepare-Criticality_Definitions.png)

Creating a criticality scale is the first important step in building the BCDR strategy. It helps in:

- **Understanding priorities:** identify which system, processes or assets are essential for the operations and which ones are less critical (and allocate resources accordingly during a disaster).
- **Allocating Resources:** ensure that the most critical elements are protected to a higher degree, considering that not all parts of the business can receive the same level of investment.
- Facilitating quick, informed decisions during disasters.
- Establishing a clear hierarchy of priorities for better response and recovery.

#### Business Commitment Model

When implementing a BCDR strategy it is important to build a detailed view of all the various aspects of business commitment required for each level of criticality. This is important to ensure that the plan is comprehensive and tailored to the specific needs of each application (according to its criticality level requirements).

Defining business commitments for each application will facilitate a more efficient allocation of resources and a targeted response to potential disruptions, protecting the organization's operations and reputation.

***How to use this template***

For each Criticality Level, define if a specific aspect needs to be calculated or documented and which type of tests are required. Each aspect or test type should be labeled as "Required", "Not Required" or "As Required".

![Business Commitment Requirements Legend](media/business-commitment-requirements.png)

🔍**ATTENTION:**
The Business Commitment Model template contains several vertical sections that are hidden by default. Be sure to expand the sections to see the full list of requirements. When all the sections are collapsed you can see the condensed topics in a "page size" view and the tables might look empty (as seen below).

![Business Commitment Model - Collapsed by Default](media/business-commitment-model-collapsed.png)

As you can see, for each tier a criticality level is defined and the corresponding commitment level is indicated as follows:

- Enhanced
- Standard
- Base
- None

##### General Requirements

The General requirements are expanded by default with all the considerations that need to be defined. This includes a list of the most important metrics to be defined and all details that needs to be discussed and documented. For example, an SLA of 99.999% being required for your mission critical applications. Mission critical would also have MTD (Maximum Tolerable Downtime), RPO and RTO optionally required. 

Some of the headings in general requirements refer to the need to prepare a specific document (and later in the BCDR strategy implementation, you can reuse examples or fill out templates provided within the ABC Guide – e.g. Business Impact Analysis, Contingency Plan…)

![Business Commitment Model - General Requirements](media/business-commitment-model-general-requirements.png)

##### Availability Requirements

Availability refers to the degree to which a system or service is operational and accessible when needed. High availability is crucial for mission-critical applications as it minimizes downtime and ensures that users can access services without disruption. Achieving high availability involves redundancy, failover mechanisms, and proactive monitoring.

The aim of the availability requirements is to help you keep track of how you plan to achieve Availability for the different aspects of all the applications belonging to the same criticality group. 

![Business Commitment Model - Availability Requirements](media/business-commitment-model-availability-requirements.png)

##### Recoverability Requirements

Recoverability is the ability to restore a system or service to its normal state after a disruption or failure. It encompasses the processes and technologies used to recover data, applications, and infrastructure.
In a BCDR strategy, recoverability is essential for business continuity. It includes backup and restoration procedures, disaster recovery plans, and redundancy to minimize data loss and downtime.

With the recoverability requirements you can keep track of the backup retention period required, the recovery architecture and if cross region replication needs to be implemented for a specific group of applications (with the same criticality level).

![Business Commitment Model - Recoverability Requirements](media/business-commitment-model-recoverability-requirements.png)

##### Deployment Requirements

Deployment refers to the process of setting up and configuring software applications, infrastructure, and resources to make them operational. Deployment can be done manually or automated, such as through Infrastructure as Code (IaC). Discussing deployment methods is crucial for ensuring consistency and repeatability. Automation, like deploying resources and configurations from a code repository, can help in rapidly restoring systems to their pre-disruption state.

Use the deployment requirements to define what will be implemented for each criticality level according to the business commitment. 

![Business Commitment Model - Deployment Requirements](media/business-commitment-model-deployment-requirements.png)

##### Monitoring Requirements

Monitoring involves continuous tracking and observation of the health, performance, and security of systems, applications, and infrastructure. It includes the collection of metrics and alerts for proactive issue detection. Monitoring is essential for identifying anomalies and taking proactive measures to maintain system health and performance. It's a key component for early detection of potential disruptions and planned maintenance.

As it pertains to BCDR planning, you should define the monitoring requirements in detail to ensure that the right metrics and logs are available to support the recovery process. The alerting requirements should include the notification methods and severity thresholds for each criticality level.

![Business Commitment Model - Monitoring Requirements](media/business-commitment-model-monitoring-requirements.png)

##### Security Control Requirements

Security control refers to measures and procedures put in place to safeguard data, systems, and infrastructure from threats and vulnerabilities. This includes access controls, encryption, firewall rules, and more.

Discussing security controls is vital to prevent security breaches and data loss during and after disruptions. Security measures should be integrated into the BCDR strategy to protect business assets. For example, you may decide to require DDoS Protection for all critical applications, but leave it as optional for all other applications.

![Business Commitment Model - Security Control Requirements](media/business-commitment-model-security-requirements.png)

##### Validation and Testing Requirements

Validation and testing processes should be considered for each criticality level. Keep in mind that the highest criticality levels are likely to require the highest level of testing and validation. Types of tests will vary by criticality level too. For example, a mission critical application may require failover testing, load testing, chaos testing, penetration testing and more. A non-critical application may only require failover testing. The frequency of testing should also be defined for each criticality level.

![Business Commitment Model - Validation and Testing Requirements](media/business-commitment-model-testing-requirements.png)

#### Fault Model and Resilience Strategies (example)

A useful preparation step that the organization should consider is to define common types of failures along with agreed resiliency strategies that should be implemented. Documenting types of failure with pre-approved mitigation strategies for each application criticality tier simplifies the tasks of creating business commitment models, performing application fault tree analysis and designing BCDR solutions.

In the example you can see how recovery is planned for different types of scenarios/events to achieve resiliency. The guide provides a good example of what a typical fault model may look like for cloud-based workloads. It is recommended to use a similar approach to document the fault model for your organization. As an alternative, you may simply document the failure modes and mitigation strategies in a document similar to the following article:

**[Failure mode analysis for Azure applications](https://learn.microsoft.com/azure/architecture/resiliency/failure-mode-analysis)**

#### RACI

The RACI table is a project management tool used to clarify roles and responsibilities for each task, activity or decision in a project. This template can be used to define both the application and organization BCDR roles and responsibilities.

![RACI Legend](media/RACI-legend.png)

#### Application Requirements (template)

A workshop (or series of workshops) with all relevant stakeholders is recommended to gather relevant information for each application. 

In the template you’ll find a list of requirements grouped by category. You can click on one of the categories listed to automatically filter the requirements listed in the table. You can use this template to assess each application's BCDR requirements for a new or existing system. The responses can then be used in the other templates in this guide.
You will find an example of how this template can be used later in Phase 2: Application Continuity (refer to the first link in the ASSESS group).

#### Test Plans (template)

This template defines the types of tests that need to be considered for each application, depending on its criticality and the related business commitment. You will find built-in instructions for each of the mentioned test. A description of the type of test and links are also available in the same table.

- Production Redeployment Test
- Failover + Failback Test
- Recovery Test
- Unit Test
- Smoke test
- UI Test
- Load Test
- Stress Test
- Performance Test
- Chaos Test (also to validate impact on specific components like Entra ID or DNS outage)
- Penetration Test
- User acceptance Test
- Contingency Test

For each test it’s important to define and keep track of the following:
- Frequency / Last Test Date / Next Test Date / If automation and a test schedule are in place.
- Outcome of the tests (functional results, performance results, Duration, RTA, RPA…)
- Owner / people involved
