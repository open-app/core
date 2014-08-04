
# Roadmap

## Overview:

This document outlines the steps in our roadmap. Nodes in the ecosystem are groups like Enspiral with high 'managed' trust. Nodes manage their own database and use Open-App Services to provide common data for their own suite of apps. 

After we have tested the Enspiral node, other groups will be able to start their own nodes, install their own customised suite of apps, query, and share data across the ecosystem and broader Open Linked Datasets. 

Steps:

 1. Provide group and account functionality (read only) to Cobudget.
 2. Develop a read-only 'Open-App UI' for [Enspiral](enspiral.com).
 3. Connect Open-App UI to People and Groups services.
 4. Establish further nodes and link the Open-App UI to other Open Linked Data.

<br>

## Steps:

### 1. Provide group and account functionality (read only) to Cobudget. 
<p align="center"><img src="/images/roadmap-step-1.png?raw=true" width="572" height="387" alt="step-1" ></p>

The first step will allow Enspiral to maintain their data (membership and subgroup lists) in one place (Loomio) and have it propagate to other apps (currently Cobudget). Group admins can avoid the tiresome work of re-inviting users and manually synching data across apps. Cobudget developers can avoid writing boilerplate group and account code. 

The People and Group services will have links to standard vocbularies allowing the apps to have broader interoperability at later steps.

<br>

### 2. Develop a read-only 'Open-App UI' for [Enspiral](enspiral.com). 
<p align="center"><img src="/images/roadmap-step-2.png?raw=true" width="572" height="387" alt="step-2" ></p>

We have funding to develop a "Directory App" for Enspiral. Initially we will use a dummy read-only database of people and group data while we focus on the UI. This "Directory App" will really be a generic "Open-App UI" for browsing different types of linked data across the ecosystem. We have completed two rounds of user-testing with paper prototypes for the UI. The main learning was that people prefer a flexible search-focused interface. 

Open-App services use a graph database ([LevelGraph](https://github.com/mcollina/levelgraph)). We want to test how users interact with graph search (similar to [Facebook's](http://en.wikipedia.org/wiki/Facebook_Graph_Search)). Graph search allows powerful queries across nodes and is very flexible. Testing this requires a working frontend app.

The 'Identity Service' provides a more complete standards-based authentication service. 

<br>

### 3. Connect Open-App UI to People and Groups services.
<p align="center"><img src="/images/roadmap-step-3.png?raw=true" width="572" height="387" alt="step-3" ></p>

At the third step the Open-App UI will be connected to live data from the People and Group Services (read only). The 'Enspiral' node will now have 3 apps that share data: Loomio, Cobudget, and the Open-App UI. 

<br>

### 4. Establish further nodes and link the Open-App UI to other Open Linked Data.
<p align="center"><img src="/images/roadmap-step-4.png?raw=true" width="572" height="387" alt="step-4" ></p>

The ecosystem is born! Other groups can now start their own nodes and share data amongst their own apps. Nodes can also share and query available data across the entire ecosystem and interoperable databases. Users can search Open-App UI for the people in their own node, linked nodes, or linked OpenDatasets (e.g. public profile information of the 830k people on DBpedia).

Apps can also set their own level of particpation:
 1. Integrate further (allow HTTP POST from an Open-App service).
 2. Use Open-App services directly for core functionality (like Cobudget).
 3. Adopt common vocabularies and data formats to permit interoperability (like DBpedia)

### 5. Build more Services















