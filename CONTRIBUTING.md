# Contributing

This project came into existence because python is a language that author is
more familiar with than existing implementations in Javascript/Typescript and
Go. Its scope is to provide CLI that more or less correspond to Go
implementation. On the top of that a python library is available. Current
implementation is considered feature complete. For this reason it is unlikely
that new features will be implemented. Some bugs might be fixed.

This page describes steps needed to (re)create development environment for contributions.

## TLDR;

Project:

* uses PEP 621 for metadata ([project] section of pyproject.toml)

* defines `setuptools` as PEP 518 (what is required to build) and corresponding
  PEP 517 (what function to call to build)

* uses `Black` as code formatter

* uses `pytest` for unit tests and `tox` for their orchestrating

* extensive amount of pre-commit hooks using `pre-commit` framework

## Getting started

These steps need to be done only for the first time:

1. Fork this repository on GitHub

2. Clone the fork locally. From now on work in a directory of a repository.

3. Create a virtual environment:
   <https://packaging.python.org/en/latest/tutorials/installing-packages/#creating-virtual-environments>

4. Install local src in Development mode:
   <https://packaging.python.org/en/latest/tutorials/installing-packages/#installing-from-a-local-src-tree>

5. Test if CLI generates output:

   ```bash
   fakelish
   ```

6. Install pre-commit hooks: <https://pre-commit.com/#installation>


## New feature or bug fix

1. Create a new branch:

  ```bash
  git checkout -b name-of-your-bugfix-or-feature master
  ```

2. Make changes to the code

3. Commit changed files into a git.

4. Run tests:

  ```bash
  tox
  ```

5. Push a branch to your forked repository.

6. Create a pull request in GitHub.
