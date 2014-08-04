# The Open-App Ecosystem

## Introduction

How can an ecosystem of people, groups and software applications (apps) function together? This is difficult question and cannot be known in advance. We've got a pretty good idea though. Here we present what we think will work but most of these concepts have not been tested in this particular way before. We invite your feedback and comments!




## Project Goals

First, what are we trying to achieve? Well, initially:

 * Different companies within the [Enspiral Network](http://enspiral.com/) are developing apps for commons based peer-production (notably [Loomio](https://www.loomio.org)). 
 * We want to allow users to share data between different apps. Users and groups should not have recreate and manually sync their accounts and group data in different apps.
 * Other developer teams are working on aligned apps (using different programming languages and frameworks).
 * We want them to particpate in the ecosystem too and have these apps interoperate with Enspiral apps.

More broadly, 

 * In the current paradigm of the Web users store data in app 'platforms' and these platforms make data available through an API.
 * The platforms own the data.
 * The data is "silo'd". The data in one platform doesn't "know" about any of the user's other data in the other platforms.
 * Large platforms are the center of the web.
 * Large platforms often degrade the user experience through selling advertising.
 * Small, locally hosted platforms can only access a small dataset and are not very powerful. 

Hmmm, not ideal. But...

 * A different, emerging paradigm (the [Semantic Web](http://en.wikipedia.org/wiki/Semantic_Web)) allows people and groups to host and control permissions to their own data.
 * These data can be linked to other data, no matter where it is hosted. 
 * People and groups are the center of the web. 

Therefore,

 * We want to let people and groups host and control their own data.
 * We want to let users create connections between their own and others' data, so that..
 * the ecosystem will be larger than just the apps that Enspiral and aligned teams create and the users of these apps.  
 * locally hosted apps have more power, and..
 * the user experience is not degraded. 

Further,

 * We want ourselves and others to be able to earn a livlihood associated with the ecosystem. 

## Overview

Identities as nodes. Shared data within nodes. Federated queries between nodes. 





## Ecosystem Layers

the ecosystem has different layers. From 'highest' to 'lowest' these are:

 1. Identities (the nodes in the network)
 2. Apps (UI plus a API's)
 3. Components (UX patterns within an app)
 4. Services (API's)
 5. Vocabularies (Ontologies, common language between apps)
 6. Messaging: 
  * Message Patterns
  * Data Formats
  * Data Transport Protocols





### Apps

'Apps' are software products with their own use-cases and branding. Apps particpate in the ecosystem in different ways. Example: Loomio is an app for collaborative decsion-making.

Particpating apps:

App   | Use-case | Target Particpation  | Status
 ---  | --- | --- | ---
[Loomio](https://github.com/loomio/loomio)  | collaborative decision-making | Connected  | [Operational](https://www.loomio.org), conection in progress
Cobudget | collaborative budgeting   |  Serviced  | Alpha, in progress
[Directory-App](https://github.com/open-app/directory-ui)  | find info related to people and groups | Interoperable, Fully serviced, Components | In design


### Components

'Components' are modular reusable UI patterns. Frontend developers can build UI's from Open-App components in the same way that backend developers can build apps from Open-App services. We plan on building components in [React](http://facebook.github.io/react/) to prepare Open-App for the arrival of [Web-Components](http://webcomponents.org/) browser support. 

No components are currently available.


### Services  

Developers can use Open-App API's ('Services') to provide some or all of a fully featured app's functionality.  We call a service that provides [CRUD](http://en.wikipedia.org/wiki/Create,_read,_update_and_delete) service to data resources associated with an Entity Type a 'Store'. Example: the 'People' service provides user account [CRUD](http://en.wikipedia.org/wiki/Create,_read,_update_and_delete) and is associated with the 'Person' type. 

Apps that 'connect', 'integrate', or use Open-App services directly ('serviced') share data. 
Example: Different Apps might share the same People, Group and Identity services and effectively share user account and group data (the [Shared Database](http://www.enterpriseintegrationpatterns.com/SharedDataBaseIntegration.html) pattern). This allows app users to sign-on into both apps with a single identity and have any changes in these data reflected in other apps. 

Service   | Description  | Vocabularies  | Status
 --- | --- | ---
People  | 'Store' for Person data  | [schema](http://schema.org/), [foaf](http://xmlns.com/foaf/0.1#), [org](http://www.w3.org/TR/vocab-org#) | In progress
Groups  | 'Store' for Group data  | [schema](http://schema.org/), [foaf](http://xmlns.com/foaf/0.1#), [org](http://www.w3.org/TR/vocab-org#) | In progress
Identity  | Authentication | [Web Payments](https://web-payments.org/specs/source/identity-credentials/) | Planned


### Vocabularies:

We reccomend using the following vocabularies. Apps and services that use common vocabularies and data messaging become interoperable with other apps and services in the ecosystem that do the same:

Vocabulary  | Description
 ---  | ---
[schema](http://schema.org/)  | General-purpose vocabulary
[foaf](http://xmlns.com/foaf/spec/) | The Friend of a Friend (FOAF) RDF vocabulary, for People and Groups
[org](http://www.w3.org/TR/vocab-org/#) | Vocabulary for describing organizational structures, specializable to a broad variety of types of organization
[rel](http://vocab.org/relationship/.html) | A vocabulary for describing relationships between people
[gr](http://www.heppnetz.de/ontologies/goodrelations/v1.html) | GoodRelations is a standardized vocabulary for product, price, store, and company data. 


### Data Messaging


#### [Request-Response](http://en.wikipedia.org/wiki/Request%E2%80%93response)

Send a pair of Request-Reply messages, each on its own channel

#### [Publish-Subscribe](http://en.wikipedia.org/wiki/Publish/subscribe)

Send the event on a Publish-Subscribe Channel, which delivers a copy of a particular event to each receiver.

####[Message Translator](http://www.eaipatterns.com/MessageTranslator.html)

Translates one data format into another.


### Data Transport Protocols




### Data Formats

Format | Status
 ---  | ---
[JSON-LD](http://json-ld.org/) | Supported
[JSON-API](http://jsonapi.org/) | Planned



## Participating in the Ecosystem

Apps can particpate in the ecosystem through four integration patterns. 









[deprecated]
We have 5 different ways in which apps can particpate in the Ecosystem. Apps may participate in one or several of the following:

 1. Connected - File Transfer | App >> Ecosystem
 2. Integrated - Messaging + File Transfer | App <<>> Ecosystem
 3. Interoperable - Common vocabularies and data messaging | App >> Vocabulary << Ecosystem
 4. Serviced - Uses Open-App micro-services | Shared Database
 5. Components - Uses Open-App UI components | Component >> Frontend App


### 1. 'Connected' - File Transfer

We can *connect* an app to the ecosystem by letting users pull their data from the app's API, translate and replicate the data on a service in our supported vocabularies and data formats. Requires a 
Example: Loomio

### 2. Integrated - Messaging + File Transfer

As well as being connected to ecosystem (#1) the *integrated* app can also reads from Open-App API's and replicate the data in its own database. 


### 3. Interoperable - Share common vocabularies and linked data formats.

Linked Datad Apps and services that use the common vocabularies and data formats are deeply *interoperable*. We prefer that Apps aim for this level of particpation.

Example: 


### 3. Serviced - Built with OpenApp microservices

Apps that use OpenApp microservices avoid writing boilerplate code for common functionality.

When many apps use the same microservice a person or group can maintain a collection of data - a list of members, assets etc in one place and share these data across apps that use the same OpenApp microservice. For example, whenever someone is added to a group in Cobudget this change is immediately reflected in DirectoryApp. Participating at this level allows groups to avoid repetitive admin tasks. 

Example: Cobudget


### 4.  - Uses OpenApp UI components 

