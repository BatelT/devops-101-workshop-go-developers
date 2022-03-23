# Artifactory Module


This module will walk you through Artifactory. What it is, what it does, why you should use a binary repository manager, and how to get started. We will cover usage for Gorepository.

## Overview


Artifactory is a universal binary repository manager. This means that it can be used to manage your build artifacts (compiled binaries, information about your builds, docker images, helm charts, etc) regardless of the technologies you're using -- Python, JavaScript, C#, Ruby, whatever. It supports 27 different package types explicitly, as well as a generic repository type for everything else. This isn't a replacement for source control tools, like GitHub or Bitbucket. Think of it as the place your code goes after it's been wrtitten and built or packaged, but before it's deployed. Repositories are broken up into three categories: local, remote, and virtual. 

**Local** repositories are what they sound like: repositories for your code, that exists locally on your machine. 
**Remote** repositories are also fairly self-explanatory; they contain remote code, like your project's dependencies. This functions sort of like a cache, so that after the first download, your project pulls its dependencies from the associated remote repository rather than from NPM or PyPi or whatever. 
**Virtual** repositories create a kind of envelope around the local and remote repositories for your project, and this is what you'll be interacting with most frequently.

A tool like this is used for many reasons, but the biggest benefits are to companies with a lot of different technologies in their stack, and companies that have security concerns requiring them to tightly control both their own code and their dependencies.


## Examples


### Go

This step will walk you through creating a Go repository type and creating your build and upload it to artifactory.

1. Set Up the Repositories
    - In the upper right-hand corner, click the dropdown that displays your username and select "Quick Setup." From that screen, select Go, click Create, and follow on-screen instructions. Default names and settings are fine for this.

    - From the main UI, clicking Artifactory -> Artifacts should now show you three new repositories with your prefix like: devops101-go, devops101-go-local, and devops101-go-remote.

![Create repo](https://user-images.githubusercontent.com/25744447/144276926-75cf1402-522b-4f80-a086-c53b617eeda1.gif)

2. Configure the JFrog CLI

    -  First let's configure the platform URL by running the following command:

        $ jfrog config add
    
    - Configure the project's Go repositories using the command:
        
        $ jfrog go-config

    - Resolve the project dependencies from Artifactory and create a build 

        $ jfrog rt go build --build-name=go-workshop-build --build-number=1 
        
    - Publish version v1.0.0 of the package to the go-local repository in Artifactory
    
        $ jfrog rt gp v1.2.3 --build-name=go-workshop-build --build-number=1

    - Collect environment variables and add them to the build info
        
       $ jfrog rt bce go-workshop-build 1

    - Publish the build info to Artifactory
      
      $ $ jfrog rt bp go-workshop-build 1
      
Now click on the builds tab under Artifactory tab and let's investigate our first build
