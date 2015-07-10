# git-db-switcher

When you work on a project that used git branch intensively, with sometimes fixes and new features developed in parallel, you often need to reset your database to be sure no new development will interact with your fixes.

We would like to provide a way to handle those constrains with a simple and universal way for all the toolchain from git branch or checkout to switch in your project.

## Example Process

1. You work on a `master` branch
2. You create a new branch called `fix-bug1`
3. Something (TBD - that project) catch that change and will create and setup a new database from a starting point (TDB - default to your `master` database or last branch you work on).
4. You checkout the branch and your website

## Dependencies and needs

1. Git
  * git branch
  * git checkout
  * git hooks to trigger action
2. Environnement variables support to easily switch between databases in your project
  * Most of current language already handle the use of environnement variables.
3. MySQL - for a starting point
  * Database backup
  * Database creation
  * Database setup

## Studiing tools
* Docker may probably help to easily handle databases steps

## Other projects or articles to look at

### PHP

* [Git Workspace](https://github.com/sandervd/git-workspace)
* [Every Feature a Branch, Every Branch a Dev Environment... Without Breaking the Bank! The Perfect Git-flow Dev Environment for Small Shops](https://ohthehugemanatee.org/blog/2013/09/02/every-feature-a-branch-every-branch-a-dev-environment-without-breaking-the-bank-the-perfect-git-flow-dev-environment-for-small-shops/)
* [Automatically Change Database Based on the Git Branch](http://foggyperspective.com/article/automatically-change-database-based-git-branch)
