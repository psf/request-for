# PyPI Quarter 1 2019 Request for Proposals

The [Python Software Foundation](https://python.org/psf-landing) [Packaging Working Group](https://www.python.org/psf/committees/#packaging-work-group) has applied for and received a commitment from the [Open Technology Fund](https://www.opentech.fund) to fulfill a contract for their [Core Infrastructure Fund](https://www.opentech.fund/funds/core-infrastructure-fund/).

[PyPI](https://pypi.org) is a foundational component of the [Python](https://python.org) ecosystem and broader computer software and technology landscape. This project aims to improve the security and accessibility of PyPI for all users worldwide, whether they are direct users like project maintainers and [`pip install`](https://pip.pypa.io/en/stable/)ers or indirect users. The impact of this work will be highly visible and improve crucial features of the service.

We plan to begin the project in January 2019. Because of the size of the project, funding has been allocated to secure one or more contractors to complete the development, testing, verification, and assist in the rollout of necessary features.

## Timeline

|Date|Milestone|
|---|---|
|2018-10-30|Request for Information period opened.|
|2018-11-13|Request for Information period closed.|
|2018-11-??|Request for Proposal period opens.|
|2018-11-30|Request for Proposal period closes.|
|2018-12-7|Date proposals will have received a decision.|
|2019-12-31|Contracts for accepted proposals should be finalized.|
|2019-01|Contract work commences.|

## What is the Request for Proposals period?

A Request for Proposals (RFP) is a process intended to allow us (The Python Software Foundation) to collect proposals from potential contractors and select contractor(s) best suited to fulfill the specified work.

After the RFP period closes we will evaluate the received proposals based on the [Evaluation Criteria](#evaluation-criteria), seek clarification from proposers as necessary, and select one or more contractors to complete the work specified in the Scope section.

**Note**: This Request For Proposal document may be updated to reflect things that we learn during the process. The canonical version and history is available [here](https://github.com/python/request-for/blob/master/2019-Q1-PyPI/RFP.md).

## How do I submit a proposal?

Proposals should be submitted as [Portable Document Format (PDF)](https://en.wikipedia.org/wiki/PDF) files via email to [ernest@python.org](mailto:ernest@python.org).

Proposals must be submitted before **December 1, 2018 [AoE](https://www.timeanddate.com/time/zones/aoe)** (2018-12-01T12:00+00:00:00).

### Elements of Proposal

A submission must, at a minimum, include the following elements:

- Description of the team that will perform the work.
  - General overview and names of individuals.
  - Experience with [relevant technologies](#specific-technologies-used).
  - Freelance or Firm? Incorporation? Subcontracting?
  - Free/Open Source Software experience?

- Agreement to [Project Management and Reporting](#project-management-and-reporting) requirements.

- What Milestone(s) are you proposing for?
  - We recommend proposing for all of the work in scope of Milestone 1, Milestone 2, or both.

- Examples of similarly-complex projects completed previously.
  - Referencing contributions to Free/Open Source projects is encouraged.

- Project timeline estimates by Milestone and Task. These timelines should fit within our [Project Timeline](#project-timeline).
  - Milestone 1 - Security - MFA
  - Milestone 1 - Security - API Keys
  - Milestone 1 - Security - Audit Trail
  - Milestone 2 - Accessibility and internationalization - Accessibility
  - Milestone 2 - Accessibility and internationalization - Internationalization

- Project budget by Milestone and Task. Deviations from our [Estimated Budgets and Caps](#estimated-budgets-and-caps) should be described and supported.
  - Milestone 1 - Security - MFA
  - Milestone 1 - Security - API Keys
  - Milestone 1 - Security - Audit Trail
  - Milestone 2 - Accessibility and internationalization - Accessibility
  - Milestone 2 - Accessibility and internationalization - Internationalization

## Evaluation Criteria

### Potential Pass/Fail:

 - Contains all elements specified in [Elements of Proposal](#elements-of-proposal).
 - Proposal is detailed enough to properly assess further criteria.
 - Formatting and Submission requirements:
   - Portable Document Format (PDF)
   - Emailed to [ernest@python.org](mailto:ernest@python.org) by **December 1, 2018 [AoE](https://www.timeanddate.com/time/zones/aoe)**

### Experience and Competency

- Does the proposal demonstrate relevant experience necessary to complete the work?
- Is there demonstrable experience with enough of the [relevant technologies](#specific-technologies-used) for each Milestone to support timelines?
- Do the examples of similarly complex projects and any references to past Free/Open Source Software contributions indicate competency?

### Cost

- Does the budget proposed fit within our [Estimated Budgets and Caps](#estimated-budgets-and-caps)?
- Are the Milestone and Task budgets reasonable and competitive?
- Are any deviations from the [Estimated Budgets and Caps](#estimated-budgets-and-caps) well supported and explained?

### Process and Timeline

- Do the proposers agree to [Project Management and Reporting](#project-management-and-reporting) requirements?
- Are the project timeline estimates within our [Project Timeline](#project-timeline)?

## Scope

This Request for Proposals is seeking Backend Developers to implement, test, verify, and assist in the rollout of the following features to the codebase that powers [PyPI](https://pypi.org/).

### Milestone 1 - Security development

#### Summary

* Support for two-factor authentication via [TOTP](https://tools.ietf.org/html/rfc6238) and [U2F/FIDO](https://fidoalliance.org/specifications/overview/).
* Application specific tokens scoped to individual users/projects (this will also cover adding token based login support to twine and setuptools)
* Advanced audit trail of user actions beyond the current journal (allowing publishers to track all actions taken by third party services on their behalf).

#### Specific Tasks

Multi-Factor Auth (MFA):

[Relevant background and context](https://github.com/pypa/warehouse/issues/996)

* Implement TOTP
* Implement U2F/FIDO
* Adding/Removing MFA user flow
* Add support for login w/ MFA user flow API Keys

API Keys:

[Relevant background and context](https://github.com/pypa/warehouse/issues/994)

* Implement per-User API Keys
* Adding/removing User API keys flow
* Implement per-Project API Keys
* Adding/removing Project API keys flow 

Audit Trail:

* Adding audits for User actions
* Adding audits for Project actions
* Implement User view for User auditing
* Implement Project view for Project maintainer auditing
* Implement Admin view for administrator auditing


### Milestone 2 - Accessibility and internationalization development

#### Summary

Accessibility audit and follow-on accessibility repair work, implementing localization and internationalization features for views, creating tooling to support translators, and integrating translations into PyPI.

#### Specific Tasks

Accessibility:

* Implement backend features required to support making the codebase [WCAG 2.0 AA](https://www.w3.org/WAI/intro/wcag) compliant.

[Relevant background and context](https://github.com/pypa/warehouse/labels/accessibility)

Localization:

* Implement localization and internationalization features
* Choosing a localization framework compatible with [Pyramid](https://trypyramid.com/) and integrating it into our application
* Replacing hardcoded English messages with localized messages in browser and email templates
* Implementing integration with [Transifex](https://www.transifex.com/) or another localization platform

[Relevant background and context](https://github.com/pypa/warehouse/issues/1453)

## Estimated Budgets and Caps

Budgets and Caps are provided to help contractors in preparing their proposals. 
Budgets are estimates created during the formation of our proposal to Open Technology Fund and Caps are based on the funding commitment that we have received.

Caps are provided so that it is understood that some features may require more funds than our estimated Budget. Proposals may go over Budget up to the Cap for one feature but fall under Budget for another.

Estimates and Caps are presented in United States Dollars.

### Milestone 1 - Security development

|Feature|Budget|Cap|
|---|---|----|
|Multi-Factor Auth|$8,000|$10,000|
|API Keys|$8,000|$10,000|
|Audit Trails|$5,000|$7,000|

### Milestone 2 - Accessibility and internationalization development

|Feature|Budget|Cap|
|---|---|----|
|Accessibility|$2,000|$3,500|
|Localization|$10,000|$12,000|

## Expectations and Requirements

### Project Timeline

This project is intended to be completed over a three to five month period beginning January 2019.

### Technology

The codebase behind PyPI is called [Warehouse](https://github.com/pypa/warehouse) and is licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0), all work submitted or dependencies added must be compliant with this license.

The backend codebase is in Python with a CSS, HTML, and Javascript frontend (using the [Stimulus](https://stimulusjs.org/) framework).

Potential proposers should be comfortable with Python and may need to implement some features or views for the frontend, but will have support of an additional contractor focused on User Interface and User Experience to implement CSS and HTML changes. Javascript features may be required but resources are available to assist with this as well.

Familiarity and expertise with all technologies is not required. Strong Python skills and experience are a must though.

#### Specific Technologies Used

For the best primer see the [Developer Documentation](https://warehouse.readthedocs.io/development/) for Warehouse.

You can also see the [complete codebase](https://github.com/pypa/warehouse) on GitHub.

##### Backend

* [Python](https://www.python.org/) 3.6+
* [Pyramid](https://trypyramid.com)
* [PostgreSQL](https://www.postgresql.org) - [SQLAlchemy](https://docs.sqlalchemy.org/en/latest/) - [psycopg2](http://initd.org/psycopg/)
* [Redis](https://redis.io)

##### Frontend

Note: Our frontend is primarily static, these tools power the toolchain that creates our final assets.

* [Node](https://nodejs.org/en/)
* [Gulp](https://gulpjs.org)
* [SASS](https://sass-lang.com)
* [Stimulus](https://stimulusjs.org/)

### Project Management and Reporting

This project will be led and managed by the Python Software Foundation Director of Infrastructure and Changeset Consulting, LLC.

Regular meetings will be held to coordinate efforts between the project managers, backend developers, and frontend developers.

Status reporting during these meetings as well as regular summaries will be required. Additionally, participation on the [public issue tracker](https://github.com/pypa/warehouse/issues) and submission of changes via [code review](https://github.com/pypa/warehouse/pulls) for the project will be required.
