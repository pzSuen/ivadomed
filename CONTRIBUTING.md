

# Contributing to IVADO Medical Imaging

## Table of contents
1. [Introduction](#introduction)
2. [Opening an issue](#opening-an-issue)
    1. [Before Submitting a New Issue](#before-submitting-a-new-issue)
    2. [Submitting an Issue](#submitting-an-issue)
3. [Contributing to IVADO Medical Imaging (Pull request)](#contributing-to-ivado-medical-imaging-pull-request)
    1. [Opening a Branch](#opening-a-branch)
    2. [Naming your Branch](#naming-your-branch)
    3. [Developing](#developing)
    4. [Committing](#committing)
    5. [Submitting a Pull Request](#submitting-a-pull-request)
4. [Versioning](#versioning)

## Introduction 


Thank you for contributing to IVADO Medical Imaging! Examples of contribution include:

- Reporting issues you encounter

- Providing new code or other content into the IVADO Medical Imaging repositories

- Contributing to the wiki or mailing list


## Opening an issue



Issues (bugs, feature requests, or others) can be submitted [on our project's issue page.](https://github.com/neuropoly/ivado-medical-imaging/issues)


### Before Submitting a New Issue


Please take a few seconds to search the issue database in case the
issue has already been raised.

When reporting an issue, make sure your installation has not been tempered
with (and if you can, update to the latest release, maybe the problem was
fixed).


### Submitting an Issue


#### Issue Title

Try to have a self-descriptive, meaningful issue title, summarizing the
problem you see. Do not add the function name, because this will be
taken care of by the [Issue Labels]().

Examples:

-   *Crashes during image cropping*
-   *Add a special mode for multi-class segmentation*

#### Issue Body


**Describe** the issue and mention the IVADO Medical Imaging version and
OS that you are using.

If you experience an error, copy/paste the Terminal output (include your
syntax) and please follow these guidelines for clarity:

-   If there is less than 10 lines of text, embed it directly in your
    comment in github. Use \"\~\~\~\" to format as code.
-   If there is 10+ lines, either use an external website such as
    [pastebin](https://pastebin.com/) (copy/paste your text and include
    the URL in your comment), or use [collapsable Github markdown
    capabilities](https://gist.github.com/ericclemmons/b146fe5da72ca1f706b2ef72a20ac39d#using-details-in-github).

Add useful information such as screenshots, etc.

If you submit a feature request, provide a *usage scenario*, imagining
how the feature would be used (ideally inputs, a sequence of commands,
and a desired outcome). Also provide references to any theoretical work
to help the reader better understand the feature.

## Contributing to IVADO Medical Imaging (Pull request)


Contributions relating to content of the github repository can be
submitted through github pull requests (PR).

PR for bug fixes or new features should be based on the
[master]{.title-ref} branch.

The following github documentation may be useful:

-   See [Using Pull
    Requests](https://help.github.com/articles/using-pull-requests) for
    more information about Pull Requests.
-   See [Fork A Repo](http://help.github.com/forking/) for an
    introduction to forking a repository.
-   See [Creating
    branches](https://help.github.com/articles/creating-and-deleting-branches-within-your-repository/)
    for an introduction on branching within GitHub.

### Opening a Branch


If you are in the [Official list of
contributors](https://github.com/neuropoly/ivado-medical-imaging/people?affiliation=ALL)
please open a branch inside [SCT\'s official
repository](https://github.com/neuropoly/ivado-medical-imaging)

### Naming your Branch

Prefix the branch name with a personal identifier and a forward slash;
If the branch you are working on is in response to an issue, provide the
issue number; Add some text that make the branch name meaningful.

Examples:

-   `ol/100-fixup-lr-scheduler`
-   `ab/loader-pep8`

### Developing


#### Conflicts


Make sure the PR changes are not in conflict with the documentation,
either documentation files ([/README.md]{.title-ref},
[/wiki/]{.title-ref}).

#### Testing


Please add tests, especially with new code. As of now, we have
integration tests, and unit tests (in [/testing/]{.title-ref}). They are
straightforward to augment, but we understand it\'s the extra mile; it
would still be appreciated if you provide something lighter (eg. in the
commit messages or in the PR or issue text) that demonstrates that an
issue was fixed, or a feature is functional.

Consider that if you add test cases, they will ensure that your feature
\-- which you probably care about \-- does not stop working in the
future.

#### Documentation


If you are implementing a new feature, update the documentation to
describe the feature, and comment the code (things that are not
trivially understandable from the code) to improve its maintainability.

Make sure to cite any papers, algorithms or articles that can help
understand the implementation of the feature. If you are implementing an
algorithm described in a paper, add pointers to the section / steps.

#### Code style


Please review your changes for styling issues, clarity, according to the
[PEP8 convention](https://www.python.org/dev/peps/pep-0008/). Correct
any code style suggested by an analyzer on your changes.
[PyCharm](https://www.jetbrains.com/help/pycharm/2016.1/code-inspection.html)
has a code analyser integrated or you can use
[pyflakes](https://github.com/PyCQA/pyflakes).

Do not address your functional changes in the same commits as any
styling clean-up you may be doing on existing code.

#### Licensing

Ensure that you are the original author of your changes, and if that is
not the case, ensure that the borrowed/adapted code is compatible with
the MIT license.

### Committing


#### Commit Titles


Provide a concise and self-descriptive title (avoid \> 80 characters).
You may "scope" the title using the applicable command name(s), folder
or other \"module\" as a prefix. If a commit is responsible for fixing
an issue, post-fix the description with `(fixes #ISSUE_NUMBER)`.

Examples:

    testing: add testing function for validation metrics
    loader: add timer
    documentation: add slice_axis to the config files
    model: add HeMIS network

#### Commit Sequences


Update your branch to be baseline on the latest master if new
developments were merged while you were developing. Please prefer
**rebasing** to merging, as explained in [this
tutorial](https://coderwall.com/p/7aymfa/please-oh-please-use-git-pull-rebase).
Note that if you do rebases after review have started, they will be
cancelled, so at this point it may be more appropriate to do a pull.

Clean-up your commit sequence. If your are not familiar with git, [this
good
tutorial](https://www.atlassian.com/git/tutorials/rewriting-history) on
the subject may help you.

Focus on committing 1 logical change at a time. See [this
article](https://github.com/erlang/otp/wiki/writing-good-commit-messages)
on the subject.

### Submitting a Pull Request


#### PR Title


The PR title is used to automatically generate the
[Changelog](https://github.com/neuropoly/ivado-medical-imaging/blob/master/CHANGES.md)
for each new release, so please follow the following rules:

-   Provide a concise and self-descriptive title (see [Issue
    Title](#issue-title)).
-   Do not include the applicable issue number in the title (do it in
    the [PR Body](#pr-body)).
-   Do not include the function name (use a [PR Labels]() instead).
-   If the PR is not ready for review, add \"(WIP)\" at the beginning of
    the title.

#### PR Body


Describe what the PR is about, explain the approach and possible
drawbacks. Don\'t hesitate to repeat some of the text from the related
issue (easier to read than having to click on the link).

If the PR fixes issue(s), indicate it after your introduction:
`Fixes #XXXX, Fixes #YYYY`. Note: it is important to respect the syntax
above so that the issue(s) will be closed upon merging the PR.

#### Continuous Integration


The PR can\'t be merged if [Travis
build](https://travis-ci.org/neuropoly/ivado-medical-imaging) hasn\'t
succeeded. If you are familiar with it, consult the Travis test results
and check for possibility of allowed failures.

#### Reviewers


Any changes submitted for inclusion to the master branch will have to go
through a
[review](https://help.github.com/articles/about-pull-request-reviews/).

Only request a review when you deem the PR as "good to go". If the PR is
not ready for review, add \"(WIP)\" at the beginning of the title.

Github may suggest you to add particular reviewers to your PR. If
that\'s the case and you don\'t know better, add all of these
suggestions. The reviewers will be notified when you add them.

## Versioning

Versioning uses the following convention: MAJOR.MINOR.PATCH, where:

PATCH version when there are backwards-compatible bug fixes or enhancements, without alteration to Python's modules or data/binaries.
MINOR version when there are minor API changes or new functionality in a backwards-compatible manner, or when there are alteration to Python's modules or data/binaries (which requires to re-run SCT installer for people working on the dev version),
MAJOR version when there are major incompatible API changes,
Beta releases follow the following convention:

MAJOR.MINOR.PATCH-beta.x (with x = 0, 1, 2, etc.)
Stable version is indicated in the file version.txt. For development version (on master), the version is "dev".
