# pip 2020 Request for Proposals

**This RfP is closed; we are currently reviewing submissions.**

The [Python Software Foundation](https://python.org/psf-landing) [Packaging Working Group](https://www.python.org/psf/committees/#packaging-work-group) is receiving funding (sources embargoed till late 2020) to work on the design, implementation, and rollout of pip's next-generation dependency resolver.

[pip](https://pip.pypa.io) is the official [package installer](https://packaging.python.org/en/latest/current/) for Python. pip aims to make it easy for the millions of people who use Python to download and install Python libraries and applications (open source and closed source, source and binary, globally and within isolated virtual environments). pip is bundled with Python installations, and is available as a standalone download. It is bundled with the Python runtime itself, and is available as a standalone download which bootstraps and installs itself. To a first approximation, the entire ecosystem of millions of Python software projects depends on pip. Thus, pip is a foundational component of the [Python](https://python.org) ecosystem and broader computer software and technology landscape.

This project aims to complete the design, implementation, and rollout of pip's next-generation dependency resolver. This will lower the barriers to installing Python software, empowering users to get a version of a package that works. It will also lower the barriers to _distributing_ Python software, empowering developers to make their work available in an easily reusable form. ([Here's a quick Twitter thread giving context on why this work is important.](
https://twitter.com/di_codes/status/1193980331004743680))

We plan to begin the project in Quarter 1 of 2020. Because of the size of the project, funding has been allocated to secure *two contractors*, a _senior developer_ and an _intermediate developer_, to work on development, testing and building test infrastructure, code review, bug triage, and assisting in the rollout of necessary features.

Please read this RFP and respond to let us know if you have questions, or submit a proposal if you are interested in performing the work for one of these contracts.

 - [Timeline](#timeline)
 - [What is an RfP?](#what-is-the-request-for-proposals-period)
 - [How do I submit a proposal?](#how-do-i-submit-a-proposal)
 - [Evaluation criteria](#evaluation-criteria)
 - [Scope of work and timeline](#scope) for [Role 1: Senior Developer](#role-1-senior-developer) and [Role 2: Intermediate Developer](#role-2-intermediate-developer)
 - [Expectations and requirements](#expectations-and-requirements), including technologies to use and project management/reporting to expect
 - [Questions, concerns, and feedback](#questions-concerns-or-feedback)

## Timeline

|Date|Milestone|
|---|---|
|November 11|Request for Proposal period opened.|
|November 22|Request for Proposal period closed.|
|November 27|Date proposals will have received a preliminary decision. **Note: due to the large number of applicants, we will not be able to provide a final decision by November 27th, but will work to provide a preliminary status by November 27th, and final decisions to all applicants by December 4th.**|
|December 31|Latest date for contracts for accepted proposals to be finalized.|
|January 2|Latest date for contract work to commence.|


## What is the Request for Proposals period?

**A Request for Proposals (RFP)** is a process intended to allow us (the Python Software Foundation) to collect proposals from potential contractors and select contractor(s) best suited to fulfill the specified work.

After the RFP period closes we will evaluate the received proposals based on the [evaluation criteria](#evaluation-criteria), seek clarification from proposers as necessary, and select one or more contractors to complete the work specified in the [scope section](#scope).

**Note**: This Request For Proposal document may be updated to reflect things that we learn during the process. The canonical version and history is available [here](https://github.com/python/request-for/blob/master/2020-pip/RFP.md).

## How do I submit a proposal?

Submit your proposal as a [Portable Document Format (PDF)](https://en.wikipedia.org/wiki/PDF) file via email to [Sumana Harihareswara \<sumanah@pypi.org\>](mailto:sumanah@pypi.org), contract project manager working with the Python Software Foundation. Please begin your subject line with "RfP Q1-2020".

Proposals must be submitted before the end of the day **November 22, 2019 [AoE](https://www.timeanddate.com/time/zones/aoe)** (2019-11-23T12:00:00Z).

You can revise an already-submitted proposal by sending a follow-up email before the end of the day November 22nd. Please don't overuse this -- one or two revisions at most, please.

### Elements of proposal

A submission must, at a minimum, include the following elements:

- Description of the team or person that will perform the work.
  - General overview and names of individuals.
  - Experience with [relevant technologies](#specific-technologies-used). This could be a copy of your CV/résumé.
  - Who would the PSF be contracting with? Are you an individual freelancer or a firm/corporation? If you're subcontracting, then to whom?
  - Free/open source software experience?

- Agreement to [project management and reporting](#project-management-and-reporting) requirements.

- What Role(s) are you proposing for?
  - Please propose for Role 1, Role 2, or both.

- Examples of similarly-complex projects completed previously.
  - Referencing contributions to free/open source projects is encouraged.

- Agreement to our project timeline for the Role(s) proposer is applying for (proposers may suggest adjustments based on your availability).

In total, we expect your proposal to be 3-6 pages long, but feel free to go under 3 or over 6 pages if you feel it is appropriate. We expect an individual applying for a single role would spend at most 1-2 hours preparing a proposal, and that companies and teams would spend at most 4-5 hours preparing a proposal.

## Evaluation criteria

### Potential pass/fail:

 - Contains all elements specified in the [elements of the proposal](#elements-of-proposal).
 - Proposal is detailed enough to properly assess further criteria.
 - Formatting and submission requirements:
   - Portable Document Format (PDF)
   - Emailed to [sumanah@pypi.org](mailto:sumanah@pypi.org) by **November 22, 2019 [AoE](https://www.timeanddate.com/time/zones/aoe)** (2019-11-23T12:00:00Z).

### Experience and competence

- Does the proposal demonstrate relevant experience necessary to complete the work?
- Is there demonstrable experience with enough of the [relevant technologies](#specific-technologies-used) for each Role to support timelines?
- Do the examples of similarly complex projects and any references to past free/open source software contributions indicate competence?

### Process and timeline

- Do the proposers agree to the [project management and reporting](#project-management-and-reporting) requirements?
- Do the proposers agree to the project timeline for the role? Are deviations from our timeline explained and supported?

## Scope

This Request for Proposals is seeking **Python developers** to implement, test, verify, and assist in the rollout of the improved dependency resolver to the Python package installer tool [pip](https://pip.pypa.io).

Discussions leading to this scope can be read in:
* [this GitHub issue about the rollout of the new resolver](https://github.com/pypa/pip/issues/6536)
* [this summary and list of issues related to the resolver](https://wiki.python.org/psf/Fundable%20Packaging%20Improvements#Finish_dependency_resolver_for_pip)

### Role 1: Senior developer

#### Summary and budget

Development: USD $116,375 for 665 hours, at USD $175 per hour

We seek a senior Python developer for the following tasks, starting in mid-December 2019 or early January 2020, till the end of May 2020.

This work can be done remotely from anywhere.

- Onboarding and reviewing open issues and pull requests, to organize materials for project plan
- Refactoring existing build logic per [overview in this blog post](https://pradyunsg.me/blog/2019/08/06/pip-update-2/)
- Collaborating with downstreams and users about config flags and transition schedules
- Introducing abstractions defined in prototype resolver and fixing bugs found in alpha testing

#### Timeline

##### Foundational work (Phase I): mid-December or early January till end of March 2020

December and January:
- Onboard and review open issues and pull requests: 70 hours (probably 2 fulltime weeks at 35 hrs/week)
- Continue refactoring existing build logic: 35 hours (probably 1 fulltime week)

February:
- Finish refactoring existing build logic: 105 hours
- Collaborate with downstreams and users about config flags and transition schedules: 35 hours

March:
- Build test infrastructure: 70 hours (probably 2 fulltime weeks at 35 hrs/week)
- Collaborate with downstreams and users about config flags and transition schedules: 35 hours
- Introduce the abstractions defined in prototype resolver while doing alpha testing: 35 hours


##### Resolver work (Phase II): April and May 2020

April:
- Improve test infrastructure and testing plan: 35 hours
- Introduce further abstractions from prototype resolver and fix bugs found in alpha testing: 105 hours (probably 3 fulltime weeks at 35 hrs/week)
- Ideally, attend [PyCon North America](https://us.pycon.org/2020/) (we are seeking funding for travel and lodging)

May:
- Improve test infrastructure: 35 hours
- Introduce further abstractions from prototype resolver and fix bugs found in alpha testing: 105 hours (probably 3 fulltime weeks at 35 hrs/week)


### Role 2: Intermediate developer

#### Summary and budget

Development: USD $103,700, for 670 hours at USD $150 per hour, plus USD $1600 for onboarding travel and USD $1600 for [PyCon](https://us.pycon.org/2020/) travel

We seek an intermediate-to-senior Python developer for the following tasks, starting in early January 2020, till the end of December 2020.

This work can be done remotely from anywhere.

- onboard
- do bug triage and code review
- write test cases
- test lead developers' work
- build test infrastructure
- investigate and fix bugs
- write the raw material for documentation to help future maintainers onboard better

Our funding also covers travel for onboarding in January, so this person can meet and work with a lead pip developer, and for travel to [PyCon North America in April](https://us.pycon.org/2020/).

#### Timeline

##### January-February 2020 (foundational work, Phase I)

This preparatory work will ensure that the developer (and user experience researcher/designer) have the tools they need to work on the resolver in the second phase.

January:
 - Onboard and review open issues and pull requests: 70 hours (probably 2 fulltime weeks of 35 hrs each) (part of this work to be done during a 1-week onsite visit, lodging and travel covered)
   - A current maintainer (specific person and location to be determined) will teach and train the new developer via architectural overview, setup and configuration, pair programming, narrative feature tours, code reviews, meta-review of the developer's code reviews, and planning for the resolver work. We aim to use [this guide](https://modelviewculture.com/pieces/software-in-person) to make this time productive, and work to ensure a closer working relationship between the developers, a granular project plan for the next few months, raw material for future documentation, and an increase in development and maintainer skills for our developer.
   - Review existing status reports on the resolver work, such as [maintainer Pradyun Gedam's November 2019 update](https://pradyunsg.me/blog/2019/11/06/oss-update-5/)

February:
 - Review open issues and PRs, write developer documentation: 70 hrs (probably 2 fulltime weeks of 35 hrs each)
   - Review and triage many of our open issues and open pull requests on pip
   - Documentation work: for example, improving the [architecture overview](https://pip.pypa.io/en/stable/development/architecture/) and the ["how to triage pip bugs" guide](https://pip.pypa.io/en/stable/development/issue-triage/)


##### March-May 2020 (Resolver, Phase II)

Work on the pip resolver by writing test cases/testing plan, testing maintainers' refactoring and new features, investigating and fixing bugs found in beta testing, and working with PSF on test infrastructure

March:
- Work on pip resolver; writing test cases and starting a testing plan, testing maintainers' refactoring and new features, and working with PSF on test infrastructure: 140 hours (4 fulltime weeks of 35 hrs each)

April:
 - Work on pip resolver; writing test cases and improving a testing plan, testing maintainers' refactoring and new features, and working with PSF on test infrastructure: 140 hours (4 fulltime weeks of 35 hrs each)
   - (Part of this work to be done during [PyCon North America](https://us.pycon.org/2020/), one week, lodging and travel covered)

May:
 - Investigate and fix bugs found in beta testing, and improve and use testing plan: 40 hours (probably 4 weeks at 10 hours/week)
   - We aim in this month to get pip's resolver feature prepared for release in pip 20.2 in July. (Per the quarterly release cadence for pip, unforeseen difficulties may delay till 20.3 in the next quarter.)

#### June-December 2020 (Maintenance and Sustainability, Phase III)
Once we have finished rolling out the resolver, the contractor will:
- Keep up with the pip code and issue review queue for 10 hours per week, thus releasing a key bottleneck and enabling existing maintainers to make progress on key architectural features
- Help new contributors develop into continuing contributors
- Help existing contributors grow into co-maintainers

June:
- Review and respond to code contributions and new issues: 40 hours (probably 4 weeks at 10 hours/week)

July:
- _vacation, unpaid_

August:
- Review and respond to code contributions and new issues: 40 hours (probably 4 weeks at 10 hours/week)

September:
- Review and respond to code contributions and new issues: 40 hours (probably 4 weeks at 10 hours/week)

October:
- Review and respond to code contributions and new issues, and possibly participate in user experience training: 40 hours (probably 4 weeks at 10 hours/week)

November:
- Review and respond to code contributions and new issues: 30 hours (probably 3 weeks at 10 hours/week)

December:
- Review and respond to code contributions and new issues: 20 hours (probably 2 weeks at 10 hours/week)

## Expectations and Requirements

### Project Timeline

This project is intended to be completed over three phases, totalling a little over one year, starting mid-December 2019 or early January 2020.

Role 1 and Role 2 have different timelines; see those roles for details.

### Technology

The [pip codebase](https://github.com/pypa/pip) is licensed under the [MIT License](https://github.com/pypa/pip/blob/master/LICENSE.txt). All work submitted or dependencies added must be compliant with this license.

The codebase is in Python. The pip documentation is built using reStructuredText and Sphinx.

Potential proposers should be comfortable with Python, and will have support from an additional contractor focused on user interface and user experience design to advise on command line experience improvements.

For Role 1 (Senior developer): Familiarity and expertise with the pip codebase, or with a Python packaging/distribution toolchain codebase, is required. Strong Python skills, and experience contributing to Python packaging/distribution tools, are required.

For Role 2 (Intermediate developer): Strong Python skills and experience are a must. Some experience working on Python packaging/distribution tools is required. Experience with some automated testing tools (not necessarily the ones we use) are strongly desired. Familiarity and expertise with all testing infrastructure technologies mentioned below is not required.

#### Specific Technologies Used

pip is a Python program that runs on client computers as part of [the Python packaging and distribution toolchain](https://packaging.python.org/). Understanding of and familiarity with how Python packaging works, how packages are built and installed, and so on, will be helpful.

##### pip codebase

For the best primer, see the [developer documentation](https://pip.pypa.io) for pip.

You can also see the [complete codebase](https://github.com/pypa/pip) on GitHub.

 - [Python](https://www.python.org/) 2.7 and 3.5+ on Linux, Mac OS, and Windows
 - [pytest](http://pytest.readthedocs.io/)
 - [tox](https://tox.readthedocs.io/en/latest/)
 - [Sphinx](http://www.sphinx-doc.org/)

##### Testing Infrastructure

pip has [an extensive continuous integration test suite](https://pip.pypa.io/en/latest/development/ci/). This test suite is built using:

- [Python](https://www.python.org/) 2.7 and 3.5+ on Linux, Mac OS, and Windows
- [tox](https://tox.readthedocs.io/en/latest/)
- [nox](https://nox.thea.codes/en/stable/)
- [pre-commit](https://pre-commit.com)
- [pytest](http://doc.pytest.org/en/latest/)

as well as many other associated Python testing, automation, and code quality tools.

Components of the test suite are executed using multiple services including:

- [Azure Pipelines](https://docs.microsoft.com/en-us/azure/devops/pipelines/index?view=azure-devops)
- [GitHub Actions](https://help.github.com/en/actions/automating-your-workflow-with-github-actions/about-github-actions)
- [AppVeyor](https://www.appveyor.com/docs/)
- [TravisCI](https://docs.travis-ci.com)
- [Read the Docs](https://docs.readthedocs.io/en/stable/index.html)

### Project Management and Reporting

This project will be led and managed by the Python Software Foundation Director of Infrastructure (Ernest W. Durbin III) and an external project manager.

Regular meetings (at most 30 minutes each, 4 times per month) will be held to coordinate efforts among the project managers, developers, and UX researcher/designer.

Oral or textual status reporting during these meetings, as well as regular brief textual summaries of current status (such as a sentence or two, a few times per week, via Slack or Zulip), will be required. Additionally, participation on the [public issue tracker](https://github.com/pypa/warehouse/issues) and submission of changes via [code review](https://github.com/pypa/warehouse/pulls) for the project will be required.

## Questions, Concerns, or Feedback

Please contact [Sumana Harihareswara \<sumanah@pypi.org\>](mailto:sumanah@pypi.org), contract project manager working with the Python Software Foundation. Please begin your subject line with "RfP Q1-2020".

