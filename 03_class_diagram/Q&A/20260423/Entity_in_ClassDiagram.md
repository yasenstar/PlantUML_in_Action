# How to Show `Boundary`, `Control` and `Entity` Icons in Class Diagram? (PlantUML)

I got this question and thought it would be quite simple and straighforward initially, while, when trying to replicate the diagramming, I found there're certain PlantUML version & syntax / grammer constraints, finally I can only re-produce in the ~90% alike diagram. This article aims to document my quick journey on all kinds of tries, while it's also one good chance of learning!

- [How to Show `Boundary`, `Control` and `Entity` Icons in Class Diagram? (PlantUML)](#how-to-show-boundary-control-and-entity-icons-in-class-diagram-plantuml)
  - [Background of the Question](#background-of-the-question)
  - [Analysis of the Diagram](#analysis-of-the-diagram)
  - [Try 01: Normal Way by Using Stereotypes.](#try-01-normal-way-by-using-stereotypes)

## Background of the Question

Raised by [Kok Leong Ang](https://www.udemy.com/user/kok-leong-ang/): can PlantUML create the class diagram with Entity, Boundary and Control?

Attached the diagram is as below:

![question_image](img/question_image.png)

## Analysis of the Diagram

Robustness diagrams are written after use cases and before class diagrams.

The question relates to one robustness diagram, including 4 elements in 3 types of the objects:

- Boundary x 1: `FormCreateTourGroup`
- Control x 1: `TourGroupControl`
- Entity x 2 ("TouPackage" is aggregated by "TourGroup")
  - `TourPackage`
  - `TourGroup`

They're also known as Robustness diagram symbols, which help to identify the roles of use case steps and represent usage requirements for the system which are building.

Whereas the Model-View-Controller (MVC) pattern is used for user interfaces, the Entity-Control-Boundary Pattern (ECB) is used for systems.

![boundary-entity-control](img/boundary-entity-control.png)

More information on those objects:
- Entities (model): Objects representing system data, often from the domain model.
- Boundaries (view/service collaborator): Objects that interface with system actors (e.g. a user or external service). Windows, screens and menus are examples of bouindaries that interface with users.
- Controls (controller): Objects that mediate between boundaries and entities. These serve as the glue between boundary elements and entity elements, implementing the logic required to manage the various elements and their interactions. It is important to understand that you may decide to implement controllers within your design as something other than objects - many controllers are simple enough to be implemented as a method of an entity or boundary class for example.

There're 4 rules applying to their communication (adding `Actor` into the context):

1. `Actors` can only talk to `boundary objects`
2. `Boundary objects` can only talk to `controllers` and `actors`
3. `Entity objects` can only talk to `controllers`
4. `Controllers` can talk to `boundary objects` and `entity objects`, and to other `controllers`, but not to `actors`

As below allowed-communication matrix:

| | Entity | Boundary | Controller |
| --- | :---: | :---: | :---: |
| Entity | X | | X |
| Boundary | | | X |
| Controller | X | X | X |

Actually, the **Robustness Diagrams** (or Analysis Diagrams, as they are sometimes called) are just speciflized **Class Diagrams**. 

Also, from diagram in the question, it have certain visibility indicators for methods or fields, below are the four definitions available in PlantUML:

| Character | Icon for Field | Icon for Method | Visibility |
| :---: | :---: | :---: | :---: |
| - | <span style="color:red;">&#9633;</span> (\&#9633;) | <span style="color:red;">&#9632;</span> (\&#9632;) | private |
| # | <span style="color:goldenrod;">&#9671;</span> (\&#9671;) | <span style="color:gold;">&#9670;</span> (\&#9670;) | private |
| ~ | <span style="color:blue;">&#9651;</span> (\&#9651;) | <span style="color:blue;">&#9650;</span> (\&#9650;) | private |
| + | <span style="color:green;">&#9675;</span> (\&#9675;) | <span style="color:green;">&#9679;</span> (\&#9679;) | private |

The way to diagramming the relations between classes are as below:

| Type | Symbol | Drawing |
| :---: | :---: | :---: |
| Extension | <\|-- | <span style="color:#b00020;">◁────</span><br> |
| Composition | *-- | <span style="color:#b00020;">◆────</span><br> |
| Aggregation | o-- | <span style="color:#b00020;">◇────</span> |

## Try 01: Normal Way by Using Stereotypes.

I say Normal Way, since when I create a PlantUML Class Diagram with using certain notations like `Entity`, `Boundary`, and `Control`, I nomrally use specific stereotypes.

PlantUML will automatically render those stereotypes, code as 