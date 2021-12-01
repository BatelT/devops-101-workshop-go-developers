# Workshop: DevOps 101 for Go developers ![1200px-Go_gopher_favicon svg](https://user-images.githubusercontent.com/25744447/144277903-f0955f64-a94a-47ef-9d43-5aa392d8aff2.png)


## Course Description

When you’re new to an industry, you encounter a lot of new concepts. This can make it really difficult to get your feet underneath you on an unfamiliar landscape, especially for junior engineers. What does DevOps really mean? What’s all this software? What’s all this jargon? Is DevOps a methodology, or a toolset? Is any of this actually going to make my life easier, or is it just a bunch of industry buzzwords? I’ll answer all of these questions (and more) during this hands-on workshop, and get you set up with an end-to-end DevOps solution to automate your build artifact storage, vulnerability detection, testing, and deployment.


## Prerequisites

1. [JFrog Cloud account](https://jfrog.com/artifactory/start-free/#saas)

    This is free, no credit card required. It includes access to Artifactory and Xray, with a limited amount of storage transfer.

2. [JFrog CLI](https://www.jfrog.com/confluence/display/CLI/JFrog+CLI)
    
    JFrog CLI is an open source project written in Go the JFrog CLI is a tool which provides a simple interface that helps to interact with all JFrog's products.

3. Go

    We will need to package a simple Go application. Go client version 1.11.0 and above is required.

4. Code editor

    Whatever you are most comfortable with. I will be using VScode. 


## Course Outline


### [Intro to DevOps](https://github.com/batelt/devops-101-workshop/blob/master/docs/intro.md)
- What is the definition of DevOps?
- What does DevOps mean for developers?
- What is all of this jargon?


### [Artifactory Module](https://github.com/batelt/devops-101-workshop/blob/master/docs/artifactory.md)
- What is binary repository manager?
- What are build artifacts?
- Why might you need to manage your build artifacts?
- Binary repository setup in Artifactory
    - Go

### [Xray Module](https://github.com/batelt/devops-101-workshop/blob/master/docs/xray.md)
- Why do devs need to worry about vulnerability detection and license compliance?
- Security and License policies
- Scan a Build
- Running Reports
- Reading Results


### Additional Resources

[Glossary of Terms](https://github.com/batelt/devops-101-workshop/blob/master/docs/glossary.md)

[Artifactory Documentation](https://www.jfrog.com/confluence/display/JFROG/Package+Management)

[Xray Documentation](https://www.jfrog.com/confluence/display/JFROG/Xray+Security+and+Compliance)

[JFrog CLI Documentation](https://www.jfrog.com/confluence/display/CLI/JFrog+CLI)

[Pipelines Documentation](https://www.jfrog.com/confluence/display/JFROG/Pipelines+Developer+Guide)

![alt text](https://dev-to-uploads.s3.amazonaws.com/i/brm2ce1pq1yu23ifc7wi.jpg)
