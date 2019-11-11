# pip 2020 Request for Proposals

The [Python Software Foundation](https://python.org/psf-landing) [Packaging Working Group](https://www.python.org/psf/committees/#packaging-work-group) is receiving funding (sources embargoed till late 2020) to work on the design, implementation, and rollout of pip's next-generation dependency resolver.

[pip](https://pip.pypa.io) is the official [package installer](https://packaging.python.org/en/latest/current/) for Python. pip aims to make it easy for the millions of people who use Python to download and install Python libraries and applications (open source and closed source, source and binary, globally and within isolated virtual environments). pip is bundled with Python installations, and is available as a standalone download. It is bundled with the Python runtime itself, and is available as a standalone download which bootstraps and installs itself. To a first approximation, the entire ecosystem of millions of Python software projects depends on pip. Thus, pip is a foundational component of the [Python](https://python.org) ecosystem and broader computer software and technology landscape.

This project aims to complete the design, implementation, and rollout of pip's next-generation dependency resolver. This will lower the barriers to installing Python software, empowering users to get a version of a package that works. It will also lower the barriers to​ distributing ​Python software, empowering developers to make their work available in an easily reusable form.

We plan to begin the project in Quarter 1 of 2020. Because of the size of the project, funding has been allocated to secure *two contractors*, a senior developer and an intermediate developer, to work on development, testing and building test infrastructure, code review, bug triage, and assisting in the rollout of necessary features.

Please read this RFP and respond to let us know if you have questions, or submit a proposal if you are interested in performing the work for one of these contracts.

## Timeline

|Date|Milestone|
|---|---|
|November 11|Request for Proposal period opens.|
|November 22|Request for Proposal period closes.|
|November 27|Date proposals will have received a decision.|
|December 31|Latest date for contracts for accepted proposals to be finalized.|
|January 2|Latest date for contract work to commence.|


## What is the Request for Proposals period?

**A Request for Proposals (RFP)** is a process intended to allow us (the Python Software Foundation) to collect proposals from potential contractors and select contractor(s) best suited to fulfill the specified work.

After the RFP period closes we will evaluate the received proposals based on the [evaluation criteria](#evaluation-criteria), seek clarification from proposers as necessary, and select one or more contractors to complete the work specified in the [scope section](#scope).

**Note**: This Request For Proposal document may be updated to reflect things that we learn during the process. The canonical version and history is available [here](https://github.com/python/request-for/blob/master/2020-pip/RFP.md).

## How do I submit a proposal?

Proposals should be submitted as [Portable Document Format (PDF)](https://en.wikipedia.org/wiki/PDF) files via email to [ewdurbin@pyfound.org](mailto:ewdurbin@pyfound.org).

Proposals must be submitted before the end of the day **November 22, 2019 [AoE](https://www.timeanddate.com/time/zones/aoe)** (2019-11-22T12:00:00Z).

You can revise an already-submitted proposal by sending a follow-up email before the end of the day November 22nd. Please don't overuse this -- one or two revisions at most, please.

### Elements of proposal

A submission must, at a minimum, include the following elements:

- Description of the team or person that will perform the work.
  - General overview and names of individuals.
  - Experience with [relevant technologies](#specific-technologies-used). This could be a copy of your CV/résumé.
  - Freelance or firm? Incorporation? Subcontracting?
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
   - Emailed to [ewdurbin@pyfound.org](mailto:ewdurbin@pyfound.org) by **November 22, 2019 [AoE](https://www.timeanddate.com/time/zones/aoe)** (2019-11-22T12:00:00Z).

### Experience and competency

- Does the proposal demonstrate relevant experience necessary to complete the work?
- Is there demonstrable experience with enough of the [relevant technologies](#specific-technologies-used) for each Role to support timelines?
- Do the examples of similarly complex projects and any references to past Free/Open Source Software contributions indicate competence?

### Process and timeline

- Do the proposers agree to the [project management and reporting](#project-management-and-reporting) requirements?
- Do the proposers agree to the project timeline for the role? Are deviations from our timeline explained and supported?

## Scope

This Request for Proposals is seeking **Python developers** to implement, test, verify, and assist in the rollout of the improved dependency resolver to the Python package installer tool [pip](https://pip.pypa.io).

Discussions leading to this scope can be read in:
* [this GitHub issue about the rollout of the new resolver](https://github.com/pypa/pip/issues/6536)
* [these issues related to the resolver](https://wiki.python.org/psf/Fundable%20Packaging%20Improvements#Finish_dependency_resolver_for_pip)

### Role 1: Senior developer

#### Summary and budget

Development: $116,375 for 665 hours, at $175 per hour

We seek a senior Python developer for the following tasks, starting in mid-December 2019 or early January 2020, till the end of May 2020.

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

Development: $103,700, for 670 hours at $150 per hour, plus $1600 for onboarding travel and $1600 for [PyCon](https://us.pycon.org/2020/) travel

We seek an intermediate-to-senior Python developer for the following tasks, starting in early January 2020, till the end of December 2020.

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
   - The current maintainer will teach and train the new developer via architectural overview, setup and configuration, pair programming, narrative feature tours, code reviews, meta-review of the developer's code reviews, and planning for the resolver work. We aim to use [this guide](https://modelviewculture.com/pieces/software-in-person) to make this time productive, and work to ensure a closer working relationship between the developers, a granular project plan for the next few months, raw material for future documentation, and an increase in development and maintainer skills for our developer.
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

The backend codebase is in Python. The pip documentation is built using reStructuredText and Sphinx.

Potential proposers should be comfortable with Python, and will have support from an additional contractor focused on user interface and user experience design to advise on command line experience improvements.

Familiarity and expertise with all technologies is not required. Strong Python skills and experience are a must, though.

#### Specific Technologies Used

For the best primer, see the [developer documentation](https://pip.pypa.io) for pip.

You can also see the [complete codebase](https://github.com/pypa/pip) on GitHub.

????? test infrastructure


##### Backend

While pip is a client-side program, there will be backend work involved in building test infrastructure.

Travis CI
Azure?
We're open

- [Python](https://www.python.org/) 3.6+
- [PostgreSQL](https://www.postgresql.org) - [SQLAlchemy](https://docs.sqlalchemy.org/en/latest/) - [psycopg2](http://initd.org/psycopg/)
- [Redis](https://redis.io)

##### Frontend

Currently the only frontend work for pip is the pip documentation, which is built using reStructuredText and Sphinx. While building test infrastructure, we may want to add some frontend capability to that. The Python Package Index uses the following, so we have some team expertise in them and would prefer that those be used for any frontend work.

Note: Our frontend is primarily static; these tools power the toolchain that creates our final assets.

- [Node](https://nodejs.org/en/)
- [Gulp](https://gulpjs.org)
- [SASS](https://sass-lang.com)
- [Stimulus](https://stimulusjs.org/)

### Project Management and Reporting

This project will be led and managed by the Python Software Foundation Director of Infrastructure and an external project manager.

Regular meetings (at most 30 minutes each, 4 times per month) will be held to coordinate efforts among the project managers, backend developers, and UX researcher/designer.

Oral or textual status reporting during these meetings, as well as regular brief textual summaries of current status (such as a sentence or two, a few times per week, via Slack), will be required. Additionally, participation on the [public issue tracker](https://github.com/pypa/warehouse/issues) and submission of changes via [code review](https://github.com/pypa/warehouse/pulls) for the project will be required.

## Questions, Concerns, or Feedback

Please contact [Ernest W. Durbin III \<ewdurbin@pyfound.org\>](mailto:ewdurbin@pyfound.org), Director of Infrastructure at the Python Software Foundation.

