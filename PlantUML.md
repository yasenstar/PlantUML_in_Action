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

## 01 Sequence Diagram

### Part 1 - Basis

#### Characteristics of Sequence Diagram

##### Intuitive Syntax

##### Text-to-Graphic Correlation

##### Efficient Crafting Process

##### Visualization While Drafting

##### Easy Edits and Revisions

#### 1.1 Basic Examples

#### 1.2 Declaring Participant

#### 1.3 Declaring Participant on Multiline

##### Ref. QA 15232

### Part 2

#### 1.4 Use Non-Letters in Participants

#### 1.5 Message to Self

#### 1.6 Text Alignment

##### skinparam sequenceMessageAlign
or sequenceMessageAlignment

###### left

###### right

###### center

##### 1.6.1 Text of Response Message below the Arrow

###### responseMessageBelowArrow (boolean)

### Part 3

#### 1.7 Change Arrow Style

#### 1.8 Change Arrow Color

##### -[#color]>

#### 1.9 Message Sequence Numbering

##### autonumber

##### autonumber "number"

##### autonumber "number" step(default=1)

##### autonumber "style/color"

##### autonumber resume/stop

##### use numbering as variable: %autonumber%
 (see:Part 5 - Message Notes)
#### 1.10 Page Title, Header and Footer

##### keyword: title

##### keyword: header, footer

### Part 4

#### 1.11 Splitting Diagrams
 (see:2.11 Splitting diagrams)
##### keyword: newpage

#### 1.12 Grouping Message

##### Frames Around Fragments (Ashley's)
 
All frame keywordsmust have a corresponding"end" to signal where the frame ends


###### Frames can be nested

###### You cannot use a note within a frame

##### keywords

###### alt: used to show one or more alternative sequences that can happen.

* used to describe alternative scenarios of a workflow, only one of the options will be executed

###### else: the default sequence in a list of alternative sequences

###### opt: an optional sequence, it either happens or not
 (see:alt: used to show one or more alternative sequences that can happen.)
* used to describe an optional step in the workflow

###### loop: shows a sequence that loops

###### par: shows a parallel sequence

###### break: shows that a sequence breaks, it stops (does not perform) any of the remaining sequence does this instead

###### critical: a fragment of a sequence that cannot be "interleaved" by other fragments (e.g. parallel fragments, etc.)

###### group: allows you to fully specify the frame name

#### 1.13 Secondary Group Label

##### only for group, between [ and ]

### Part 5 - Message Notes

#### 1.14 Notes on Messages

##### keywords

###### note left / right
 
end note for multiline note


#### 1.15 Some Other Notes

##### relative

###### note left of

###### note right of

###### note over

#### 1.16 Changing Notes Shape [hnote, rnote]

#### 1.17 Note over all Participants [across]

##### note cross

#### 1.18 Several Notes Aligned at the Same Level [/]

### Part 6

#### 1.19 Creole and HTML

##### Creole Cheat Sheet

##### Question raised in Forum

#### 1.20 Divider or Separator

##### Use == separator to divide diagram into logical steps

#### 1.21 Reference

##### keyword: ref over

### Part 7

#### 1.22 Delay

##### symbol: ...

##### ... text ...

#### 1.23 Text Wrapping

##### manually add \n in the text

##### use "maxMessageSize (unit: pixel)" setting

#### 1.24 Space

##### manually use ||| to indicate some spacing

##### specify a number of pixel to be used

### Part 8

#### 1.25 Lifeline Activation and Destruction
 (see:1.32 Sterotypes and Spots)
#### 1.26 Return

##### syntax: return label

### Part 9

#### 1.27 Participant Creation

##### keyword: create

#### 1.28 Shortcut Syntax

##### Activate the target: ++

##### Deactivate the source: --

##### Create an instance of the target: **

##### Destroy an instance of the target: !!

### Part 10

#### 1.29 Incoming and Outgoing Messages

##### using "[" and "]"

#### 1.30 Short Arrows for Incoming and Outgoing Messages using ?

### Part 11

#### 1.31 Anchors and Duration

##### keyword: teoz

#### 1.32 Sterotypes and Spots
 (see:2.09 Stereotypes)
##### << and >>

### Part 12

#### 1.33 More Information on Titles
 
Usecreole formatting in the title


##### Add newline using \n in title description
 
Define title on multi-lines usingtitle  andend title


#### 1.34 Participants Encompass
 
box andend box


##### Can add option title / bgcolor after box keyword

#### 1.35 Removing Foot Boxes

##### hide footbox keyword

### Part 13

#### 1.36 Skinparam
 (see:1.39 Specific SkinParameter)
##### "skinparam" command

#### 1.37 Changing Padding

### Part 14

#### 1.38 Appendix:
Examples of All Arrow Type

##### 1.38.1 Normal Arrow

##### 1.38.2 Itself Arrow

##### 1.38.3 Incoming and Outgoing Messages (with '[', ']')

###### 1.38.3.1 Incoming Messages (with '[')

###### 1.38.3.2 Outgoing Messages (with ']')

##### 1.38.4 Short Incoming and Outgoing Messages (with '?')

###### 1.38.4.1 Short Incoming Messages (with '?')

###### 1.38.4.2 Short Outgoing Messages (with '?')

##### 1.38.5 Outgoing Message (with ']')

##### 1.38.6 Short Incoming and Outgoing Message (with '?')

##### 1.38.7 Short Incoming (with '?')

##### 1.38.8 Short Outgoing (with '?')

### Part 15

#### 1.39 Specific SkinParameter

##### 1.39.1 By default

##### 1.39.2 Lifeline Strategy

##### 1.39.3 Style Strictuml

### Part 16

#### 1.40 Hide Unlinked Participant

#### 1.41 Color a Group Message

#### 1.42 Mainframe

##### QA-4019

#### 1.43 Slanted or Odd Arrows

##### (nn) option

## 02 Use Case Diagram

### 2.01 Usecases

#### keyword: usecase

### 2.02 Actors

#### keyword: actor

### 2.03 Change Actor Style

#### skinparam actorStyle

#### Stick man (by default)

#### Awesome man (c4 style)

#### Hollow man

### 2.04 Usecases description

### 2.05 Use package

### 2.06 Basic example

#### arrow: -->

### 2.07 Extension

#### symbol: <|--

### 2.08 Using notes

#### note left of

#### note right of

#### note top of

#### note bottom of

### 2.09 Stereotypes
 (see:3.09 Notes and Stereotypes)
#### << and >>

### 2.10 Changing arrows direction

### 2.11 Splitting diagrams

#### keyword: newpage

### 2.12 Left to Right Direction

### 2.13 Skinparam

### 2.14 Complete example

### 2.15 Business Use Case

#### 2.15 1 Business Usecase

#### 2.15.2 Business Actor

### 2.16 Change Arrow Color and Style (inline style)

### 2.17 Change Element Color and Style (inline style)

### 2.18 Display JSON Data on Usecase Diagram

#### 2.18.1 Simple Example

## 03 Class Diagram

### 3.01 Declaring Element

### 3.02 Relations between Classes

### 3.03 Label on Relations

### 3.04 Using Non-Letters in Element Names and Relation Labels

### 3.05 Adding Methods

### 3.06 Defining Visibility

### 3.07 Abstract and Static

### 3.08 Advanced Class Body

### 3.09 Notes and Stereotypes

### 3.10 More on Notes

### 3.11 Note on Field or Method

#### 3.11.1 Constraint

#### 3.11.2 Note on Field or Method

#### 3.11.3 Note on Method with the Same Name

### 3.12 Note on Links

### 3.13 Abstract Class and Interface

### 3.14 Hide Attributes, Methods...

### 3.15 Hide Classes

### 3.16 Remove Classes

### 3.17 Hide, Remove or Restore Tagged Elements or Wildcard

### 3.18 Hide or Remove Unlinked Class

### 3.19 Use Generics

### 3.20 Specific Spot

### 3.21 Packages

### 3.22 Packages Style

### 3.23 Namespaces

### 3.24 Automatic Package Creation

### 3.25 Lollipop Interface

### 3.26 Changing Arrows Orientation

### 3.27 Association Classes

### 3.28 Association on Same Class

### 3.29 Skinparam

### 3.30 Skinned Stereotypes

### 3.31 Color Gradient

### 3.32 Help on Layout

### 3.33 Splitting Large Files

### 3.34 Extends and Implements

### 3.35 Bracketed Relations (linking or arrow) Style

#### 3.35.1 Line Style

#### 3.35.2 Line Color

#### 3.35.3 Line Thickness

#### 3.35.4 Mix

### 3.36 Change Relations (linking or arrow) color and style (inline style)

### 3.37 Change Class Color and Style (inline style)

### 3.38 Arrow from/to Class Members

### 3.39 Grouping Inheritance Arrow Heads

#### 3.39.1 GroupInheritance 1 (no grouping)

#### 3.39.2 GroupInheritance 2 (grouping from 2)

#### 3.39.3 GroupInheritance 3 (grouping only from 3)

#### 3.39.4 GroupInheritance 4 (grouping only from 4)

### 3.40 Display JSON Data on Class or Object Diagram

### 3.41 Packages and Namespaces Enhancement

## 04 Object Diagram

### 4.01 Definition of Objects

### 4.02 Relations between Objects

### 4.03 Associations Objects

### 4.04 Adding Fields

### 4.05 Common Features with Class Diagrams

### 4.06 Map Table or Associative Array

### 4.07 Program (or project) evaluation and review technique (PERT) with Map

## 05 Activity Diagram (legacy)

## 06 Activity Diagram (New Syntax)

## 07 Component Diagram

## 08 Deployment Diagram

## 09 State Diagram

## 10 Timing Diagram

# Non-UML Diagrams

## 11 Display JSON Data

## 12 Display YAML Data

## 13 Network Diagram (nwdiag)

## 14 Salt (Wireframe)

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
