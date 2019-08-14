# PyPI Quarter 4 2019 Request for Information

The [Python Software Foundation](https://python.org/psf-landing) [Packaging Working Group](https://www.python.org/psf/committees/#packaging-work-group) has [recieved a grant](https://pyfound.blogspot.com/2018/12/upcoming-pypi-improvements-for-2019.html) from [Facebook Research](https://research.fb.com) to implement advanced security features for PyPI.

[PyPI](https://pypi.org) is a foundational component of the [Python](https://python.org) ecosystem and broader computer software and technology landscape. This project aims to improve the security PyPI for all users worldwide, whether they are direct users like project maintainers and [`pip install`](https://pip.pypa.io/en/stable/)ers or indirect users. The impact of this work will be to implement long desired security features for the service.

We plan to begin the project in Quarter 4 of 2019. Because of the size of the project, funding has been allocated to secure one or more contractors to complete the development, testing, verification, and assist in the rollout of necessary features.

## Timeline

|Date|Milestone|
|---|---|
|TBD|Request for Information period opens.|
|TBD|Request for Information period closes.|
|TBD|Request for Proposal period opens. (? weeks after RFI close)|
|TBD|Request for Proposal period closes. (? days after RFP open)|
|TBD|Date proposals will have recieved a decision. (? weeks after RFP close)|
|TBD|Contracts for accepted proposals should be finalized.|
|TBD|Contract work commences.|

### Register Interest

To receive notification when our Request for Information period closes and the Request for Proposals period opens, please [register your interest here](https://forms.gle/ToVjmwna2wuqAbqG8).

## What is the Request for Information period?

A Request for Information (RFI) is a process intended to allow us (The Python Software Foundation), the Python community, and potential contractors to openly share information, requirements, and ideas to improve the scope and definition of the project at hand.

This window allows for discussion on open questions for the direction of key features, exploration of prior art, and refinement of existing scope.

We hope that it will help potential contractors better understand the work to be completed and develop better specified proposals. Additionally we hope that the open nature of our RFI will expose the project to multiple perspectives and potentially help shape the direction for some choices in the project.

After the RFI period closes, we will use the results of the process to prepare and open a Request for Proposals to solicit proposals from contractors to complete the work.

**Note**: This Request For Information document may be updated to reflect things that we learn during the process. The canonical version and history is available [here](https://github.com/python/request-for/blob/master/2019-Q4-PyPI/RFI.md).

## How do I participate?

### Code of Conduct

This process requires that participants understand and adhere to the [Python Community Code of Conduct](https://www.python.org/psf/codeofconduct/) and [Python Packaging Authority Code of Conduct](https://www.pypa.io/en/latest/code-of-conduct/).

### Venue

Our RFI will be conducted on the [Python Community Discussion Forum](https://discuss.python.org/c/python-software-foundation/) **Category TBD**.

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

This Request for Information is seeking Developers to implement, test, verify, and assist in the rollout of the following features to the codebase that powers [PyPI](https://pypi.org/).

- Verifiable cryptographic signing of artifacts ([PEP 458](https://www.python.org/dev/peps/pep-0458/)/[TUF](https://theupdateframework.github.io) or simiilar)
- Technical infrastructure and methods for automated detection of malicious package uploads
- Continuation of high priority improvements to previous security work on API Tokens and Multi-Factor authentication
- User Interface and User Experience design to support above features
- User adoption planning and design for above features
- Documentaion for above features

### Open Questions

#### Verifiable Cryptographic Signing of Artifacts

[PEP 458](https://www.python.org/dev/peps/pep-0458/) and [PEP 480](https://www.python.org/dev/peps/pep-0480/) were authored to propose implementation of [The Update Framework](https://theupdateframework.github.io) on [PyPI](https://pypi.org/) to allow end users to verify the integrity of packages downloaded from PyPI.

We are hoping that this RFI will allow for exploration of prior art in other package repositories and discussion of potential solutions for PyPI. This feedback from the community, experts, and potential contractors will allow for a decision to be made on what solution is requested in our Request for Proposals.

Key discussion points are:

- Acceptance criteria for the community
- Implementation feasibility for PyPI
- Future maintaibility and support requirements from PyPI administrators
- Security and operational efficacy of proposed solutions

#### Automated Detection of Malicious Uploads

[PyPI](https://pypi.org/) adds tens of thousands of new releases across the projects hosted in the repository and thousands of new projects monthly.

There are regular ongoing attempts by bad actors to upload releases and artifacts that include malicious payloads either in [`setup.py` files](https://www.bleepingcomputer.com/news/security/python-package-installation-can-trigger-malicious-code/) or within the package contents itself. Additionally spam and scam artists sometimes attempt to create projects that include references and links to decieve search indexes and users.

The moderation capacity of the PyPI team is limited and currently relies on reports from the community to address malicious package uploads and spam/scam postings on the site.

We are hoping that this RFI will allow for exploration of prior art in other venues and discussion of potential solutions for PyPI. This feedback from the community, experts, and potential contractors will allow for a decision to be made on what solution is requested in our Request for Proposals.

Key discussion points are:

- Acceptance criteria for the PyPI maintainers and moderators
- Methods for detection of malicious content
- Implementation feasibilty for PyPI and associated scalability

## Estimated Budgets and Caps

Budgets and Caps are provided to help contractors in preparing their proposals. 

Budgets are estimates created during the formation of our proposal to Open Technology Fund and Caps are based on the funding commitment that we have received.

Caps are provided so that it is understood that some features may require more funds than our estimated Budget. Proposals may go over Budget up to the Cap for one feature but fall under Budget for another.

These values may change as a result of our RFI process.

Estimates and Caps in United States Dollars.

**These estimates are To Be Determined as a result of the RFI**


## Expectations and Requirements

### Timeline

This project is intended to be completed over a three to five month period beginning November 2019.

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

This project will be led and managed by the Python Software Foundation Director of Infrastructure and potentially an external Project Manager.

Regular meetings will be held to coordinate efforts between the project managers, backend developers, and frontend developers.

Status reporting during these meetings as well as regular summaries will be required. Additionally, participation on the [public issue tracker](https://github.com/pypa/warehouse/issues) and submission of changes via [code review](https://github.com/pypa/warehouse/pulls) for the project will be required.
