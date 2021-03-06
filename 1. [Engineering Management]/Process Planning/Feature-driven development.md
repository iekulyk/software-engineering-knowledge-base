[Feature-driven development](https://en.wikipedia.org/wiki/Feature-driven_development)
------------------------------------------
![visualization](https://upload.wikimedia.org/wikipedia/commons/9/99/Fdd_process_diagram.png)

**Feature-driven development (FDD)** is an iterative and incremental software development process. It is one of a number of lightweight or Agile methods for developing software. FDD blends a number of industry-recognized best practices into a cohesive whole. These practices are all driven from a client-valued functionality (feature) perspective. Its main purpose is to deliver tangible, working software repeatedly in a timely manner.

**Develop overall model**
The FDD project starts with a high-level walkthrough of the scope of the system and its context. Next, detailed domain models are created for each modeling area by small groups and presented for peer review. One of the proposed models, or a combination of them, is selected to become the model for each domain area. Domain area models are progressively merged into an overall model.

**Build feature list**
The knowledge gathered during the initial modeling is used to identify a list of features, by functionally decomposing the domain into subject areas. Subject areas each contain business activities, and the steps within each business activity form the basis for a categorized feature list. Features in this respect are small pieces of client-valued functions expressed in the form "<action> <result> <object>", for example: 'Calculate the total of a sale' or 'Validate the password of a user'. Features should not take more than two weeks to complete, else they should be broken down into smaller pieces.

**Plan by feature**
After the feature list is completed, the next step is to produce the development plan; assigning ownership of features (or feature sets) as classes to programmers.

**Design by feature**
A design package is produced for each feature. A chief programmer selects a small group of features that are to be developed within two weeks. Together with the corresponding class owners, the chief programmer works out detailed sequence diagrams for each feature and refines the overall model. Next, the class and method prologues are written and finally a design inspection is held.

**Build by feature**
After a successful design inspection a per feature activity to produce a completed client-valued function (feature) is planned. The class owners develops the code for their classes. After a unit test and a successful code inspection, the completed feature is promoted to the main build.

Milestones
------------------------------
Since features are small, completing a feature is a relatively small task. For accurate state reporting and keeping track of the software development project it is however important to mark the progress made on each feature. FDD therefore defines six milestones per feature that are to be completed sequentially. The first three milestones are completed during the Design By Feature activity, the last three are completed during the Build By Feature activity. To help with tracking progress, a percentage complete is assigned to each milestone. In the table below the milestones (and their completion percentage) are shown. At the point that coding begins a feature is already 44% complete (Domain Walkthrough 1%, Design 40% and Design Inspection 3% = 44%).



| Domain Walkthrough | Design |	Design Inspection |	Code |	Code Inspection |	Promote To Build |
|--------------------|--------|-------------------|------|------------------|------------------|
|         1%  	 		 |   40%  |         3%        | 45%  |        10%       |         1%       |

**Best practices**
Feature-Driven Development is built on a core set of software engineering best practices, all aimed at a client-valued feature perspective.

  - **Domain Object Modeling* consists of exploring and explaining the domain of the problem to be solved. The resulting domain object model provides an overall framework in which to add features.
  - **Developing by Feature**. Any function that is too complex to be implemented within two weeks is further decomposed into smaller functions until each sub-problem is small enough to be called a feature. This makes it easier to deliver correct functions and to extend or modify the system.
  - **Individual Code Ownership**.  Individual class ownership means that distinct pieces or grouping of code are assigned to a single owner. The owner is responsible for the consistency, performance, and conceptual integrity of the class.
  - **Feature Teams**  A feature team is a small, dynamically formed team that develops a small activity. By doing so, multiple minds are always applied to each design decision and also multiple design options are always evaluated before one is chosen.
  - **Inspections** Inspections are carried out to ensure good quality design and code, primarily by detection of defects.
  - **Configuration Management** Configuration management helps with identifying the source code for all features that have been completed to date and to maintain a history of changes to classes as feature teams enhance them.
  - **Regular Builds** ensure there is always an up to date system that can be demonstrated to the client and helps highlighting integration errors of source code for the features early.
  - **Visibility of progress and results** By frequent, appropriate, and accurate progress reporting at all levels inside and outside the project, based on completed work, managers are helped at steering a project correctly.
  
  Activities and sub-activities
  ----------------------------------------
  
| Activity               | Sub-activity |	Description      |
|------------------------|--------------|------------------|
|  Develop Overall Model |   Form Modeling Team           |        The MODELING TEAM comprises permanent members from the domain and development areas, specifically the domain experts and the chief programmers. Other project staff members are then rotated through the modeling sessions so that everyone gets a chance to participate and to see the process in action.          |
||Conduct Domain Walk-through|A domain expert gives a DOMAIN OVERVIEW of the domain area to be modeled. This should also include information that is related to this DOMAIN AREA but not necessarily a part of its implementation.|
||Study Documents|Optionally the team studies available REFERENCE or REFERENCED REQUIREMENTS documents such as object models, functional requirements (traditional or use-case format), data models, and user guides.|
||Develop Small Group Models|Forming groups of no more than three, each SMALL GROUP will compose a SMALL GROUP MODEL in support of the domain area. The Chief Architect may propose a ´strawman´ model to facilitate the progress of the teams. A member from each small group presents that groups proposed model for the domain area. The Chief Architect may also propose further model alternatives.|
||Develop Team Model|The MODELING TEAM selects a proposed TEAM MODEL or composes a model by merging ideas from the proposed models.|
||Refine Overall Object Model|Every so often, the OVERALL MODEL, consisting of an overall SEQUENCE DIAGRAM and a CLASS DIAGRAM, is REFINED with the new model shapes produced by iterations of the ‘Develop Team Model’ task above.|
||Write Model Notes|EXPLANATORY NOTES on detailed or complex model shapes and on significant model alternatives are made for future reference by the project.|
|Build Feature List|Form Features List Team|he FEATURE LIST TEAM comprises the chief programmers from the MODELING TEAM in the process ‘Develop Overall Model’.|
||Build Features List|he FEATURE LIST TEAM shall identify the FEATURE LIST using the knowledge obtained from the process ‘Develop Overall Model’. This is a simple functional decomposition into SUBJECT AREAS that come from the partitioning of the domain by the domain experts for their domain area walkthroughs in the process ‘Develop Overall Model’. It is decomposed into SUBJECT AREAS that comprise BUSINESS ACTIVITIES that comprise BUSINESS ACTIVITY steps (FEATURES).|
|Plan By Feature|Form Planning Team|The PLANNING TEAM comprises the development manager plus the chief programmers|
||Determine Development Sequence|The main tasks in the process ‘Plan By Feature’ are not a strict sequence. Like many PLANNING activities they are considered together, with REFINEMENTS made from one or more tasks and then considering the others again. The PLANNING TEAM shall assign a DATE (month and year only) for completion of each BUSINESS ACTIVITY. The identification of the BUSINESS ACTIVITY and the completion DATE (and thus the DEVELOPMENT SEQUENCE) is based on:   Dependencies between FEATURES in terms of CLASSES involved;   Balancing load across CLASS OWNERS;   The complexity of the FEATURES to be implemented;   Bringing forward high-risk or complex BUSINESS ACTIVITIES;   Consideration of any external (visible) milestones such as betas, previews, feedback checkpoints and the "whole products" that satisfy such milestones.|
||Assign Business Activities to Chief Programmers|The PLANNING TEAM shall assign chief programmers as owners of BUSINESS ACTIVITIES. The assignment is based on:   The DEVELOPMENT SEQUENCE;   Dependencies between FEATURES in terms of CLASSES involved;   Balancing load across CLASS OWNERS (remember that chief programmers are also CLASS OWNERS);   The complexity of the FEATURES to be implemented.|
||Assign Classes to Developers|The PLANNING TEAM shall assign developers as CLASS OWNERS. Developers own multiple CLASSES. The assignment of CLASSES to developers is based on:Balancing load across developers;The complexity of the CLASSES;The usage (e.g. high-use) of the CLASSES;The DEVELOPMENT SEQUENCE.|
||Design By Feature|Form Feature Team|
||Conduct Domain Walk-through|The domain expert gives a DOMAIN OVERVIEW of the domain area for the FEATURE to be designed. This should also include domain information that is related to the FEATURE but not necessarily a part of its implementation. This is an optional task based on the complexity of the FEATURE and/or its interactions.|
||Study Referenced Documents|The FEATURE TEAM studies the REFERENCED REQUIREMENT(S) for the feature to be designed, all COVERING MEMOS, screen designs, external system interface specifications and any other supporting documentation. This is an optional task based on the complexity of the FEATURE and/or its interactions.|
||Develop Sequence Diagram(s)|Develop the SEQUENCE DIAGRAM(S) required for the FEATURE to be designed. The diagram files should be checked into the version control system. Any ALTERNATIVE DESIGNS, design decisions, requirements clarifications and EXPLANATORY NOTES are also recorded and written up in the DESIGN ALTERNATIVES section of the DESIGN PACKAGE.|
||Refine Object Model|The Chief Programmer creates a FEATURE TEAM Area for the FEATURE(S). This area is either a directory on the file server or a directory on their PC that is backed up to the server by the Chief Programmer as required or utilizes work area support in your version control system. The purpose of the FEATURE TEAM Area is that work in progress by the FEATURE TEAM can be shared and is visible amongst the FEATURE TEAM but is not visible to the rest of the project. The Chief Programmer makes some REFINEMENTS on the model to add new / updated CLASSES, methods, attributes and/or to make changes to existing CLASSES, methods or attributes based on the SEQUENCE DIAGRAM(S) defined for the FEATURE(S). This results in the implementation language source files being updated in the FEATURE TEAM Area. The Chief Programmer creates model diagrams in a publishable format. These files should be checked into the version control system and submitted for publishing on the project intranet.|
||Write Class and Method Prologue|Using the updated implementation language source files from the ‘Refine Object Model’ task in the shared FEATURE TEAM Area, the development owner of each CLASS writes the CLASS AND METHOD PROLOGUE for each item defined by the FEATURE and SEQUENCE DIAGRAM(S). This includes parameter types, return types, exceptions and messages. Once each developer has completed this task, the Chief Programmer generates the API documentation using <your tool> and submits it for publication on the project intranet.|
||Design Inspection|A design inspection with the FEATURE TEAM members or with other project members is held. The decision to inspect within the FEATURE TEAM or with other project team members is that of the Chief Programmer. On acceptance a TODO TASK LIST is generated per affected CLASS, and each team member adds their tasks to their calendar task list. The Chief Programmer must also merge changes from the shared FEATURE TEAM Area into the change control system.|
|Build By Feature|Implement Classes and Methods|The development CLASS owners will perform the IMPLEMENTATION of the items necessary to satisfy the requirements of their CLASS for this FEATURE.|
||Inspect Code|A CODE INSPECTION with the FEATURE TEAM members or with other project members is held either before or after the unit test task. The decision to inspect within the FEATURE TEAM or with other project team members is that of the Chief Programmer. The decision to inspect before or after unit test is that of the Chief Programmer.|
||Conduct Unit Test|The development CLASS owner tests their code to ensure all requirements of their CLASS are satisfied. The Chief Programmer determines what FEATURE TEAM-level unit testing is required (if any). That is, if any testing across the CLASSES developed for this FEATURE is required.|
||Promote to Build|PROMOTION to the BUILD of CLASSES is only possible after a successful CODE INSPECTION. The Chief Programmer tracks the individual CLASSES being promoted, through feedback from the developers, and is the integration point for the entire FEATURE.|
