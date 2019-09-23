# PyPI Quarter 4 2019 Request for Proposals

The [Python Software Foundation](https://python.org/psf-landing) [Packaging Working Group](https://www.python.org/psf/committees/#packaging-work-group) has [received a grant](https://pyfound.blogspot.com/2018/12/upcoming-pypi-improvements-for-2019.html) from [Facebook Research](https://research.fb.com) to implement advanced security features for PyPI.

[PyPI](https://pypi.org) is a foundational component of the [Python](https://python.org) ecosystem and broader computer software and technology landscape. This project aims to improve the security of PyPI for all users worldwide, whether they are direct users like project maintainers and [`pip install`](https://pip.pypa.io/en/stable/)ers or indirect users. The impact of this work will be to implement long-desired security features for the service (see below).

We plan to begin the project in Quarter 4 of 2019. Because of the size of the project, funding has been allocated to secure one or more contractors to complete the development, testing, verification, and assist in the rollout of necessary features.

Please read this RFP and respond to let us know if you have questions, or submit a proposal if you are interested in performing the work.

## Timeline

|Date|Milestone|
|---|---|
|August 28|Request for Information period opened.|
|September 18|Request for Information period closed.|
|September 24|Request for Proposal period opened.|
|October 16|Request for Proposal period closes.|
|October 29|Date proposals will have received a decision.|
|November 30|Contracts for accepted proposals should be finalized.|
|December 2|Contract work commences.|


## What is the Request for Proposals period?

**A Request for Proposals (RFP)** is a process intended to allow us (the Python Software Foundation)to collect proposals from potential contractors and select contractor(s) best suited to fulfill the specified work.

After the RFP period closes we will evaluate the received proposals based on the [evaluation criteria](#evaluation-criteria), seek clarification from proposers as necessary, and select one or more contractors to complete the work specified in the [scope section](#scope).

**Note**: This Request For Proposal document may be updated to reflect things that we learn during the process. The canonical version and history is available [here](https://github.com/python/request-for/blob/master/2019-Q1-PyPI/RFP.md).

## How do I submit a proposal?

Proposals should be submitted as [Portable Document Format (PDF)](https://en.wikipedia.org/wiki/PDF) files via email to [ewdurbin@pyfound.org](mailto:ewdurbin@pyfound.org).

Proposals must be submitted before the end of the day **October 16, 2019 [AoE](https://www.timeanddate.com/time/zones/aoe)** (2019-10-16T12:00:00Z).

### Elements of proposal

A submission must, at a minimum, include the following elements:

- Description of the team that will perform the work.
  - General overview and names of individuals.
  - Experience with [relevant technologies](#specific-technologies-used).
  - Freelance or firm? Incorporation? Subcontracting?
  - Free/Open Source Software experience?

- Agreement to [project management and reporting](#project-management-and-reporting) requirements.

- What Milestone(s) are you proposing for?
  - We recommend proposing for all of the work in scope of Milestone 1, Milestone 2, or both.

- Examples of similarly-complex projects completed previously.
  - Referencing contributions to Free/Open Source projects is encouraged.

- Project timeline estimates by milestone and task. These timelines should fit within our [project timeline](#project-timeline), however proposers may suggest adjustments based on their availability.
  - Milestone 1 - Verifiable cryptographic signing of artifacts
  - Milestone 2 - Systems for Automated Detection of Malicious Uploads

- Project budget by milestone and task. Deviations from our [estimated budgets and caps](#estimated-budgets-and-caps) should be described and supported.
  - Milestone 1 - Verifiable cryptographic signing of artifacts
  - Milestone 2 - Systems for Automated Detection of Malicious Uploads

In total, we expect your proposal to be 5-10 pages long, but feel free to go under 5 or over 10 pages if you feel it is appropriate.

## Evaluation criteria

### Potential pass/fail:

 - Contains all elements specified in the [elements of the proposal](#elements-of-proposal).
 - Proposal is detailed enough to properly assess further criteria.
 - Formatting and Submission requirements:
   - Portable Document Format (PDF)
   - Emailed to [ewdurbin@pyfound.org](mailto:ewdurbin@pyfound.org) by **October 16, 2019 [AoE](https://www.timeanddate.com/time/zones/aoe)** (2019-10-16T12:00:00Z)

### Experience and competency

- Does the proposal demonstrate relevant experience necessary to complete the work?
- Is there demonstrable experience with enough of the [relevant technologies](#specific-technologies-used) for each Milestone to support timelines?
- Do the examples of similarly complex projects and any references to past Free/Open Source Software contributions indicate competency?

### Cost

- Does the budget proposed fit within our [estimated budgets and caps](#estimated-budgets-and-caps)?
- Are the milestone and task budgets reasonable and competitive?
- Are any deviations from the [estimated budgets and caps](#estimated-budgets-and-caps) well supported and explained?

### Process and timeline

- Do the proposers agree to the [project management and reporting](#project-management-and-reporting) requirements?
- Are the project timeline estimates within our [project timeline](#project-timeline)? Are deviations from our timeline explained and supported?

## Scope

This Request for Proposals is seeking **backend developers** to implement, test, verify, and assist in the rollout of the following features to the codebase that powers [PyPI](https://pypi.org/).

Discussions leading to these milestones can be read in the [forum for our Request for Information](https://discuss.python.org/c/python-software-foundation/pypi-q4-rfi).

### Milestone 1 - Verifiable cryptographic signing of artifacts

#### Summary

* Implementation of [PEP 458 once accepted](https://www.python.org/dev/peps/pep-0458/) to add integration of [The Update Framework](https://theupdateframework.github.io/) to PyPI
* Development of either a stand alone service or code in the [Warehouse codebase](https://github.com/pypa/warehouse) to create, sign, serve, and handle caching concerns for TUF metadata
* Development of necessary code in the [Warehouse codebase] to integrate TUF](https://theupdateframework.github.io/) metadata and signing

[Relevant background and context](https://github.com/pypa/warehouse/issues/5247)

#### Specific tasks

* Development of systems for generation and signing of metadata compliant with [TUF](https://theupdateframework.github.io/)
* Development of systems for serving signed metadata compliant with [TUF](https://theupdateframework.github.io/)
* Development of systems for appropriately caching and invalidation of caches for metadata service
* Documentation for Administrators of PyPI for handling key material and interacting with the systems
* Documentation for PyPI client libraries for sourcing and validating [TUF](https://theupdateframework.github.io/) metadata

**Note**: Implementation of support for TUF signing or verification in the Python packaging toolchain (e.g. setuptools, pip, twine, etc) is not in scope.

### Milestone 2 - Systems for Automated Detection of Malicious Uploads

#### Summary

* Development of infrastructure as either a standalone service or code in the [Warehouse codebase](https://github.com/pypa/warehouse) to automatically screen metadata and uploads to PyPI for malicious content via pluggable checks, reporting results to PyPI
* Development of necessary code in the [Warehouse codebase](https://github.com/pypa/warehouse) to store results of automated screening for administrator review

[Relevant background and context](https://github.com/pypa/warehouse/issues/5117)

#### Specific tasks

* Develop systems for running automated checks on new Projects, Release, and Release Files.
* Develop a pluggable system for development and deployment of new checks
* Implement database models to store check results relating to Projects, Releases, and Release Files from checks
* Implement Administrator views for reviewing results
* Documentation process for the development and submission of new checks

**Note**: Surfacing malware detection results to PyPI publishers and users via the Web User Interface or any API is not in scope.

## Estimated Budgets and Caps

**Budgets and caps** are provided to help contractors in preparing their proposals.

Budgets are PSF's estimates, and caps are based on the funding commitment that we have received.

Caps are provided to indicate that we understand that some features may require more funds than our estimated budget. Proposals may go over budget up to the cap for one feature, but fall under budget for another.

Estimates and caps in United States dollars.

|Task|TBD Budget|TBD Cap|
|---|---|---|
|Verifiable cryptographic signing of artifacts (approximately 4-5 weeks)|$25,000|$30,000|
|Automated detection of malicious uploads (approximately 3-4 weeks)|$20,000|$24,500|
|Documentation for above features|$3,000|$5,500|
|Total|not applicable|$65,000|

## Expectations and Requirements

### Project Timeline

This project is intended to be completed over a three to five month period beginning December 2019. Proposals with a shorter or longer timeline are acceptable if it is explained, and supported by estimated budget and costs.

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

## Questions, Concerns, or Feedback

Please contact [Ernest W. Durbin III \<ewdurbin@pyfound.org\>](mailto:ewdurbin@pyfound.org), Director of Infrastructure at the Python Software Foundation.