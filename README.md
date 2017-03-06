#Lumbergh

Lumbergh is a project management tool for engineers and non-engineers who have a love/hate relationship with process.

## Aspirational Goals

* Free-form metadata allows the tool to be process-agnostic
* A low-friction, command-line tool allows engineers to mutate the plan
* A simple export format allows consumption and analysis by non-engineers
* A rich graph export format enables full programmatic access to the plan
* Supports large (10+ engineers) software projects

## Design Choices

### A Version-Controlled Project Plan "Golden Copy"

* The golden copy of the project plan lives alongside source code
* The filesystem tree is used to encode a hierarchy of deliverables
* Shell scripts in the tree are used to encode acceptance criteria
* Symbolic links are used to declare non-decompositional dependencies 
* Schemaless JSON files are used to store metadata about the deliverable

### A Low-Friction Command-Line Tool for Engineers and Non-Engineers

* An interactive mode to navigate and mutate the plan with minimal keystrokes
* An intuitive non-interactive command set for exporting 
* Not-mandatory, but those who want to edit the files manually get a linter
