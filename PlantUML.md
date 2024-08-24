 PlantUML

# 00 Quick Start

## Local Installation

### installation FAQ

## Command Line Operations

### Create "Hello World" in Sequence Diagram

## Some resources

### PlantUML Project in GitHub

### PlantUML Language Reference Guide

### PlantUML cheatsheet

### PlantUML 101

### PlantUML Beginner's Guide

### Pladitor - out-of-the-box PlantUML diagram editor

### Ashley's PlantUML Doc

### Hitchhiker's Guide to PlantUML

### Real World PlantUML

## PlantUML Implementation

### Pure JavaScript Implementation

### PlanUML Web Server

### Node.js Model and CLI for running PlantUML

## PlantUML Forum

# UML Related Diagrams

## Structural (Static) UML Modeling

### 02 Use Case Diagram

#### 2.01 Usecases

##### keyword: usecase
 (see:usecase: ( u ))
#### 2.02 Actors

##### keyword: actor
 (see:actor: : a :)
#### 2.03 Change Actor Style

##### skinparam actorStyle

##### Stick man (by default)

##### Awesome man (c4 style)

##### Hollow man

#### 2.04 Usecases description

##### -- (dashes)

##### .. (periods)
 
'== (equals)

##### __ (underscores)

#### 2.05 Use package

##### package PackageName {}

##### rectangle Name {}

#### 2.06 Basic example

##### arrow: ->, --> and more

#### 2.07 Extension

##### symbol: <|--

##### Mapping to Class Diagram's Generalization Relationship
 (see:Mapping to ArchiMate's Specialization Relationship)
##### Mapping to ArchiMate's Specialization Relationship

#### 2.08 Using notes

##### note left of

##### note right of

##### note top of

##### note bottom of

#### 2.09 Stereotypes
 (see:3.09 Notes and Stereotypes)
##### << and >>

#### 2.10 Changing arrows direction
 (see:3.26 Changing Arrows Orientation)
##### --> or ..>

##### <-- or <..

##### -left-> or -l-> or -le->

#### 2.11 Splitting diagrams

##### keyword: newpage

#### 2.12 Left to Right Direction

#### 2.13 Skinparam

##### In the diagram definition part

##### In an included file

##### In a configuration file

#### 2.14 Complete example

#### 2.15 Business Use Case

##### 2.15 1 Business Usecase

##### 2.15.2 Business Actor

#### 2.16 Change Arrow Color and Style (inline style)

#### 2.17 Change Element Color and Style (inline style)

#### 2.18 Display JSON Data on Usecase Diagram
 (see:11 Display JSON Data)
##### 2.18.1 Simple Example

##### Work with JSON

### 03 Class Diagram

#### Group 1: Notation Definition

##### 3.01 Declaring Element

###### Class

###### Interface
 (see:interface: () i)
##### 3.02 Relations between Classes

###### Extension Relation

###### Composition Relation

###### Aggregation Relation

##### 3.03 Label on Relations

###### use : followed by text of the label

###### use "" for cardinality on each side of relation

##### 3.04 Using Non-Letters in
Element Names and Relation Labels

###### Use the "as" keyword

###### Put "" around the class name

###### 3.04.1 Starting names with $

#### Group 2: Basis on Class Body

##### 3.05 Adding Methods

###### Use ":" follow by the field's or method's name

###### {field}, {method}

##### Real Example: Customer Shopping class diagram

##### 3.06 Defining Visibility

###### turn off:
skinparam classAttributeIconSize 0

* -: Private

* +: Public

* #: Protected

* ~: package private

##### 3.07 Abstract and Static

- In UML, we indicate a class is static by underlining its name in the first compartment of the class diagram.We can similarly indicate operations and methods are static by underlining the entire line referring to them.
- To indicate a class is abstract, we italicize its name. Abstract methods are also indicated by italicizing the entire line referring to them.


###### static method: {static}

###### abstract method: {abstract}

##### 3.08 Advanced Class Body

###### --

###### ..
 
''==

###### __

#### Group 3: Notes in Class Diagram

##### 3.09 Notes and Stereotypes

##### 3.10 More on Notes

###### <b>, <u>, <i>

###### <s>, <del>, <strike>

###### <font color="#AAAAAA"> or <font color="colorname">

###### <color:#AAAAAA> or <color:colorname>

###### <size:nn> to change font size, in pixel

###### <img src="file"> or <img:file>

##### 3.11 Note on Field or Method

###### 3.11.1 Constraint

###### 3.11.2 Note on Field or Method

###### 3.11.3 Note on Method with the Same Name

##### 3.12 Note on Links

#### Group 4: Class and Interface

##### 3.13 Abstract Class and Interface

###### keyword: abstract

###### keyword: abstract class

###### keyword: interface

###### keyword: annotation

###### keyword: enum

##### 3.14 Hide Attributes, Methods...

###### command: hide/show

###### hide empty members

##### 3.15 Hide Classes

###### show/hide

##### 3.16 Remove Classes

###### remove/hide/restore with $tags

##### 3.17 Hide, Remove or Restore Tagged Elements or Wildcard

##### 3.18 Hide or Remove Unlinked Class

###### hide @unlinked

###### remove @unlinked

#### Group 5: Use Generics and Specific Spot

##### 3.19 Use Generics

###### Usually generics are represented as classifier's template parameter.

###### Generics in Java have been around for a while but support for mapping generically specified artifacts in UML to their Ecore representation is new to UML2 2.1

###### UML Parameterized Class

###### bracket < and >

##### 3.20 Specific Spot

###### spot characters: C, I, E, A

###### within stereotype <<>>, 1) (), 2) single character, 3) color code or color name

#### Group 6: Packages

A package in the Unified Modeling Language is used "to group elements, and to provide a namespace for the grouped elements".[1] A package may contain other packages, thus providing for a hierarchical organization of packages.



Pretty much all UML elements can be grouped into packages. Thus, classes, objects, use cases, components, nodes, node instances etc. can all be organized as packages, thus enabling a manageable organization of the myriad elements that a real-world UML model entails.


##### 3.21 Packages

###### keyword: package

###### package definitions can be nested

##### 3.22 Packages Style

###### command: skinparam packageStyle

###### using stereotype on package

* <<Node>>

* <<Rectangle>>

* <<Folder>>: default

* <<Frame>>

* <<Cloud>>

* <<Database>>

###### can define links between packages

##### 3.23 Namespaces

##### 3.24 Automatic Package Creation

###### define another separator: set spearator ???

###### disable automatic namespace creation: set separator none

#### Group 7: Arrows and Association

##### 3.25 Lollipop Interface
 (see:Lollipop: ball and socket)
###### Discussion: Interface consumption socket

###### Forum: #2259 - using circle

###### Ball and Socket by Martin Fowler

##### 3.26 Changing Arrows Orientation

##### 3.27 Association Classes
 
defineassociation class after a relation

 
defineassociationin another direction


###### How to associate more than 1 classes to one same relation?

##### 3.28 Association on Same Class

#### Group 8: Styles

##### 3.29 Skinparam

##### 3.30 Skinned Stereotypes

###### discussion #16549

###### discussion #16650

##### 3.31 Color Gradient

##### 3.32 Help on Layout

###### keyword: together

###### use hidden links to force the layout

##### 3.33 Splitting Large Files
 
use thepage (hpages)x(vpages) to split images


###### discussion #3876

##### 3.34 Extends and Implements
 
keyword:implements


* UML realization relationship

UML realization relationships between the definition and implementations of an interface (the equivalent of Java implements)



Although Java does not support multiple inheritance in the same way as languages such as C++, it does support the idea of implementation of multiple interfaces. The form of inheritance represented by theimplements  keyword in Java is inheritance of interface only. This type of inheritance is sometimes calledsub-typing.

In UML, the relationship between a class implementing an interface and the interface definition is called arealization relationship, and it is drawn as a dashed line with a closed arrowhead from the implementing class to the interface. Interfaces are drawn using the same symbol as a class but with an additional keyword <<interface>> above the class name.

 
keyword:extends


* UML generalization / specialization relationship

UML generalization relationships, used to indicate that one interface extends one or more others.



Interfaces can extend one or more other interfaces. A UML generalization relationship (solid line with closed arrowhead) is used to represent this sort of relationship.


###### Article: Inheritance and Interfaces in Java and UML

###### Interface in Java

##### 3.35 Bracketed Relations (linking or arrow) Style
   syntax: class1 -[style]-> class2

###### 3.35.1 Line Style

###### 3.35.2 Line Color

###### 3.35.3 Line Thickness

###### 3.35.4 Mix

* Question raised: #19008

##### 3.36 Change Relations (linking or arrow) color and style (inline style)

##### 3.37 Change Class Color and Style (inline style)

###### #color ##[style]color

###### #[color|back:color];head:color;line:color;line.[bold|dashed|dotted];text:color

#### Group 9: Others

##### 3.38 Arrow from/to Class Members

##### 3.39 Grouping Inheritance Arrow Heads

###### 3.39.1 GroupInheritance 1 (no grouping)

###### 3.39.2 GroupInheritance 2 (grouping from 2)

###### 3.39.3 GroupInheritance 3 (grouping only from 3)

###### 3.39.4 GroupInheritance 4 (grouping only from 4)

##### 3.40 Display JSON Data on Class or Object Diagram
 (see:11 Display JSON Data)
##### 3.41 Packages and Namespaces Enhancement

### 04 Object Diagram

An object diagram is a graphical representation that showcase objects and their relationshipsat a specific moment in time.

It provides asnapshot of the system's structure, capturing thestatic view of the instances present and their associations.


#### 4.01 Definition of Objects

#### 4.02 Relations between Objects

##### Extension: <|--

##### Composition: *--

##### Aggregation: o--

#### 4.03 Associations Objects

##### diamond

#### 4.04 Adding Fields

#### 4.05 Common Features with Class Diagrams

##### Hide attributes, methods
 (see:3.14 Hide Attributes, Methods...)
##### Defines notes
 (see:Group 3: Notes in Class Diagram)
##### Use packages
 (see:Group 6: Packages)
##### Skin the output
 (see:Group 8: Styles)
#### 4.06 Map Table or Associative Array

##### keyword: map and Separator: =>

#### 4.07 Program (or project) evaluation and review technique (PERT) with Map

##### Sample PERT

#### 4.08 Display JSON Data on Class or Object Diagram
 (see:11 Display JSON Data)
### 07 Component Diagram

#### Basis

##### 7.01 Components
 (see:component: [ e ])
###### 7.01.01 Naming Exceptions

###### Ref: ArchiMate 3.2 Specification

##### 7.02 Interfaces
 (see:interface: () i)
##### 7.03 Basic Example

#### 7.04 Using Notes

##### Use "note direction of" to define notes related to a single object

##### defined with the "note" and "end note" keyword, then link to other objects using the ".." symbol or arrow symbols

#### 7.05 Grouping Components

#### Component Notation
 (see:7.14 Specific SkinParameter)
##### 7.07 Use UML2 Notation

###### by default from v1.2020.13-14 UML2 notation is used

##### 7.08 Use UML1 Notation

##### 7.09 Use Rectangle Notation (remove UML notation)

#### Styles

##### 7.06 Changing Arrows Direction

##### 7.10 Long Description

###### Question raised to Forum: #19128

##### 7.11 Individual Colors

##### 7.12 Using Sprite in Stereotype

###### Piskel - free online sprites editor

###### Only 4, 8, 16 graylevel are allowed

##### 7.13 Skinparam

##### 7.14 Specific SkinParameter

#### Display Related

##### 7.15 Hide or Remove Unlinked Component

###### By default, all components are displayed

###### Can hide @unlinked components

###### Or can remove @unlinked components

##### 7.16 Hide, Remove or Restore Tagged Component or Wildcard

###### Question on why cannot restore tag after "remove *"

##### 7.17 Display JSON Data on Component Diagram

###### Question asked in Forum

#### 7.18 Port [port, portIn, portOut]

##### Lollipop: ball and socket

###### Interface symbols with a complete circle at their end represent an interface that the component provides - this "lollipop" symbol is shorthand for a realization relationship of an interface classifier

* [a] --0 [b]

###### Interface symbols with only a half circle at their end (a.k.a sockets) represent a interface that the component require

* [a] --( [b]

###### Interface combines half circle and complete circle in the middle

* [a] --(0-- [b]

##### Sample: IBM - the component diagram - Figure 7

### 08 Deployment Diagram

#### Declaring

##### 8.01 Declaring Element

##### 8.02 Declaring Element (using short form)

###### actor: : a :

###### component: [ e ]

###### interface: () i

###### usecase: ( u )

#### Linking/Arrow and Arrow / Elements Styles

##### 8.03 Linking or Arrow

###### Simple Link

###### Link with Arrow

###### Lollipop Style

##### 8.04 Bracketed Arrow Style

###### Line Style: bold, dashed, dotted, hidden, plain

###### Line Color: [#colorName]

###### Line Thickness: [thickness=(1,2,4,8,16)]

###### Mix in bracketed style portion

##### 8.05 Change Arrow Color and Style (inline style)

##### 8.06 Change Element Color and Style (inline style)

#### Packages or Nested

##### 8.07 Nestable Elements

##### 8.08 Packages and Nested Elements

#### Alias and Styles

##### 8.09 Alias

##### 8.10 Round Corner

##### 8.11 Specific SkinParameter

#### Appendix

##### 8.12 Appendix: All type of Arrow Line

##### 8.13 Appendix: All type of arrow head or '0' arrow

##### 8.14 Appendix: Test of inline style on all element

##### 8.15 Appendix: Test of style on all element

##### 8.16 Appendix: Test of stereotype with style on all element

#### Others

##### 8.17 Display JSON Data on Deployment Diagram

##### 8.18 Mixing Deployment (Usecase, Component, Deployment) element within a Class or Object Diagram

##### 8.19 Port [port, portIn, portOut]
 (see:9.10 Point [entryPoint, exitPoint]9.11 Pin [inputPin, outputPin])
## Behavioral (Dynamic) UML Modeling

### 01 Sequence Diagram

#### Part 1 - Basis

##### Characteristics of Sequence Diagram

###### Intuitive Syntax

###### Text-to-Graphic Correlation

###### Efficient Crafting Process

###### Visualization While Drafting

###### Easy Edits and Revisions

##### 1.1 Basic Examples

##### 1.2 Declaring Participant

##### 1.3 Declaring Participant on Multiline

###### Ref. QA 15232

#### Part 2

##### 1.4 Use Non-Letters in Participants

##### 1.5 Message to Self

##### 1.6 Text Alignment

###### skinparam sequenceMessageAlign
or sequenceMessageAlignment

* left

* right

* center

###### 1.6.1 Text of Response Message below the Arrow

* responseMessageBelowArrow (boolean)

#### Part 3

##### 1.7 Change Arrow Style
 (see:1.29 Incoming and Outgoing Messages)
##### 1.8 Change Arrow Color

###### -[#color]>

##### 1.9 Message Sequence Numbering

###### autonumber

###### autonumber "number"

###### autonumber "number" step(default=1)

###### autonumber "style/color"

###### autonumber resume/stop

###### use numbering as variable: %autonumber%
 (see:Part 5 - Message Notes)
##### 1.10 Page Title, Header and Footer

###### keyword: title

###### keyword: header, footer

#### Part 4

##### 1.11 Splitting Diagrams
 (see:2.11 Splitting diagrams)
###### keyword: newpage

##### 1.12 Grouping Message

###### Frames Around Fragments (Ashley's)
 
All frame keywordsmust have a corresponding"end" to signal where the frame ends


* Frames can be nested

* You cannot use a note within a frame

###### keywords

* alt: used to show one or more alternative sequences that can happen.

  + used to describe alternative scenarios of a workflow, only one of the options will be executed

* else: the default sequence in a list of alternative sequences

* opt: an optional sequence, it either happens or not
 (see:alt: used to show one or more alternative sequences that can happen.)
  + used to describe an optional step in the workflow

* loop: shows a sequence that loops

* par: shows a parallel sequence

* break: shows that a sequence breaks, it stops (does not perform) any of the remaining sequence does this instead

* critical: a fragment of a sequence that cannot be "interleaved" by other fragments (e.g. parallel fragments, etc.)

* group: allows you to fully specify the frame name

##### 1.13 Secondary Group Label

###### only for group, between [ and ]

#### Part 5 - Message Notes
 (see:2.08 Using notes)
##### 1.14 Notes on Messages

###### keywords

* note left / right
 
end note for multiline note


##### 1.15 Some Other Notes

###### relative

* note left of

* note right of

* note over

##### 1.16 Changing Notes Shape [hnote, rnote]

##### 1.17 Note over all Participants [across]

###### note cross

##### 1.18 Several Notes Aligned at the Same Level [/]

#### Part 6

##### 1.19 Creole and HTML

###### Creole Cheat Sheet

###### Question raised in Forum

##### 1.20 Divider or Separator

###### Use == separator to divide diagram into logical steps

##### 1.21 Reference

###### keyword: ref over

#### Part 7

##### 1.22 Delay

###### symbol: ...

###### ... text ...

##### 1.23 Text Wrapping

###### manually add \n in the text

###### use "maxMessageSize (unit: pixel)" setting

##### 1.24 Space

###### manually use ||| to indicate some spacing

###### specify a number of pixel to be used

#### Part 8

##### 1.25 Lifeline Activation and Destruction
 (see:Activate the target: ++Deactivate the source: --Destroy an instance of the target: !!1.32 Stereotypes and Spots)
##### 1.26 Return

###### syntax: return label

#### Part 9

##### 1.27 Participant Creation
 (see:1.25 Lifeline Activation and DestructionCreate an instance of the target: **)
###### keyword: create

##### 1.28 Shortcut Syntax

###### Activate the target: ++

###### Deactivate the source: --

###### Create an instance of the target: **

###### Destroy an instance of the target: !!

#### Part 10

##### 1.29 Incoming and Outgoing Messages

###### using "[" and "]"

##### 1.30 Short Arrows for Incoming and Outgoing Messages using ?

#### Part 11

##### 1.31 Anchors and Duration

###### keyword: teoz

##### 1.32 Stereotypes and Spots
 (see:2.09 Stereotypes)
###### stereotype: << and >>

* guillemet character as default

a pair of punctuation marks in the form of sideways double chevrons, « and », used as quotation marks in a number of languages


* skinparam guillemet false

###### spotted characters: (X,color)

#### Part 12

##### 1.33 More Information on Titles
 
Usecreole formatting in the title


###### Add newline using \n in title description
 
Define title on multi-lines usingtitle  andend title


##### 1.34 Participants Encompass
 
box andend box


###### Can add option title / bgcolor after box keyword

##### 1.35 Removing Foot Boxes

###### hide footbox keyword

#### Part 13

##### 1.36 Skinparam
 (see:1.39 Specific SkinParameter)
###### "skinparam" command

###### All Skin Parameters with Samples

##### 1.37 Changing Padding

#### Part 14

##### 1.38 Appendix:
Examples of All Arrow Type

###### 1.38.1 Normal Arrow

###### 1.38.2 Itself Arrow

###### 1.38.3 Incoming and Outgoing Messages (with '[', ']')

* 1.38.3.1 Incoming Messages (with '[')

* 1.38.3.2 Outgoing Messages (with ']')

###### 1.38.4 Short Incoming and Outgoing Messages (with '?')

* 1.38.4.1 Short Incoming Messages (with '?')

* 1.38.4.2 Short Outgoing Messages (with '?')

###### 1.38.5 Outgoing Message (with ']')

###### 1.38.6 Short Incoming and Outgoing Message (with '?')

###### 1.38.7 Short Incoming (with '?')

###### 1.38.8 Short Outgoing (with '?')

#### Part 15

##### 1.39 Specific SkinParameter

###### 1.39.1 By default

###### 1.39.2 Lifeline Strategy

###### 1.39.3 Style Strictuml

#### Part 16

##### 1.40 Hide Unlinked Participant

##### 1.41 Color a Group Message

##### 1.42 Mainframe

###### QA-4019

##### 1.43 Slanted or Odd Arrows

###### (nn) option

### 05 Activity Diagram (legacy)

#### 5.01 Simple Action
 (see:6.01 Simple Action6.02 Start/Stop/End)
##### use (*) for starting point and ending point

##### use (*top) to force starting point to be at the top

##### use --> for arrows

#### 5.02 Label on Arrows

##### using [ and ] after --> for labeling on arrows

#### 5.03 Changing Arrow Direction
 (see:7.06 Changing Arrows Direction)
##### e.g. -down->

#### 5.04 Branches
 (see:6.03 Conditional6.04 Switch and Case [switch, case, endswitch]6.05 Conditional with Stop on an Action [kill, detach])
##### use if/then/else keyword

#### 5.05 More on Branches

#### 5.06 Synchronization

##### use === code === to display sync bars

#### 5.07 Long Action Description

##### <size:xx></size>: font size

##### <color:###></color>: font color

##### <b></b>: font bold

##### <i></i>: font italic

##### <image:sourcename>: insert image

#### 5.08 Notes
 (see:6.12 Notes)
##### Add notes just after the description of activity
 
usingendnote if want to have multiline note


#### 5.09 Partition
 (see:6.18 Grouping or Partition)
##### keyword: partition

##### close the partition definition using closing bracket }

#### 5.10 Skinparam

##### In diagram definition

##### In an included file

##### In a configuration file

#### 5.11 Octagon

##### skinparam activityShape octagon

#### 5.12 Complete Example

### 06 Activity Diagram (New Syntax)

#### 6.01 Simple Action

##### Activities label starts with : and ends with ;

#### 6.02 Start/Stop/End
 
Usestart keywords to denote the beginning

 
UseStoporEnd  to denote the end of a diagram


#### Branches

##### 6.03 Conditional
 (see:9.08 Conditional [choice])
###### Basic Syntax

* if (...) then (...)

* if (...) is (...) then

* if (...) equals (...) then

###### 6.03.01 Several Tests (horizontal Mode)

* elseif keyword to have several tests

###### 6.03.02 Several Tests (Vertical Mode)
 
command!pragma useVerticalIf on  to have the tests in vertical mode

 
Use the-P command-line option to specify the pragma:

java -jar plantuml.jar -P useVerticalIf=on


##### 6.04 Switch and Case [switch, case, endswitch]

##### 6.05 Conditional with Stop on an Action [kill, detach]

###### stop: stop action on a if loop

###### kill or detach: stop at the precise action

##### 6.08 Goto and Label Processing [label, goto]

###### label <label_name>

###### goto <label_name>

#### Looping

##### 6.06 Repeat Loop

###### 6.06.01 Simple Repeat Loop

* "repeat" and "repeat while" keyword

* "repeat" and "backward" keyword

###### 6.06.02 Repeat Loop with Repeat Action and Backward Action
 (see:6.09.02 While Loop with Backward Action)
##### 6.07 Break on a Repeat Loop [break]

##### 6.09 While Loop

###### 6.09.01 Simple While Loop

* use while and endwhile keywords

###### 6.09.02 While Loop with Backward Action

* use backward keyword

###### 6.09.03 Infinite While Loop

#### Parallel vs Split Processing

##### 6.10 Parallel Processing [fork, fork again, end fork, end merge]

###### 6.10.01 Simple fork

###### 6.10.02 fork with end merge

###### 6.10.03 Label on end fork (or UML joinspec)

###### 6.10.04 Other example

##### 6.11 Split Processing

###### 6.11.01 Split

* use split, split again and end split keywords

###### 6.11.02 Input split (multi-start)

* use hidden arrows to make an input split (multi-start)

###### 6.11.03 Output split (multi-end)

* use kill or detach to make an output split (multi-end)

#### Styling and Formatting

##### 6.12 Notes

##### 6.13 Colors

###### Can specify a color for some activities

###### Can use gradient color

##### 6.14 Lines without Arrows

###### skinparam ArrowHeadColor none

##### 6.15 Arrows

###### -> notation

##### 6.16 Connector

###### use () to denote connector

##### 6.17 Color on Connector

#### 6.18 Grouping or Partition

##### 6.18.01 Group

##### 6.18.02 Partition

##### 6.18.3 Group, Partition, Package, Rectangle or Card

#### 6.19 Swimlanes

##### use pipe | define swimlanes

##### can add if conditional or repeat or while loop within swimlanes

##### Alias: |[#<color>|]<swimlane_alias>| <swimlane_title>

#### 6.20 Detach or Kill [detach, kill]

#### 6.21 SDL (Specification and Decription Language)

##### SDL Forum

##### Overview of SDL

###### Also available in GitHub

##### 6.21.01 Table of SDL Shape Name

##### 6.21.02 SDL using Final Separator (Deprecated form)

##### 6.21.03 SLD using Normal separator and Stereotype (Current official form)

#### 6.22 Complete Example

#### 6.23 Condition Style

##### 6.23.01 Inside Sytle (by default)

##### 6.23.02 Diamond Style

###### skinparam conditionStyle diamond

##### 6.23.03 InsideDiamand (or Foo1) Style

###### skinparam conditionStyle InsideDiamond

#### 6.24 Condition End Style

##### 6.24.01 Diamond Style (by default)

###### skinparam ConditionEndStyle diamond

##### 6.24.02 Horizontal Line (hline) Style

###### skinparam ConditionEndStyle hline

#### 6.25 Using (global) Style

##### 6.25.01 Without Style (by default)

##### 6.25.02 With Style

### 09 State Diagram

#### 9.01 Simple State

##### What is State?

###### Rumbaugh defines that: "A State is an abstraction of the attribute values and links of an object. Sets of values are grouped together into a state according to properties that affect the gross behavior of the object."

##### State Notation

##### State Diagram vs Activity Diagram

#### 9.02 Change State Rendering

#### 9.03 Compsite State

##### Internal Sub-state

##### Sub-state to sub-state

#### 9.04 Long Name

#### 9.05 History [[H], [H*]]
 
Unless otherwise specified, when a transition enters a composition state, the action ofthe nested state machine starts over again at the initial state (unless the transition targets a substate directly)

 
History states allow the state machine tore-enter the last substate that was active prior to leaving  the composition state.


#### 9.06 Fork [fork, join]

#### 9.07 Concurrent State [--, ||]

##### Horizontal separator --

##### Vertical separator ||

#### 9.08 Conditional [choice]

##### Question about <<sdlreceive>>

##### Source code for <<sdlreceive>>

#### 9.09 Stereotypes full example [start, choice, fork, join, end]

##### /plantuml/statediagram/command/CommandCreateState.java

###### <<start>>: LeafType.CIRCLE_START

###### <<choice>>: LeafType.STATE_CHOICE

###### <<fork>>: LeafType.STATE_FORK_JOIN

###### <<join>>: LeafType.STATE_FORK_JOIN

###### <<end>>: LeafType.CIRCLE_END

###### <<history>>: LeafType.PSEUDO_STATE

###### <<history*>>: LeafType.DEEP_HISTORY

##### /plantuml/svek/GeneralImageBuilder.java

###### <<sdlreceive>>: EntityImageState2(leaf, skinParam, umlDiagramType.getStyleName())

#### Input & Output notation

##### 9.10 Point [entryPoint, exitPoint]

##### 9.11 Pin [inputPin, outputPin]

##### 9.12 Expansion [expansionInput, expansionOutput]

#### styles

##### 9.13 Arrow direction

##### 9.14 Change line color and style

##### 9.18 Inline color

##### 9.19 Skinparam

##### 9.20 Changing style

##### 9.21 Change state color and style (inline style)

#### notes

##### 9.15 Note

##### 9.16 Note on link

##### 9.17 More in Notes

#### 9.22 Alias

#### 9.23 Display JSON Data on State diagram

### 10 Timing Diagram

#### 10.01 Declaring element or participant

##### analog

##### binary

##### clock

##### concise

##### robust

##### change: @

##### verb: is

#### 10.02 Binary and Clock

#### 10.03 Adding message

#### 10.04 Relative time

##### use relative time wiht @

#### 10.05 Anchor Points

#### 10.06 Participant Oriented

#### 10.07 Setting Scale

#### 10.08 Initial state

#### 10.09 Intricated state

##### Intricated or undefined robust state

##### Intricated or undefined binary state

#### 10.10 Hidden state

#### 10.11 Hide time axis

#### 10.12 Using Time and Date

#### 10.13 Adding constraint

#### 10.14 Highlighted period

#### 10.15 Using Notes

#### 10.16 Adding Texts

#### 10.17 Complete example

#### 10.18 Digital Example

#### 10.19 Adding Color

#### 10.20 Using (global) style

#### 10.21 Applying Colors to specific lines

#### 10.22 Compact mode

##### By default
 
Global mode with modecompact

 
Local model with onlycompact  on element


# Non-UML Diagrams

## 11 Display JSON Data

### 11.1 Complex Example

### 11.2 Highlight Parts

### 11.3 Using Different Styles for Highlight

### 11.4 JSON Basic Element

#### Synthesis of all JSON basic element

### 11.5 JSON Array or Table

#### Array Type

#### Minimal Array or Table

#### Number Array

#### String Array

#### Boolean Array

### 11.6 JSON Numbers

### 11.7 JSON Strings

#### JSON Unicode

#### JSON Two-Character Escape Sequence

### 11.8 Minimal JSON Examples

### 11.9 Empty Table or List

### 11.10 Using (Global) Style

### 11.11 Display JSON Data on Class or Object Diagram

### 11.12 Display JSON Data on Deployment Diagram

### 11.13 Display JSON Data on State Diagram

## 12 Display YAML Data

### 12.1 Complex Example

### 12.2 Specific Key (with symbols or unicode)

### 12.3 Highlight Parts

### 12.4 Using Different Styles for Highlight

### 12.5 Using (Global) Style

## 13 Network Diagram (nwdiag)

### 13.1 Simple Diagram

#### Define a Network

#### Define some Elements or Servers on a Network

#### Full Example

### 13.2 Define Multiple Addresses

### 13.3 Grouping Nodes

#### Define Group inside Network Definitions

#### Define Group outside of Network Definitions

#### Define Several Groups on Same Network

##### Example with 2 Group

##### Example with 3 Groups

### 13.4 Extended Syntax (for network or group)

#### Network

#### Group

### 13.5 Using Sprites

### 13.6 Using OpenIconic

### 13.7 Same Nodes on more than two Networks

### 13.8 Peer Networks

### 13.9 Peer Networks and Group

#### Without Group

#### Group on First

#### Group on Second

#### Group on Third

### 13.10 Add Title, Captain, Header, Footer or Legend on Network Diagram

### 13.11 With or Without Shadow

### 13.12 Change Width of the Network

### 13.13 Other Internal Networks

### 13.14 Using (global) Style

### 13.15 Appendix: Test of all Shapes on Network Diagram (nwdiag)

## 14 Salt (Wireframe)

### 14.1 Basic Widgets

### 14.2 Text Area

### 14.3 Open, Close Droplist

### 14.4 Using Grid [| and #, !, -, +]

### 14.5 Group Box [^]

### 14.6 Using Separator [.., ==, ~~, --]

### 14.7 Tree Widget [T]

### 14.8 Tree Table [T]

### 14.9 Exclosing Brackets [{, }]

### 14.10 Adding Tabs [/]

### 14.11 Using Menu [*]

### 14.12 Advanced Table

### 14.13 Scroll Bars [S, SI, S-]

### 14.14 Colors

### 14.15 Creole on Salt

### 14.16 Pseudo Sprite [<<, >>]

### 14.17 OpenIconic

### 14.18 Add Title, Header, Footer, Caption or Legend

## 15 Archimate Diagram

## 16 Gantt Diagram

## 17 Mindmap

## 18 Work Breakdown Structure (WBS)

## 19 Maths

## 20 Entity Relationship Diagram

# PlantUML as a Language

## 21 Common Commands in PlantUML

## 22 Creole

## 23 Defining the using sprites

## 24 Skinparam command

## 25 Preprocessing

## 26 Unicode

## 27 PlantUML Standard Library

# Add-on and Reference

## Formatting Diagrams with Skinparams, HTML and Creole

## RUP - Rational Unified Process by SWI Group

## A Comprehensive Guide to Sequence Diagram
 (see:01 Sequence Diagram)
## A Comprehensive Guide to Use Case Diagram
 (see:02 Use Case Diagram)
# Other reference

## UML Diagram Type (by visual paradigm)

### Structureal Diagram

#### Composite Structure Diagram

#### Deployment Diagram

#### Package Diagram

#### Profile Diagram

#### Class Diagram

#### Object Diagram

#### Component Diagram

### Behavioral Diagrams

#### Activity Diagram

#### Use Case Diagram

#### State Machine Diagram

#### Interactiion Diagram

##### Sequence Diagram

##### Communication Diagram

##### Interaction Overview Diagram

##### Timing Diagram
