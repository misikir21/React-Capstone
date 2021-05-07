# curriculum-tools-copy-projects

The bash script stored in this repo will help you to quickly copy [GitHub project boards](https://docs.github.com/en/github/managing-your-work-on-github/about-project-boards) with associated issues.
It will be useful for the Microverse group projects that should be based on project board templates prepared by Microverse.


## Getting Started

In order to successfully copy a given project board, you need to follow the below steps.

### Prerequisites

1. Initialize an empty repository for your group project.

2. Manually [copy project board](https://docs.github.com/en/github/managing-your-work-on-github/copying-a-project-board) from a specific template to your own repo.
    - [JavaScript Group Capstone](https://github.com/microverseinc/curriculum-javascript/projects/1)
    - ...

3. Install [jq](https://stedolan.github.io/jq/download/).

``` bash
    brew install jq # for OS X
    sudo apt-get install jq # for Linux
    chocolatey install jq # for Windows
```

4. Generate [personal access token for GitHub API](https://github.com/settings/tokens/new?scopes=repo).

### Usage

1. Clone this repository.
2. Open terminal.
3. Navigate to the cloned repo dir.
     ``` bash
         cd curriculum-tools-copy-projects
     ```
4. Run script with correct input parameters
     ``` bash
         sh copy_github_board.sh <YOUR_GITHUB_AUTH_TOKEN> <SOURCE_GITHUB_USERNAME> <SOURCE_REPO_NAME> <YOUR_GITHUB_USERNAME> <YOUR_GROUP_PROJECT_REPO_NAME> 
     ```
     
     - for example, in case of the JavaScript Group Capstone, you should use:
     
     ``` bash
         sh copy_github_board.sh <YOUR_GITHUB_AUTH_TOKEN> microverseinc curriculum-javascript <YOUR_GITHUB_USERNAME> <YOUR_GROUP_PROJECT_REPO_NAME> 
     ```
5. Verify that the template project board and your board look exactly the same.


## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

Feel free to check the [issues page](../../issues/).

## Show your support

Give a ⭐️ if you like this project!

## Acknowledgments

This script is based on the [How to copy project cards on GitHub](https://blog.termian.dev/posts/project-cards-copy-github/) by Damian Terlecki.