# PyPI Quarter 4 2019 Request for Information

The [Python Software Foundation](https://python.org/psf-landing) [Packaging Working Group](https://www.python.org/psf/committees/#packaging-work-group) has [received a grant](https://pyfound.blogspot.com/2018/12/upcoming-pypi-improvements-for-2019.html) from [Facebook Research](https://research.fb.com) to implement advanced security features for PyPI.

[PyPI](https://pypi.org) is a foundational component of the [Python](https://python.org) ecosystem and broader computer software and technology landscape. This project aims to improve the security of PyPI for all users worldwide, whether they are direct users like project maintainers and [`pip install`](https://pip.pypa.io/en/stable/)ers or indirect users. The impact of this work will be to implement long-desired security features for the service (see below).

We plan to begin the project in Quarter 4 of 2019. Because of the size of the project, funding has been allocated to secure one or more contractors to complete the development, testing, verification, and assist in the rollout of necessary features.

Please read this RFI and respond to let us know if you have questions, or may be interested in applying to work on the project.

## Timeline

|Date|Milestone|
|---|---|
|August 23|Request for Information period opens.|
|September 6|Request for Information period closes.|
|September 16|Request for Proposal period opens. (10 days after RFI close)|
|October 8|Request for Proposal period closes. (3 weeks after RFP open)|
|October 22|Date proposals will have received a decision. (2 weeks after RFP close)|
|November 31|Contracts for accepted proposals should be finalized.|
|December 1|Contract work commences.|

### Register Interest

To receive notification when our Request for Information period closes and the Request for Proposals period opens, please [register your interest here](https://forms.gle/ToVjmwna2wuqAbqG8).

## What is the Request for Information period?

**A Request for Information (RFI)** is a process intended to allow us (the Python Software Foundation), the Python community, and potential contractors to openly share information, requirements, and ideas to improve the scope and definition of the project at hand.

This window allows us to discuss open questions to direct of key features, explore prior art, and refine existing scope.

We hope that it will help potential contractors better understand the work to be completed and develop better-specified proposals. Additionally, we hope that the open nature of our RFI will expose the project to multiple perspectives, and potentially help shape the direction for some choices in the project.

After the RFI period closes, we will use the results of the process to prepare and open a **Request for Proposals (RFP)** to solicit proposals from contractors to complete the work.

**Note**: We may update this Request For Information document to reflect what we learn during the process. The canonical version and history is available [here](https://github.com/python/request-for/blob/master/2019-Q4-PyPI/RFI.md).

## How do I participate?

### Code of Conduct

This process requires that participants understand and adhere to the [Python Community Code of Conduct](https://www.python.org/psf/codeofconduct/) and [Python Packaging Authority Code of Conduct](https://www.pypa.io/en/latest/code-of-conduct/).

### Venue

We will conduct our RFI on the [Python Community Discussion Forum](https://discuss.python.org/c/python-software-foundation/) **Category TBD**.

Participants will need to create an account in order to propose new topics of discussion or respond to existing topics.

All discussions will remain public and available for review by potential proposal authors who do not wish to or cannot create an account to participate directly.

### Moderation

The RFI will be moderated by the Python Software Foundation Director of Infrastructure as well as existing community contributors to the PyPI project.

We will answer questions as promptly as possible during US/Eastern business hours and business days. If possible, community contributors may answer questions or moderate the forum outside those hours.

Moderators of the RFI may merge, edit, or discard topics or responses in some circumstances.

* Merge: If a given topic is a duplicate or highly similar to an existing topic.
* Edit: If a given response or topic is inaccurate or in conflict with our Code of Conduct.
* Discard: If a given response or topic is outside the scope of the RFI or discussion, or is an egregious/intentional violation of our Code of Conduct.

## Scope

This Request for Information is seeking **software developers** to design, implement, test, verify, and assist in the rollout of the following features to the codebase that powers [PyPI](https://pypi.org/).

- Verifiable cryptographic signing of artifacts ([PEP 458](https://www.python.org/dev/peps/pep-0458/)/[TUF](https://theupdateframework.github.io) or simiilar)
- Technical infrastructure and methods for automated detection of malicious package uploads
- Continuation of high priority improvements to previous security work on API Tokens and Multi-Factor authentication
- Documentation for above features

### Open Questions

#### Verifiable Cryptographic Signing of Artifacts

[PEP 458](https://www.python.org/dev/peps/pep-0458/) and [PEP 480](https://www.python.org/dev/peps/pep-0480/) were authored to propose implementation of [The Update Framework](https://theupdateframework.github.io) on [PyPI](https://pypi.org/) to allow end users to verify the integrity of packages downloaded from PyPI.

We are hoping that this RFI will allow the community, experts, and potential contractors to explore prior art in other package repositories, and discuss potential solutions for PyPI. This feedback will allow the PSF to decide what solution to request in our Request for Proposals.

Key discussion points are:

- Acceptance criteria for the community
- Implementation feasibility for PyPI
- Future maintainability and support requirements from PyPI administrators
- Security and operational efficacy of proposed solutions

#### Automated Detection of Malicious Uploads

[PyPI](https://pypi.org/) adds tens of thousands of new releases across the projects hosted in the repository and thousands of new projects monthly.

There are regular ongoing attempts by bad actors to upload releases and artifacts that include malicious payloads either in [`setup.py` files](https://www.bleepingcomputer.com/news/security/python-package-installation-can-trigger-malicious-code/) or within the package contents itself. Additionally, spam and scam artists sometimes attempt to create projects that include references and links to deceive search indexes and users.

The moderation capacity of the PyPI team is limited and currently relies on reports from the community to address malicious package uploads and spam/scam postings on the site.

We are hoping that this RFI will allow the community, experts, and potential contractors to explore prior art in other package repositories, and discuss potential solutions for PyPI. This feedback will allow the PSF to decide what solution to request in our Request for Proposals.

Key discussion points are:

- Acceptance criteria for the PyPI maintainers and moderators
- Methods for detection of malicious content
- Implementation feasibilty for PyPI and associated scalability

#### Continuations of API Token and Multi-Factor Authentication Work

A previous grant from the Open Technology Fund allowed the PSF to fund [work implementing multi-factor authentication and scoped upload API tokens on PyPI](https://github.com/pypa/warehouse/milestone/13). During the cryptographic signing and malicious upload detection work, we may discover requirements for further improvements in PyPI's MFA or API tokens.

## Estimated Budgets and Caps

**Budgets and caps** are provided to help contractors in preparing their proposals.

Budgets are PSF's estimates, and caps are based on the funding commitment that we have received.

Caps are provided to indicate that we understand that some features may require more funds than our estimated budget. Proposals may go over budget up to the cap for one feature, but fall under budget for another.

These values may change as a result of our RFI process.

Estimates and caps in United States dollars.

|Task|TBD Budget|TBD Cap|
|---|---|---|
|Verifiable cryptographic signing of artifacts|$15,750|$18,500|
|Automated detection of malicious uploads|$15,750|$18,500|
|Continuations of API token and multi-factor authentication work|$7,800|$9800|
|Documentation for above features|$2700|$5,200|
|Total|not applicable|$52,000|

**These estimates are To Be Determined as a result of the RFI**

## Expectations and Requirements

### Timeline

This project is intended to be completed over a three to five month period beginning November 2019.

### Technology

The codebase behind PyPI is called [Warehouse](https://github.com/pypa/warehouse) and is licensed under the [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0). All work submitted or dependencies added must be compliant with this license.

The backend codebase is in Python with a CSS, HTML, and JavaScript frontend (using the [Stimulus](https://stimulusjs.org/) framework).

Potential proposers should be comfortable with Python and may need to implement some features or views for the frontend, but will have support from an additional contractor focused on user interface and user experience design to implement CSS and HTML changes. JavaScript features may be required but resources are available to assist with this as well.

Familiarity and expertise with all technologies is not required. Strong Python skills and experience are a must, though.

#### Specific Technologies Used

For the best primer, see the [developer documentation](https://warehouse.readthedocs.io/development/) for Warehouse.

You can also see the [complete codebase](https://github.com/pypa/warehouse) on GitHub.

##### Backend

* [Python](https://www.python.org/) 3.6+
* [Pyramid](https://trypyramid.com)
* [PostgreSQL](https://www.postgresql.org) - [SQLAlchemy](https://docs.sqlalchemy.org/en/latest/) - [psycopg2](http://initd.org/psycopg/)
* [Redis](https://redis.io)

##### Frontend

Note: Our frontend is primarily static; these tools power the toolchain that creates our final assets.

* [Node](https://nodejs.org/en/)
* [Gulp](https://gulpjs.org)
* [SASS](https://sass-lang.com)
* [Stimulus](https://stimulusjs.org/)

### Project Management and Reporting

This project will be led and managed by the Python Software Foundation Director of Infrastructure and potentially an external project manager.

Regular meetings will be held to coordinate efforts among the project managers, backend developers, frontend developers, and UX designer.

Oral or textual status reporting during these meetings, as well as regular textual summaries of current status, will be required. Additionally, participation on the [public issue tracker](https://github.com/pypa/warehouse/issues) and submission of changes via [code review](https://github.com/pypa/warehouse/pulls) for the project will be required.
