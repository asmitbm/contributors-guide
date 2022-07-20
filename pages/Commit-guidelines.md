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