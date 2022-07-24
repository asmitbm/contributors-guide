#### What makes a good commit

The cardinal rule for creating good commits is to ensure there is only one "logical change" per commit. Why? Because more changes per commit may result in more bugs.

#### Why do we need good commit messages

#### How to write good commit messages

A commit message consists of three parts:

* [Summary line](#summary-line)
* [Description](#description)
* [Issue reference](#issue-reference)

Commit template

```
tag: Short explanation of the commit

Longer explanation explaining exactly what's changed and why, whether
any documentation or web feature has been changed, what bugs were fixed
and so forth. Be concise but not too brief.

Fixes #123.
```

It is preferable to follow these guidelines for each patch before pushing it to git.

##### Summary Line:

Example:

```
feat: Add blog pages
```

* Be sure to not exceed 50 characters. Maintaining summary lines at this length makes them readable and provides a clear explanation of the change.

* After adding `tag`, the summary line should begin with a capital letter, unless it begins with a lowercase symbol or identifier.

* Use imperative present tense ("Add feature" not "Added feature")

* Prefix your commit with one `tag`, to make it easier to know what type of change you have done. See the list of **`tags`** below

* Leave out the trailing period (full stop).

`tag` types:

* **`feat`**: A new feature

* **`fix`**: A bug fix

* **`docs`**: Documentation only changes

* **`style`**: Changes that do not affect the meaning of the code or documentation (white-space, spelling errors, missing semi-colons, line endings, etc)

* **`refactor`**: A code change that neither fixes a bug or adds a feature

* **`perf`**: A code change that improves performance

##### Description

Example:

```
This pull request adds blog page feature to the documentation website, 
where people can read about Weaviate's latest releases. 
Blogs can be updated by adding markdown files to `_posts/blog/` folder.
```

* Each description line must be no more than 75 characters long (there is no limit on number of lines).

* You should explain why the changes were made. This is especially important for complex, non-self-explanatory changes.

* The commit message is primarily for your and others' benefit, and they should be able to understand it both now and in the future.

* If the summary is self-explanatory, you can omit writing the description.

##### Issue reference

Example:

```
Fixes: #123
```

* If the commit fixes an issue, add a line on the last paragraph: "Fixes: #ISSUE_NUMBER.".

* The issue reference will add the commit link to the issue automatically.