# Contributing

These rules apply to every repository in this account. GitHub shows this file only where a
repository has no `CONTRIBUTING.md` of its own; such a file may add detail but must not relax
these rules.

## Tests

Every test explains why it exists, at the level of the individual test.

- Each test function, parametrised case or rule states:
  - **Protects:** the behaviour, risk or requirement it guards;
  - **Detects:** the failure it catches, and what that failure means for a user;
  - **Needs:** its prerequisites, such as hardware, data or a platform. A test that cannot
    run reports `SKIP` or `UNSUPPORTED`, never a pass;
  - **Breadcrumb:** the source it exercises.
- A check that cannot fail is not a check. Each rule ships with one input that must fail
  and one that must pass. New tests are written to fail first.
- Reviews are recorded per test, against a hash of the test's source. Changing the test
  makes its review stale. A generated inventory reports which tests are unreviewed; it
  never certifies them.
- Weakening an assertion, widening a tolerance, adding a skip or deleting a test needs
  its own justification in the pull request.

## Documentation

- Link documents to each other and to the code they describe with relative links. Every
  living document is reachable from the README.
- A change to code updates the documents that describe it in the same pull request.
- Dated records, such as reviews and test receipts, are never rewritten. A correction is
  a new record that links the old one.
- Write for an engineer who will act on the document. Lead with the result, cite sources,
  say what is measured and what is not known, and leave out filler and boilerplate.

## Getting started

Each README starts with no more than four commands: install, build, test and run. The
test command is the one continuous integration runs, and the README says which stages
(hardware, platform-specific) it does not cover.

## Pull requests

Describe the behaviour change, link the issue or requirement, list the documents and
tests you changed and why, and include the failing-first output of new tests. Signed
commits are required where branch protection asks for them.
