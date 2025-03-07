# Welcome to Rosetree's template SFDX Project Repository!

## What is it for?
This template repository aims to enable consistent experiences across different project types by defining several key configuration files.

## What's included?



### PMD GitHub Action for Pull Requests

This template repository includes a GitHub Action (./.github/workflows/CI.yml) that runs the [Salesforce Code Analyzer](https://forcedotcom.github.io/sfdx-scanner/) against changes introduced in a pull request. This static analysis is performed with PMD, ESLint, and other frameworks. [PMD (Problem Mistake Detector)](https://pmd.github.io/pmd/index.html) is a static analyis tool that can help identify issues in code related to best practice, security, performance. This repository includes a PMD ruleset configuration that is referenced in the static analysis, so feel free to tailor to your project's specific needs.

> Important note: if you don't want the static analysis to "fail" a PR, you can increase the severity threshold in the CI.yml file. Currently, this threshold is set to 3 as a default.

Lastly, if you're working with legacy code, it's understandable to not address every static analysis violation. To mute rules, you can use the following syntax:

```java
@SupressWarnings('PMD.[rulesetName]')
```

***Please use this bypass sparingly and only when working with existing client code.***

### Codeowners definition

A codeowners definition (./.github/CODEOWNERS) can define which users should be automatically 
added to pull requests based on file types. Have you ever wanted to ensure that a 
specific team member __always__ is tagged to review proposed changes to a critical 
Apex class? This is where you can define that. More details can be found in [GitHub's
documentation](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners). 

> Important note: the default CODEOWNERS file includes Tim and Jesse to demonstrate how to configure it, please update this post-project creation.

### Pull Request Template

Authoring a pull request is an essential part of our workflows, and the new template defines a "Description" section and a brief checklist to ensure we're following our [style guide](https://github.com/Rosetree-Solutions/Rosetree-Guides/blob/main/ApexStyleGuide.md) and running our tests. 

## Okay, cool, how do I get started?

By clicking the bright green "Use This Template" button! (And selecting "Create a new repository").

<img width="924" alt="Screenshot 2023-04-28 at 12 29 10 PM" src="https://user-images.githubusercontent.com/20362765/235225562-d82d344b-1b56-49f0-a388-60a337d60885.png">

Next, fill out the relevant details and you're all set.

<img width="785" alt="Screenshot 2023-04-28 at 12 29 21 PM" src="https://user-images.githubusercontent.com/20362765/235225613-052cf9bf-6ccc-4603-a6a1-f44185508403.png">

## Other Considerations

Branch protections should be set up by the project's technical lead to enforce PRs into the trunk branch of the repository.
