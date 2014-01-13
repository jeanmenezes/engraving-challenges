# Git Basics

If you have not worked on projects that use Git, GitHub, and the Pull Request mechanism for collaborating, here is a brief overview of the basic concepts involved.  You will also find much more information on Git from [the free Git Book] (http://git-scm.com/book).  You will also find more specific information on the workflow employed by this particular project in [the Git Workflow document](git-workflow.md).

## Initial Setup

Before you begin, you will need to create an account on [GitHub](https://github.com).  You will also need to install [Git tools](http://git-scm.com/downloads) on your own machine.

## Repositories

A project has a main repository ("repo") stored on GitHub.  This is the public face of the project and is where the files accessible to everyone are stored.  It is used as the basis for other repositories that individual contributors may maintain, both on GitHub and on their own local machines.  It is customary to refer to this main repository as the "upstream" repo.

This repo is what you will *read* from whenever you need to get the latest and greatest versions of the project files.  You will never probably write to this repo directly; only the project lead(s) will do this.

When you first join a project, you start by visiting the main repo and pressing the `Fork` button to create your own copy of that repo.  This fork is *also* stored on GitHub.  You will then create a "clone" of your own fork by pressing the `Clone in Desktop` button while viewing your fork.  This copies your fork to your own machine.  The copy of the fork on GitHub is customarily called the "origin" repo, and the copy on your own machine might be referred to as the "local" repo.

## Workflow Overview

It is the local repo on your own machine you will be working on mostly.  When you want to make your work available to others, you will upload your changes to your origin repo on GitHub and then issue a Pull Request to ask the project lead to merge your changes into the upstream repo.  Once your changes have been merged into the upstream repo, they become available to others.  You will also periodically update your own local repo from the upstream repo to incorporate others' changes.

Your local repo is your own personal sandbox.  You can play with these files however you like, including adding new ones.  You will normally create "branches" (via `git checkout -b`) for your work, but the rules for how you are expected to manage your branches may differ from project to project.  That is where the [git workflow](git-workflow.md) for your specific project will hopefully give you more guidance.

Every so often, you decide things are at a state where you want to take a snapshot of your current sandbox to record the current state of your work for posterity.  You do this via `git commit`.  After one or more of these commits, you might decide you are at a point where you feel these should be written to your fork on GitHub, so you do a `git push`.  After one or more of these pushes, you might decide your work is ready to be shared with others, so you visit your fork on GitHub and press the `Pull Request` button to ask the project leads to merge your changes into the main (upstream) repo.

Every so often, you will also decide it would be good to grab the work others have been contributing.  So you do a `git fetch upstream` to download the latest version of everything.  Because of the details of how git manages version control, you have to also do a `git rebase` or `git merge` to fully incorporate these downloaded changes into your local repo.  This is the step hardest to fully grasp, I find, but do not worry at this point about the specifics of what this does.  Once you have updated your local repo, you can continue working, do more commits, more pushes, and pull requests, more fetches, and the cycle continues.

Again, this basic overview applies to many projects on GitHub.  For more information on the workflow for this specific project, including when and how to branch, commit, push, and issue Pull Requests, see the [Git Workflow document](git-workflow.md).
