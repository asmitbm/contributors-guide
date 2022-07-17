This is a beginner's guide to using git and GitHub to help you contribute to Weaviate. There are four main GitHub repositories of Weaviate, which you can contribute to as beginner. This includes:

* [Weaviate](https://github.com/semi-technologies/weaviate) - our main product Weaviate core
* [Weaviate-io](https://github.com/semi-technologies/weaviate-io) - official Weaviate documentation
* [Weaviate Examples](https://github.com/semi-technologies/weaviate-examples) - apps built using Weaviate vector search engine
* [Awesome Weaviate](https://github.com/semi-technologies/awesome-weaviate) - list of examples and tutorials of how to use the Weaviate vector search engine 

#### Start by Forking

* Simply click the `Fork` button on the GitHub website. That's how easy it is. This will create a copy of the repository in your account.

<!--![fork repo](../assets/fork.png)-->

* Once you have done that, head over to your account, select the forked repository, and clone your repo to your local machine

<!--![clone repo](../assets/clone.png)-->

```
git clone git@github.com:<USERNAME>/weaviate.git
```

("weaviate" is used as the example repo. Make careful to cite the particular repository you are contributing to (for example, "weaviate-io")

* After cloning the repository from GitHub, use the change directory command to first move to that folder

```
cd weaviate
```

* Track the "upstream" repo you forked in order to keep your fork up to date. You'll need to add a remote to complete this

```
git remote add upstream https://github.com/semi-technologies/weaviate.git
```
* To check if your local copy has a reference and upstream link to the remote repository in GitHub, run the command below

```
git remote -v
```

Output:

```
origin    https://github.com/Your_Username/weaviate.git (fetch)
origin    https://github.com/Your_Username/weaviate.git (push)
upstream  https://github.com/semi-technologies/weaviate.git (fetch)
upstream  https://github.com/semi-technologies/weaviate.git (push)
```

When you want to update your fork with the most recent upstream changes, you must first fetch the upstream repo's branches and commits to bring them into your repository. This can be done in two ways:

* [Using GitHub and git CLI](#using-github-and-git-cli)
* [Using git CLI]()

##### Using GitHub and git CLI

* Head over to your forked repository, and under `Fetch Upstream`, click `Fetch and merge`. This will bring all the latest changes in your forked repository.

* Next open git CLI, and checkout on `main` branch (if you make any changes, make sure to commit them first)

```
git checkout main
```

* Then pull the changes into local repository

```
git pull origin main
```

This will sync with the latest changes in your forked repository

##### Using git CLI

The only difference between this method and the previous one is that you will fetch the remote using CLI. 

* Check out the `main` branch first

```
git checkout main
```

* Fetch the remote 

```
git fetch upstream
```

* Then pull its changes into your local default branch

```
git pull upstream main
```

* Last, push to your own remote origin to keep the forked repo in sync

```
git push origin main
```

One liner script for super users:

```
git remote add upstream https://github.com/semi-technologies/weaviate.git || true && git fetch upstream && git checkout main && git pull upstream main && git push origin main
```

##### View all branches including those from upstream

```
git branch -a
```

#### Create a new branch to work on

It's important to create a new branch whenever you start working on a new feature or bugfix. In addition to being standard git process, it also maintains your changes structured and distinct from the `main` branch so that you can submit and handle many pull requests with ease for each task you do.

Create a new branch from the `main` branch to contain your changes. Give your branch its own simple informative name. 

For enhancements use `feature/issue#` or `feature/nameOfFeature`

For bugs use `bug/issue#` or `bug/nameOfBug`

```
git checkout -b feature/newPage
```

This will create a new branch and checkout to it. Now, start hacking away and making any modifications you want.

#### Create a Pull Request

A few considerations must be made before submitting a pull request. Your pull request will be merged more quickly if your branch is cleaned up.

If any commits to the `upstream main branch` have been made during the period you've been working on your changes, you will need to `rebase` your development branch so that merging it will be a fast-forward process without requiring any effort on conflict resolution.

Fetch the upstream main branch and update your local repository by following the [above](#using-git-cli) steps.

Rebase your development branch if there were any new commits

```
git checkout feature/newPage
git rebase main
```

##### Pull request process

Here are some general guidelines about how to submit a pull request:

* If you're making visual changes, include a screenshot of the affected element before and after

* Please update the documentation if you change any user-facing functionality in Weaviate

* Each pull request should implement one new feature or fix one bug. Submit multiple pull requests if you want to add or fix multiple items.

* Do not commit changes to files that are irrelevant to your feature or bug fix

* Write a good commit message. Check out [commit guidelines](Commit-guidelines.md)

**How to create a pull request:**

Make sure you are on your development branch

* Add your files to the staging area

```
git add filename
```

You can also use `git add .` to stage all the files, but it is not recommended to use. You might include created files, backups, and configuration files containing information you don't want included. Prior to adding files to the staging area, always validate visually which files need to be staged.

* Check if the file(s) is added in the staging area

```
git status
```

* If everything is good to go, proceed with commiting your changes with a good commit message

```
git commit -m "your commit message"
```

* Push your changes to forked repository on GitHub

```
git push origin feature/newPage
```

When all of your changes have been committed and pushed to GitHub, visit the page for your fork there, choose the development branch, and then press the `Create pull request` button. 

If you need to make any further commits to your pull request, simply check out your development branch and push the updates to GitHub. Your pull request will automatically keep track of and update the commits made to your development branch.

* Complete the pull request by filling out our [pull request template](https://github.com/semi-technologies/weaviate-io/blob/main/.github/PULL_REQUEST_TEMPLATE.md)

* Once your changes are ready, make sure you self review your pull request to speed up the review process.

#### Self reviewing pull requests

You should always review your own pull request first.

For any changes you commit, make sure that you:

* Confirm that the changes meet the objectives of the issue you created or are working on.

* Compare your pull request's source changes to staging to ensure that the output matches the source and that everything is rendering as expected. This assists in detecting issues such as typos or content that isn't rendering due to versioning issues.

* Check for technical accuracy in the content. You can always [ask for help](https://join.slack.com/t/weaviate/shared_invite/zt-goaoifjr-o8FuVz9b1HLzhlUfyfddhw) if you get stuck.

* Verify that the syntax of new or updated Liquid statements is proper. Jekyll uses the [Liquid](https://shopify.github.io/liquid/) templating language to process templates.

* If there are any failing checks in your PR, try troubleshooting them until they are passing or [ask for help](https://join.slack.com/t/weaviate/shared_invite/zt-goaoifjr-o8FuVz9b1HLzhlUfyfddhw).