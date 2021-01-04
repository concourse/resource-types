<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents** 

- [Concourse Resource Types](#concourse-resource-types)
  - [Submitting a Resource Type](#submitting-a-resource-type)
  - [Where to get help](#where-to-get-help)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Concourse Resource Types
Welcome to the Concourse [resource types](https://concourse-ci.org/resource-types.html) repository! Here you can publish your resource type. Upon approval, it will be live in the Concourse docs site under the ‘Resource Types’ [section](https://resource-types.concourse-ci.org/).

On this page, you’ll find details on how to contribute a resource type to the repository. You can find instructions on building a resource type [here](https://concourse-ci.org/implementing-resource-types.html). 

## Submitting a Resource Type
Resource types can be submitted directly to this repo through a fork-and-PR workflow:
1. [Fork](https://help.github.com/articles/fork-a-repo/) the [Concourse Resource Types repo](http://github.com/concourse/resource-types) into your Github account.
1. Add a yaml file for your resource type directly in the same folder as this README.md.

    Follow the schema: `[OWNER_NAME]-[RESOURCE_TYPE_NAME].yml` for file name (e.g. concourse-git-resource.yml)
    ```
    ...
    /README.md
    /your-new-yaml.yml
    ...
    ```

1. Populate your file with the resource type name, repo url and the description of the resource type. For example:
    ```yaml
    name: git
    repo: https://github.com/concourse/git-resource
    ## Add the full url of the image if it is not listed under dockerhub
    container_image: concourse/git-resource
    description: |
        tracks commits in a branch of a Git repository
    ```
1. Commit your work, making sure your commit has a signature certifying agreement to the [DCO](https://developercertificate.org). For more information, see [signing your work](https://github.com/concourse/concourse/blob/master/CONTRIBUTING.md#signing-your-work).
1. When you're ready, push your code and [submit a pull request](https://help.github.com/articles/creating-a-pull-request-from-a-fork/)!
1. Your pull request will be reviewed by one or more maintainers, and you might receive feedback or requests for additional changes to your code.
    
    In order to approve a resource type, we check the following:
    - You are the primary maintainer of the resource type or affiliated to the maintaining org.
    - The repository url of the resource type is valid.
    - The container image of the resource type exits.
1. When a maintainer accepts your changes, they will merge your pull request.

## Where to get help
There are two main channels that the Concourse community uses for getting help and discussing potential changes.
  1. Get help in Discord in the #resource-types channel. [Click here](https://discord.gg/MeRxXKW) to get access.
  1. Discuss new ideas in the [Concourse forums](http://discuss.concourse-ci.org/).

