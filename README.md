# Recipes Collection: QA SFIA Project

## Introduction
The purpose of the project was to create a CRUD (Create Read Update Delete) application using all the concepts and skills aquired in the first six weeks in QA academy ([Cloud Native - Fundamental Project Specification](https://portal.qa-community.co.uk/~/cne/projects/fundamental--cn)). 

## Table of Contents


## Requirements
The requirements are listed below:
- Jira board 
- Clear Documentation 
- Risk Assessment
- A relational database 
- A functional application created in Java
- Front-end website and integrated API
- ~~Fully designed tests~~
- Version Control System
- CI server
- Application deployed to a cloud-based virtual machine

## Recipes Collection
In order to meet the requirements, an application to store recipes was implemented. The application allows the user to create a list of recipes with a description of the procedure to follow, the ingredients needed and their quantity.

## MOSCOW approach

The MOSCOW approach was followed to make sure that the essential features of the app were prioritised and to ensure the creation of a fully functional product that meets all the requirements.
- #### Must Have
1. CRUD functionality at least for the recipes
2. Database to store the recipes
3. Circle CI must deploy the app
4. The app shoild run on a virtual machine spinning in the Google Cloud Platform
5. Clear documentation and planning
- #### Should Have
1. Multiple html pages allowing the user to perform each CRUD functionality
-### Wont have
1. User login feature
2. Advance design on the front end 

## Database

The following image shows the relationship present between the "Recipe" and "Ingredients" entities.

![ERD diagram](ERD.png)

A recipe can contain more than one ingredient, so there is a one-to-many relationship between the two entities. The primary keys of the tables are the id which are automatically generated and the entities are connected to each other through the foreign key (which is the id of the recipe a particular ingredient belongs to).
The CRUD functionality was implemented in both tables as shown in the following sections. 

## CI Pipeline
The following figure shows which technologies were used and the relationship between them. The source code was implemented in Java and to ensure that the changes on the project will not get lost, a version control system (git) was used. The CI server (circleci) keeps track of any new features added to the application by polling the git repository, and as soon as an update is available, the CI server builds the code and deploys it in the virtual machine running on Google Cloud Platform. Finally, Jira Software was used as a project tracking platform. This process guarantees a continuous integration. 
![CI diagram](pipeline.png)

## Planning
The planning of the project was essential in order to meet the MVP (Minimum Viable Product). The project tracking tool used was a Jira board which allows to produce epics which have user stories with tasks related to them.
![User Stories](user.png)
In order to interact with the tasks dynamically, "sprints" were created. These are a good way to keep track of the progress of the project because it allows to classify the tasks as "to do", "in progress" or done.
![PN board](jira.png)


## Risk assessment
![Risk Assessment](https://docs.google.com/document/d/1HFkSVNzoGUVQ0q5xYNdBtZqSv8gIKmyCva692vqYvHE/edit?usp=sharing)

