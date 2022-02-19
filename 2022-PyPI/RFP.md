# PyPI 2022 Request for Proposals

The [Python Software Foundation](https://python.org/psf-landing) has funding available for designing, developing and deploying organization accounts in PyPI.

[PyPI](https://pypi.org/) is the official repository of [Python](https://www.python.org/) packages. PyPI allows users to search for packages, publish and distribute packages.The aim of this project is to allow PyPI users to set up an organization account, invite other users to join, organize those users into teams, and manage ownership and permissions across multiple projects. We hope to provide organization accounts as a paid service to companies and complimentary access to community projects. The organization account feature will provide the structure based on which new features can be offered to paying customers. You can read [this post](https://pyfound.blogspot.com/2021/12/pypi-user-feedback-summary.html) that summarizes the user surveys. 

We hope to hire two contractors who will code, test, review, document and deploy the organization account features. The two contractors include one backend developer and one frontend developer.

Please read this RFP to know how to submit your proposal or to get in touch with us.

## Timeline

|Date|Milestone|
|---|---|
|February 16|Request for Proposal period opens|
|March 4|Request for Proposal period closes|
|March 11|Submitted proposals receive preliminary decision|
|March 18|Shortlisted proposals receive final decision|
|March 25|Contracts finalized|
|April 1|Start of contract work|

## What is the Request for Proposals period?

**A Request for Proposal (RFP)** is a process intended to allow us (the Python Software Foundation) to collect proposals from potential contractors and select contractor(s) best suited to fulfill the specified work.
After the RFP period closes we will evaluate the received proposals based on the [evaluation criteria](#evaluation-criteria), seek clarification from proposers as necessary, and select one or more contractors to complete the work specified in the [scope section](#scope).

**Note**: This Request For Proposal document may be updated to reflect things that we learn during the process. The canonical version and history is available [here](https://github.com/psf/request-for/blob/main/2022-PyPI/RFP.md).

## How do I submit a proposal?

Fill this [form](https://forms.gle/pdQU7WhLfJVMq9BKA) and attach the proposal as a PDF file. Form submissions without the proposal file will not be considered. 

Proposals must be submitted before the end of the day **March 4, 2022 [AoE](https://www.timeanddate.com/time/zones/aoe)**

### Elements of proposal

A submission must, at a minimum, include the following elements:

- Description of the team or person that will perform the work.
  - What Role(s) are you proposing for? Please propose for Frontend Developer, Backend Developer, or both.
  - General overview and names of individuals.
  - Experience with [relevant technologies](#specific-technologies-used). This could be a copy of your CV/résumé.
  - Who would the PSF be contracting with? Are you an individual freelancer or a firm/corporation? If you're subcontracting, then to whom?
  - Examples of similarly-complex projects completed previously. Referencing contributions to free/open source projects is encouraged.
  - Links to Github repo or projects
  - For the frontend developer role, please highlight any UX/UI design experience
- Agreement to [project management and reporting](#project-management-and-reporting) requirements.
- Agreement to the [PSF Code of Conduct](https://www.python.org/psf/conduct/)
- Agreement to our project timeline for the Role(s) proposer is applying for (proposers may suggest adjustments based on your availability).

Please submit a **single PDF file**.

## Evaluation criteria

### Potential pass/fail:
 - Contains all elements specified in the [elements of the proposal](#elements-of-proposal).
 - Proposal is detailed enough to properly assess further criteria.
 - Formatting and submission requirements:
   - Portable Document Format (PDF)
   - Submitted by this [form](https://forms.gle/pdQU7WhLfJVMq9BKA) by **March 4, 2022 [AoE](https://www.timeanddate.com/time/zones/aoe)**
   
### Experience and competence
- Does the proposal demonstrate relevant experience necessary to complete the work?
- Is there demonstrable experience with enough of the [relevant technologies](#specific-technologies-used) for each Role to support timelines?
- Do the examples of similarly complex projects and any references to past free/open source software contributions indicate competence?

### Process and timeline
- Do the proposers agree to the [project management and reporting](#project-management-and-reporting) requirements?
- Do the proposers agree to the [PSF Code of Conduct](https://www.python.org/psf/conduct/)?
- Do the proposers agree to the project timeline for the role? Are deviations from our timeline explained and supported?

Shortlisted proposals will be invited for an interview.

## Scope

This RFP is seeking a **backend developer** and a **frontend developer** to code, test, document and deploy the organization account feature in [PyPI](https://pypi.org/). 

### Summary and budget for both roles

Budget for each role: Up to US $98,000 for approx. 560 hours depending on contractor rate

We expect both roles to start by early April. Both roles can be done remotely. Each working week consists of 35 hours. Each milestone is applicable to the backend and frontend developer roles.

#### Milestone 1 - Define owner, admin and member roles

Timeline: 10 weeks

Specific tasks
- Onboarding
- Enable a user to create an organization account
- Define permission level for owner, admin and member
- Allow management of users in a organization based on permission level
- Allow management of projects in a organization based on permission level

#### Milestone 2 - Define billing manager role and billing mechanism

Timeline: 3 weeks

Specific tasks
- Define billing manager role
- Define billing mechanism by which payment will be collected and managed

#### Milestone 3 - Define PSF admin role

Timeline: 3 weeks

Specific tasks
- Define PSF admin role
- Create dashboard to manage accounts and view analytics

## Expectations and Requirements

### Project Timeline

This project is intended to be completed over a 16 week period beginning April 2022. Proposals with a shorter or longer timeline are acceptable if it is explained, and supported by estimated budget and costs.

### Technology

The codebase behind PyPI is called [Warehouse](https://github.com/pypa/warehouse) and is licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0). All work submitted or dependencies added must be compliant with this license.

The backend codebase is in Python with a CSS, HTML, and JavaScript frontend (using the [Stimulus](https://stimulusjs.org/) framework).

Familiarity and expertise with all technologies is not required. Strong Python skills and experience are a must, though.

#### Specific Technologies Used

For the best primer, see the [developer documentation](https://warehouse.readthedocs.io/development/) for Warehouse.

You can also see the [complete codebase](https://github.com/pypa/warehouse) on GitHub.

##### Backend

* [Python](https://www.python.org/) 3.9
* [Pyramid](https://trypyramid.com)
* [PostgreSQL](https://www.postgresql.org) - [SQLAlchemy](https://docs.sqlalchemy.org/en/latest/) - [psycopg2](http://initd.org/psycopg/)
* [Redis](https://redis.io)

##### Frontend

Note: Our frontend is primarily static; these tools power the toolchain that creates our final assets.

* [Node](https://nodejs.org/en/)
* [Gulp](https://gulpjs.com/)
* [SASS](https://sass-lang.com)
* [Stimulus](https://stimulusjs.org/)

### Project management and reporting

This project will run in 2 week sprints with testing at the end of each sprint. The project manager will create a sprint board to ensure project progress visibility. Each milestone will consist of task tickets which can be viewed on the sprint board. Contractors will be expected to attend weekly meetings lasting 30-45 minutes to assess project progress, provide additional updates via Slack, participate on the sprint board and submit code for testing. Testing will be done by the contractors and end users.

## Contact

If you have any questions, please email the Packaging project manager- [Shamika Mohanan \<sm@pyfound.org\>](mailto:sm@pyfound.org)
.


