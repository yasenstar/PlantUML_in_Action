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

#### 1.26 Return

##### syntax: return label

### Part 9

#### 1.27 Participant Creation

#### 1.28 Shortcut Syntax for Activation, Deactivation, Creation

### Part 10

#### 1.29 Incoming and Outgoing Messages

#### 1.30 Short Arrows for Incoming and Outgoing Messages

### Part 11

#### 1.31 Anchors and Duration

#### 1.32 Sterotypes and Spots

### Part 12

#### 1.33 More Information on Titles

#### 1.34 Participants Encompass

#### 1.35 Removing Foot Boxes

### Part 13

#### 1.36 Skinparam
 (see:1.39 Specific SkinParameter)
#### 1.37 Changing Padding

### Part 14

#### 1.38 Appendix: Examples of All Arrow Type

##### 1.38.1 Normal Arrow

##### 1.38.2 Itself Arrow

##### 1.38.3 Incoming and Outgoing Messages (with '[', ']')

###### 1.38.3.1 Incoming Messages (with '[')

###### 1.38.3.2 Outgoing Messages (with ']')

##### 1.38.4 Short Incoming and Outgoing Messages (with '?')

###### 1.38.4.1 Short Incoming Messages (with '?')

###### 1.38.4.2 Short Outgoing Messages (with '?')

### Part 15

#### 1.39 Specific SkinParameter

##### 1.39.1 By default

##### 1.39.2 Lifeline Strategy

##### 1.39.3 Style Strictuml

### Part 16

#### 1.40 Hide Unlinked Participant

#### 1.41 Color a Group Message

#### 1.42 Mainframe

#### 1.43 Slanted or Odd Arrows

## 02 Use Case Diagram

## 03 Class Diagram

## 04 Object Diagram

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
