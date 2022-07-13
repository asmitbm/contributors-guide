#### Suggesting Enhancements

This section walks you through the process of submitting an enhancement for an addition to Weaviate core, such as a brand-new feature or a small change to an already-existing feature. Following these guidelines can help you make a better suggestion, and make it easier for the maintainers and the community to understand your proposal and find other similar suggestions.

When filling out the template, be sure to include the steps you would take if the requested feature were available.

We recommend you to check the Weaviate Module System to get better understanding of how Weaviate works.

* [Overview and High-Level Architecture](https://weaviate.io/developers/contributor-guide/current/weaviate-module-system/overview.html)
* [Code-Level Architecture](https://weaviate.io/developers/contributor-guide/current/weaviate-module-system/architecture.html)

Be sure to checkout the [folder structure](Folder-structure.md) to get high level overview of the repository.

#### How do I make a (good) suggestion for improvement?

Enhancement suggestions are tracked as GitHub issues. Check if there's already a WIP (work in progress) issue which describes that enhancement. If not, create an issue in the repository using the template and provide the following information:

* **Use a clear and descriptive title** for the issue to identify the suggestion.
* Give as many specifics as you can in a **step-by-step description** of the suggested improvement.
* **Add specific examples** to demonstrate the steps. If possible, include code snippets in Markdown format.
* **Describe the current behavior** and then **explain which behaviour you were expecting and why**.
* **Include images, animated GIFs, or video links** that can be used to illustrate the steps or highlight the area of Weaviate that the suggestion relates to.
* **Explain why this enhancement would be useful** to most Weaviate users.
* Specify which **version of Weaviate** you're using. Check the version in your `docker-compose.yml` file.

#### Folder Structure

```
.
├── adapters 
│   ├── client 
│   ├── handlers
│   │   ├── graphql
│   │   └── rest
│   └── repos
│       ├── classifications
│       ├── db
│       ├── modules
│       └── schema
├── ci
├── client
│   ├── batch
│   ├── classifications
│   ├── graphql
│   ├── meta
│   ├── obejcts
│   ├── operations
│   ├── schema
│   └── well-known
├── cmd
|   └── weaviate-server
├── deprecations
├── docker-compose
├── entities
│   ├── additional
│   ├── aggregation
│   ├── filters
│   ├── models
│   ├── modulecapabilities
│   ├── moduletools
│   ├── multi
│   ├── schema
|   |   └── crossref
│   ├── search
│   ├── searchparams
│   ├── storagestate
│   └── storobj
├── genesis
│   ├── client
|   |   └── operations
│   ├── cmd
|   |   └── weaviate-genesis-server
│   ├── models
│   ├── restapi
|   |   └── operations
│   ├── state
│   ├── test
|   |   └── acceptance
│   ├── tools
├── modules
│   ├── img2vec-neural
│   ├── multi2vec-clip
│   ├── ner-transformers
│   ├── qna-transformers
│   ├── text-spellcheck
│   ├── text2vec-contextionary
│   ├── text2vec-openai
│   └── text2vec-transformers
├── openapi-specs
├── test
|   ├── acceptance
|   ├── helper
|   └── integration
├── tools
│   ├── dev
│   ├── license_headers
│   ├── release_template
│   └── test
└── usecases
    ├── auth
    ├── classification
    ├── cluster
    ├── config
    ├── connstate
    ├── locks
    ├── modules
    ├── monitoring
    ├── network
    ├── objects
    ├── schema
    ├── sharding
    ├── traverser
    └── vectorizer
```