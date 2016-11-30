# How to contribute

CWRC, Islandora, Drupal, and Fedora Commons are are built and maintained by open-source communities. Everyone is encouraged to submit issues and changes (patches) to improve Drupal, and to contribute in other ways.

This file provides an introduction to contributing and a few guidelines that we need contributors to follow so that we can have a chance of keeping on top of things.

## Getting Started

1. Make sure you have a [Github account](https://github.com/signup/free).
2. Submit a ticket for your issue, assuming one does not already exist. We have added issue and pull request templates to help you do this.
    * Clearly describe the issue, including steps to reproduce, when it is a bug.
3. [Fork this repository on GitHub](https://help.github.com/articles/fork-a-repo/).

Note that we use the [Git Flow branching model](http://nvie.com/posts/a-successful-git-branching-model/) in this repository:

* We use the `master` branch for bringing forth production releases
* We use the `develop` branch for "next release" development.
* We prefix feature branch names with `feature/`.
* We prefix release branch names with `release/`.
* We prefix hotfix branch names with `hotfix/`.
* We prefix support branch names with `support/`.
* We do not prefix version tags.

These are the suggested names in the Git Flow branching model, and the defaults for the [nvie/gitflow tools][gitflow-tools].

We suggest installing the [nvie/gitflow tools][gitflow-tools] to help you follow these conventions.

[gitflow-tools]: https://github.com/nvie/gitflow

## Making changes

1. If you haven't already, clone your fork of the project to your local computer.
    * If you are using the [nvie/gitflow tools][gitflow-tools], this is a good time to run `git flow init` (note that this project uses the default branch/prefix names suggested by the tool).
    * If you use [Git hooks](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks) to run automated lints / checks, this is a good time to set them up.
2. Create a branch (with the appropriate name prefix) where you want to base your work.
    * If you are using the [nvie/gitflow tools][gitflow-tools], you can do this by running `git flow $type start $name` (e.g.: `git flow feature start add-support-for-foo`).
    * If you are not using the git flow tools, you can do this by runnning `git checkout -b $type/$name` (e.g.: `git checkout -b feature/add-support-for-foo`)
3. Make commits of logical units of work.
    * Smaller / simpler commits are usually easier to review.
    * Follow the [Drupal coding standards](https://www.drupal.org/coding-standards/) for [PHP](https://www.drupal.org/docs/develop/standards/coding-standards), [CSS](https://www.drupal.org/docs/develop/standards/css), [JavaScript](https://www.drupal.org/docs/develop/standards/javascript) and [documentation](https://www.drupal.org/docs/develop/coding-standards/api-documentation-and-comment-standards) when writing code.
    * Ideally, lint the files to make sure they do not contain syntax errors before committing them. (`php -l $file` will lint PHP files, for example).
    * Ideally, [write good commit messages](http://chris.beams.io/posts/git-commit/).
4. Double-check your work:
    * If the repository contains automated tests, make sure they all pass.
    * Check that all the files conform to Drupal coding standards. [PHPCodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer) can do this automatically, and its included `phpcbf` tool can fix many simple mistakes!
5. Push your branch to your fork.
    * If you are using the [nvie/gitflow tools][gitflow-tools], you can do this by running `git flow $type publish $name` (e.g.: `git flow feature publish add-support-for-foo`).
    * If you are not using the git flow tools, you can do this by runnning `git push --set-upstream $type/$name` (e.g.: `git push --set-upstream feature/add-support-for-foo`).
6. Follow the prompts in the message that Github returns, or visit your fork's page on Github to [submit a pull request](https://github.com/thoughtbot/factory_girl_rails/compare/).
