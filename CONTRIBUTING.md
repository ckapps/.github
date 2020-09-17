# Contributing to @ckapp

:tada: First off, thanks for taking the time to contribute! :tada:

The following is a set of guidelines for contributing to @ckapps packages, which are hosted in the [ckapps Organization](https://github.com/ckapps) on GitHub. Think of them as mostly guidelines, not rules. Use your best judgment, and feel free to propose changes to this document in a pull request.

#### Table Of Contents

[Code of Conduct](#code-of-conduct)

[How Can I Contribute?](#how-can-i-contribute)

- [Reporting Bugs](#reporting-bugs)
- [Suggesting Enhancements](#suggesting-enhancements)
- [Your First Code Contribution](#your-first-code-contribution)
- [Pull Requests](#pull-requests)

[Styleguides](#styleguides)

- [Git Commit Messages](#git-commit-messages)
- [TypeScript Styleguide](#typescript-styleguide)
- [Specs Styleguide](#specs-styleguide)
- [Documentation Styleguide](#documentation-styleguide)

[Additional Notes](#additional-notes)

- [Issue and Pull Request Labels](#issue-and-pull-request-labels)

## Code of Conduct

This project and everyone participating in it is governed by the [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

## How Can I Contribute?

### Reporting Bugs

Before creating bug reports, please check [this list](#before-submitting-a-bug-report) as you might find out that you don't need to create one. When you are creating a bug report, please [include as many details as possible](#how-do-i-submit-a-good-bug-report). Fill out [the required template](https://github.com/ckapps/.github/blob/master/ISSUE_TEMPLATE/bug_report.md), the information it asks for helps us resolve issues faster.

<details><summary>Ticket is closed</summary>If the ticket is already closed, but it seems that you are still experiencing the same problem, open a new issue and link to the original issue in the body.</details>

#### Before Submitting A Bug Report

- **Check** if you are already using the **latest version** of the package. The problem may have been fixed in a newer version already
- **Figure out how to reproduce** the bug, maybe even by preparing a minimum setup. This will help investigating the problem.
- **Perform a [search](https://github.com/search?q=+is%3Aissue+user%3Ackapps)** to see if a similar enhancement has already been suggested. If so, add a comment instead of creating a new one

#### How Do I Submit A (Good) Bug Report?

Bugs are tracked as [GitHub issues](https://guides.github.com/features/issues/). Create an issue on that repository and provide the following information by filling out one of our issue templates.

Explain the problem and include additional details to help maintainers reproduce the problem:

- **Use a clear and descriptive title** for the issue to identify the problem
- **Describe steps to reproduce the problem** in as many details as possible
- **Provide specific examples to demonstrate the steps**. Include links to files or GitHub projects, or copy/pasteable snippets, which you use in those examples. If you're providing snippets in the issue, use [Markdown code blocks](https://help.github.com/articles/markdown-basics/#multiple-lines)
- **Describe the behavior you observed after following the steps** and point out what exactly is the problem with that behavior.
- **Explain which behavior you expected to see instead and why.**
- **Include screenshots and animated GIFs** which help you demonstrate the steps. Check out [recordit](https://recordit.co/) for creating GIFs

Include details about your configuration and environment:

- **Which package version you're using?** Check the `package.json`
- **Specify the run environment** the problem occurs (e.g. node.js + version or browser + version)

### Suggesting Enhancements

Before creating enhancement suggestions, please check [this list](#before-submitting-an-enhancement-suggestion) as you might find out that you don't need to create one. When you are creating an enhancement suggestion, please [include as many details as possible](#how-do-i-submit-a-good-enhancement-suggestion). Fill in [the template](https://github.com/ckapps/.github/blob/master/ISSUE_TEMPLATE/feature_request.md).

#### Before Submitting An Enhancement Suggestion

- **Check** if you are already using the **latest version** of the package. The enhancement may have been implemented in a newer version already
- **Perform a [search](https://github.com/search?q=+is%3Aissue+user%3Ackapps)** to see if a similar enhancement has already been suggested. If so, add a comment instead of creating a new one

#### How Do I Submit A (Good) Enhancement Suggestion?

Enhancement suggestions are tracked as [GitHub issues](https://guides.github.com/features/issues/). Create an issue on that repository and provide the following information:

- **Use a clear and descriptive title** for the issue to identify the suggestion
- **Provide a step-by-step description of the suggested enhancement** in as many details as possible
- **Provide specific examples to demonstrate the steps**. Include copy/pasteable snippets which you use in those examples, as [Markdown code blocks](https://help.github.com/articles/markdown-basics/#multiple-lines)
- **Describe the current behavior** and **explain which behavior you expected to see instead** and why
- **Include screenshots and animated GIFs** which help you demonstrate the steps. Check out [recordit](https://recordit.co/) for creating GIFs
- **Specify which package version you're using**

### Your First Code Contribution

Unsure where to begin contributing? You can start by looking through these `good first issue` and `help wanted` issues:

- [Good first issues][good-first-issue] - a good issue to start contributing
- [Help wanted issues][help-wanted] - little bit more comprehensive issues than `good first issue`s

Both issue lists are sorted by total number of comments. While not perfect, number of comments is a reasonable proxy for impact a given change will have.

### Pull Requests

The process described here has several goals:

- Maintain quality
- Fix problems that are important to users
- Engage the community in working towards the best possible solutions
- Enable a sustainable system for maintainers to review contributions

Please follow these steps to have your contribution considered by the maintainers:

1. Create a pull request from one of our templates from [here](https://github.com/ckapps/.github/tree/master/PULL_REQUEST_TEMPLATE)
2. Follow the [styleguides](#styleguides)
3. After you submit your pull request, verify that all [status checks](https://help.github.com/articles/about-status-checks/) are passing

## Styleguides

### Git Commit Messages

- Use the present tense ("Add feature" not "Added feature")
- Use the imperative mood ("Move cursor to..." not "Moves cursor to...")
- Reference issues and pull requests liberally after the first line
- Enforce [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)

### TypeScript Styleguide

- All TypeScript code is linted using [eslint](https://eslint.org/)
- All TypeScript code is formatted using [Prettier](https://prettier.io/)

### Specs Styleguide

- All code is tested using [jest](https://jestjs.io/)
- The test files are placed next to the tested module, naming it `<file-name>.spec.ts`
- Treat `describe` as a noun or situation.
- Treat `it` as a statement about state or how an operation changes state.

#### Example

```typescript
describe('a dog', () => {
  it('barks', () => { ... // spec here });

  describe('when the dog is happy', () => {
    it('barks', () => { ... // spec here });
  });
});
```

### Documentation Styleguide

- Use [JSDoc](https://jsdoc.app/) for code documentation

## Additional Notes

### Issue and Pull Request Labels

This section provides a list of the labels we are using to organize and track issues and pull requests.

| Label name             | search :mag_right:                            | Description                                             |
| ---------------------- | --------------------------------------------- | ------------------------------------------------------- |
| `:gear: package`       | [search][search-org-label-gear-package]       | (npm) package related follow.                           |
| `:gear: project`       | [search][search-org-label-gear-project]       | Everything related to the project configuration / setup |
| `:orange_book: docs`   | [search][search-org-label-book-docs]          | Improvements or additions to documentation              |
| `ci`                   | [search][search-org-label-ci]                 | Related to Continous integration                        |
| `:construction: chore` | [search][search-org-label-construction-chore] | Housekeeping                                            |

[search-org-label-gear-package]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3Ackapps+label%3A":gear:+package"
[search-org-label-gear-project]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3Ackapps+label%3A":gear:+project"
[search-org-label-book-docs]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3Ackapps+label%3A":orange_book:+docs"
[search-org-label-ci]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3Ackapps+label%3Aci
[search-org-label-construction-chore]: https://github.com/search?q=is%3Aopen+is%3Aissue+user%3Ackapps+label%3A":construction:+chore"
[good-first-issue]: https://github.com/search?q=is%3Aopen+is%3Aissue+label%3A"good+first+issue"+label%3A"help+wanted"+user%3Ackapps+sort%3Acomments-desc
[help-wanted]: https://github.com/search?q=is%3Aopen+is%3Aissue+label%3A"help+wanted"+user%3Ackapps+sort%3Acomments-desc+-label%3A"good+first+issue"
