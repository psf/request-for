# PyPI Quarter 1 2019 Request for Information

The [Python Software Foundation](https://python.org/psf-landing) [Packaging Working Group](https://www.python.org/psf/committees/#packaging-work-group) has applied for and received a commitment from the [Open Technology Fund](https://www.opentech.fund) to fulfill a contract for their [Core Infrastructure Fund](https://www.opentech.fund/funds/core-infrastructure-fund/).

[PyPI](https://pypi.org) is a foundational component of the [Python](https://python.org) ecosystem and broader computer software and technology landscape. This project aims to improve the security and accessibility of PyPI for all users worldwide, whether they are direct users like project maintainers and [`pip install`](https://pip.pypa.io/en/stable/)ers or indirect users. The impact of this work will be highly visible and improve crucial features of the service.

We plan to begin the project in January 2019. Because of the size of the project, funding has been allocated to secure one or more contractors to complete the development, testing, verification, and assist in the rollout of necessary features.

## Timeline

|Date|Milestone|
|---|---|
|2018-10-30|Request for Information period opens.|
|2018-11-13|Request for Information period closes.|
|2018-11|Request for Proposal period opens. (1-2 weeks after RFI close)|
|2018-11|Request for Proposal period closes. (10 days after RFP open)|
|2018-12|Date proposals will have recieved a decision. (1-2 weeks after RFP close)|
|2019-12-31|Contracts for accepted proposals should be finalized.|
|2019-01|Contract work commences.|

### Register Interest

To receive notification when our Request for Information period closes and the Request for Proposals period opens, please [register your interest here](https://goo.gl/forms/Jx5aXUhwSgzqjGtl2).

## What is the Request for Information period?

A Request for Information (RFI) is a process intended to allow us (The Python Software Foundation) and potential contractors to openly share information to improve the scope and definition of the project at hand.

We hope that it will help potential contractors better understand the work to be completed and develop better specified proposals. Additionally we hope that the open nature of our RFI will expose the project to multiple perspectives and potentially help shape the direction for some choices in the project.

**Note**: This Request For Information document may be updated to reflect things that we learn during the process. The canonical version and history is available [here](https://github.com/python/request-for/blob/master/2019-Q1-PyPI/RFI.md).

## How do I participate?

### Code of Conduct

This process requires that participants understand and adhere to the [Python Community Code of Conduct](https://www.python.org/psf/codeofconduct/).

### Venue

Our RFI will be conducted on the [Python Community Discussion Forum](https://discuss.python.org/c/python-software-foundation/psf-pypi-rfi-q1-2019).
Participants will need to create an account in order to propose new topics of discussion or respond to existing topics.

All discussions will remain public and available for review by potential proposal authors who do not wish to or cannot create an account to participate directly.

### Moderation

The RFI will be moderated by the Python Software Foundation Director of Infrastructure as well as existing community contributors to the PyPI project.

Questions will be answered as promptly as possible during US/Eastern business hours and business days. If possible community contributors may answer questions or moderate the forum outside those hours.

Moderators of the RFI may merge, edit, or discard topics or responses in some circumstances.

* Merge: If a given topic is a duplicate or highly similar to an existing topic.
* Edit: If a given response or topic is inaccurate or in conflict with our Code of Conduct
* Discard: If a given response or topic is outside the scope of the RFI or discussion, or is an egregious/intentional violation of our Code of Conduct.

## Scope

This Request for Information is seeking Backend Developers to implement, test, verify, and assist in the rollout of the following features to the codebase that powers [PyPI](https://pypi.org/).

### Milestone 1 - Security development

#### Summary

* Support for two-factor authentication via [TOTP](https://tools.ietf.org/html/rfc6238) and [U2F/FIDO](https://fidoalliance.org/specifications/overview/).
* Application specific tokens scoped to individual users/projects (this will also cover adding token based login support to twine and setuptools)
* Advanced audit trail of user actions beyond the current journal (allowing publishers to track all actions taken by third party services on their behalf).

#### Specific Tasks

Multi-Factor Auth:

* Implement TOTP
* Implement U2F/FIDO
* Adding/Removing 2FA user flow
* Login w/ 2FA user flow API Keys

API Keys:

* Implement per-user API Keys
* Adding/removing User API keys flow
* Per-project API Keys
* Adding/removing Project API keys flow 

Audit Trail:

* Adding audits for user actions
* Admin view for auditing


### Milestone 2 - Accessibility and internationalization development

#### Summary

Accessibility audit and follow-on accessibility repair work, implementing localization and internationalization features and recruiting translators and integrating translations into PyPI.

#### Specific Tasks

Accessibility:

* Any backend features required to support making the codebase [WCAG 2.0 AA](https://www.w3.org/WAI/intro/wcag) compliant.

Localization:

* Implementing localization and internationalization features
* Choosing a localization framework compatible with [Pyramid](https://trypyramid.com/) and integrating it into our application
* Replacing hardcoded English messages with localized messages in browser and email templates
* Configuring integration with [Transifex](https://www.transifex.com/) or another localization platform

## Estimated Budgets and Caps

Budgets and Caps are provided to help contractors in preparing their proposals. 
Budgets are estimates created during the formation of our proposal to Open Technology Fund and Caps are based on the commitment that we have received.

Caps are provided so that it is understood that some features may require more funds than our estimated Budget. Proposals may go over Budget up to the Cap for one feature but fall under Budget for another.

These values may change as a result of our RFI process.

Estimates and Caps in United States Dollars.

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

### Timeline

This project is intended to be completed over a three month period beginning January 2019.

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
