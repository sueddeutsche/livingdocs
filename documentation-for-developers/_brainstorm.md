# Brainstorm

## current status

### Where is the documentation

Most of the documentation lives in a public repository:

https://github.com/upfrontIO/livingdocs

There is a high level documentation like Livingdocs concepts and architecture alongside a low level one like API endpoints description.

The quick-start-documentation is mainly private and lives in multiple private repositories across two Github organizations: Livingdocs and nzzdev. It takes the form of multiple README.md at the root of repositories:

#### intial setup
Livingdocs quick start: https://github.com/upfrontIO/team/blob/master/Onboarding/initial_setup.md

#### editors
Livingdocs: https://github.com/upfrontIO/livingdocs-editor/blob/master/README.md

nzz: https://github.com/nzzdev/livingdocs-editor/blob/master/README.md

boilerplate: https://github.com/upfrontIO/livingdocs-editor-boilerplate

#### dependencies

server: https://github.com/upfrontIO/livingdocs-server/blob/master/README.md

framework: https://github.com/upfrontIO/livingdocs-framework/blob/master/README.md

#### servers

li-service-server: https://github.com/upfrontIO/livingdocs-service-server/blob/master/README.md

nzz-api: https://github.com/nzzdev/livingdocs-api/blob/master/README.md

#### design

Boilerplate: https://github.com/upfrontIO/livingdocs-design-boilerplate

Bluewin from boilerplate: https://github.com/upfrontIO/bluewin-design

Timeline design: https://github.com/upfrontIO/livingdocs-design-timeline

design website: https://github.com/upfrontIO/livingdocs-design-website

#### NZZ

How to test design locally: https://github.com/nzzdev/morpheus/blob/develop/livingdocs/readme.md

NZZ delivery architecture: https://github.com/nzzdev/cms-guide/blob/master/architecture/delivery_current.md

New NZZ delivery architecture: https://github.com/nzzdev/cms-guide/blob/master/architecture/delivery_new.md

Troubleshoot Livingdocs: https://github.com/nzzdev/cms-troubleshoot-guide

Build Livingdocs design: https://github.com/nzzdev/nzz-standard

Design: https://github.com/nzzdev/livingdocs-design-nzz

#### delivery

blog: https://github.com/upfrontIO/livingdocs-delivery

bluewin: https://github.com/upfrontIO/bluewin-delivery

#### devops

rancher 1: https://github.com/upfrontIO/infrastructure

rancher 2: https://github.com/upfrontIO/livingdocs-rancher

docker: https://github.com/upfrontIO/livingdocs-docker

elasticsearch docker: https://github.com/upfrontIO/dockerfile-elasticsearch

postgres docker: https://github.com/upfrontIO/dockerfile-postgres

#### guides

npm publish, commit messages...: https://github.com/upfrontIO/guides

linting...: https://github.com/upfrontIO/apply-guides

#### others

editable: https://github.com/upfrontIO/editable.js

design viewer: https://github.com/upfrontIO/livingdocs-design-viewer

ldm aka livingdocs manager: https://github.com/upfrontIO/livingdocs-manager

### Is documentation duplicated?

Yes, mostly when it concerns developers workflow: setups, how-tos...

### Where is documentation outdated?

Tough to say for now, most developers know their stuff without looking at the documentation. Each piece of documentation should be challenged to know for sure.

Elimination of duplicated documentation is to do prior assessing the "outdatedness" of pieces of the documentation.

### Missing documentation?

Again hard to say, once the documentation challenged we should find the missing pieces.

## Guidelines

### Who does the documentation target?

Public documentation targets everyone, private documentation targets developers or designers.

### What to include? What not? Where to draw the line?

Maybe we could include everything. Every bit of knowledge that anyone holds could be documented. And then separate the documentation according to each public needs: developers, designers, managers...

### What language to use

As of now it's markdown in Github. This question of the form could be answered after the content is up-to-date.

### Distinguish guide / documentation?

A possibility is to have a complete documentation. And multiple guides that helps to achieve specific goals: upload a design... Each guides would use specific points of the documentation as small chunk of knowledge: setup docker...

## Maintenance

### How to detect outdated documentation

Having more tests and labeling existing tests as documentation breakers.

### How to update documentation

If we stay in Github, same as code through PR and reviews.

### Documentation is feedback

Refactor what’s too complicated to use

# Thoughts

- It would be cool to use docker (elasticsearch and postgres) as a service for local development. This way the setup for designers and developers would ditch docker. PLUS we could use prefilled (seeded) databases for editor testing.

- Naming: having a piece a software named as its user is not cool: li-editor/editors

- Naming: li-server is too close to li-service-server or nzz-server and it does not do the same thing. It's almost the equivalent of calling the framework li-editor and the li-editor a li-service-editor.

- Naming: Livingdocs folks call the nzz-api what the NZZ folks call the li-api...

