# documentation

## Types

encapsulation of documentation

The documentation lives in two kind of locations: the livingdoc repository and in READMEs in each project repository.

Four types of documentation coexists:

### META
**Location: in the livingdoc repository**
- general concepts
- global project architecture

### README
**Location: each project repository**
- technical presentation of the repository
- no node setup nor docker installation
- features list
- repo architecture
- names of repo managers
- details on configuration

### GUIDE
**Location: in the livingdoc repository**
- Livingdocs in 2 minutes
- contains a list of guides to get a new person up and running in no time :)
- based on real needs, exhaustive how-tos from scratch for each targeted public: developers, designers...
- guides should act as mortar between the project READMEs

### IN CODE
**Location: in the code**
- API documentation in the code
- once done it could automatically extracted and rendered as web pages continuously

## Classification

```bash
.
├── boilerplate
│   └── publish_plugin.md             [README] #boilerplate
├── cheat-sheets
│   └── postgres.md                   [GUIDE] #postgres
├── concepts
│   └── main_concepts.md              [META] #concepts
├── data-migrations
│   ├── migrations.md                 [GUIDE] #migration
│   └── migration-task-states.jpg
├── delivery
│   ├── api_essentials.md             [IN CODE] #restAPI
│   ├── api_link.png
│   ├── css_resources.png
│   └── (deprecated)webhooks.md
├── deployment
│   ├── amazon_s3.md                  [GUIDE] #deployment
│   └── docker.md
├── design
│   ├── (brokenByLukas)migrations     [GUIDE] #migration #design
│   │   ├── migrations.md
│   │   └── migration-subjects.png
│   ├── component-config.md           [README, META] #design
│   ├── create_designs.md             [README, META] #design
│   └── upload.md                     [GUIDE, README] #design
├── ideas                             [META, NOTDOC] #ideas
│   ├── document-model.md
│   └── track-changes.md
├── installation                      [META] #requirements
│   ├── hardware-requirements.md
│   └── requirements.md
├── livingdocs-framework              [README] #framework
│   ├── browser_api.md
│   ├── component_model.md
│   ├── component_tree.md
│   ├── directives.md
│   └── livingdoc.md
├── page-management                   [META] #pageManagement
│   ├── component_card_definition.md
│   ├── elastic_indices.md
│   ├── main.md
│   ├── overview.png
│   ├── sample_app.md
│   ├── teaser_assignment.md
│   └── teaser_assignment.png
├── README.md
├── roadmap
│   └── overview.md                   [NOTDOC]
├── server                            [IN CODE] #server
│   ├── api_basics.md
│   ├── api_cors.md
│   ├── api_errors.md
│   ├── deployment.md
│   ├── editing_api_authentication.md
│   ├── editing_api_design.md
│   ├── editing_api_document_list.md
│   ├── editing_api_documents.md
│   ├── editing_api_endpoints.md
│   ├── editing_api_hooks.md
│   ├── editing_api_publications.md
│   ├── editing_api_revisions.md
│   ├── editing_api_spaces.md
│   ├── editing_api_users.md
│   ├── home.md
│   ├── how_to_create_a_user.md       [README] #server
│   ├── public_api_endpoints.md
│   ├── third_party_integrations.md
│   └── webhook_system.md
└── WERE_HIRING.md
```


