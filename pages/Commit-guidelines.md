#### Commit Guidelines

The cardinal rule for creating good commits is to ensure there is only one "logical change" per commit.

Example commit

```
tag: short explanation of the commit

Longer explanation explaining exactly what's changed and why, whether
any documentation or web feature has been changed, what bugs were fixed
and so forth. Be concise but not too brief.

Fixes #12345.
```
`tag` types:

* **feat**: A new feature

* **fix**: A bug fix

* **docs**: Documentation only changes

* **style**: Changes that do not affect the meaning of the code or documentation (white-space, spelling errors, missing semi-colons, line endings, etc)

* **refactor**: A code change that neither fixes a bug or adds a feature

* **perf**: A code change that improves performance

Few tips for writing good commit messages:

* The commit message is primarily for the benefit of the others, and they should be able to understand it both now and six months from now.

* Prefix your commit with one `tag`, to make it easier to know what type of change you have done.

* Use the present tense ("Add feature" not "Added feature")

* If the commit fixes an issue, add a line on the last paragraph: "Fixes: #ISSUE_NUMBER.".

* Leave out the trailing period (full stop).

* Each line in description must not exceed 75 characters (there is no limit on number of lines).