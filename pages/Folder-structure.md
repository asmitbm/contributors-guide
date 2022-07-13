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