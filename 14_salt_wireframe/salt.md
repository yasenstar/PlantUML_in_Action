## Salt (Wireframe)

**Salt** is a subproject of PlantUML that may help you to design graphical interface or [*Website Wireframe or Page Schematic or Screen Blueprint*](https://en.wikipedia.org/wiki/Website_wireframe).

It is very useful in crafting **graphical interfaces**, schematics, and blueprints. It aids in aligning **conceptual structures** with **visual design**, emphasizing **functionality over aesthetics**. **Wireframes**, central to this process, are used across various disciplines.

Developers, designers, and user experience professionals employ them to visualize **interface elements**, **navigational systems**, and to facilitate collaboration. They vary in **fidelity**, from low-detail sketches to high-detail representations, crucial for **prototyping** and **iterative design**. This collaborative process integrates different expertise, from **business analysis** to **user research**, ensuring that the end design aligns with both **business** and **user requirements**.


## Basic widgets

You can use either ``@startsalt`` keyword, or ``@startuml`` followed by a line with ``salt`` keyword.

A window must start and end with brackets. You can then define:

* Button using ``[`` and ``]``.
* Radio button using ``(`` and ``)``.
* Checkbox using ``[`` and ``]``.
* User text area using ``"``.
* Droplist using ``^``.

<plantuml>
@startsalt
{
  Just plain text
  [This is my button]
  ()  Unchecked radio
  (X) Checked radio
  []  Unchecked box
  [X] Checked box
  "Enter text here   "
  ^This is a droplist^
}
@endsalt
</plantuml>


## Text area

Here is an attempt to create a [text area](https://html.spec.whatwg.org/multipage/form-elements.html#the-textarea-element):

<plantuml>
@startsalt
{+
   This is a long
   text in a textarea
   .
   "                         "
}
@endsalt
</plantuml>

Note:
- the dot (`.`) to fill up vertical space;
- the last line of space (``"     "``) to make the area wider.

*[Ref. [QA-14765](https://forum.plantuml.net/14765/)]*


Then you can add [scroll bar](salt#6b6xvjbaj4gpk362kjkx):
<plantuml>
@startsalt
{SI
   This is a long
   text in a textarea
   .
   "                         "
}
@endsalt
</plantuml>
<plantuml>
@startsalt
{S-
   This is a long
   text in a textarea
   .
   "                         "
}
@endsalt
</plantuml>


## Open, close droplist 

You can open a droplist, by adding values enclosed by `^`, as:

<plantuml>
@startsalt
{
  ^This is a closed droplist^ |
  ^This is an open droplist^^ item 1^^ item 2^ |
  ^This is another open droplist^ item 1^ item 2^ 
}
@endsalt
</plantuml>

*[Ref. [QA-4184](https://forum.plantuml.net/4184)]*


## Using grid [| and #, !, -, +]

A table is automatically created when you use an opening bracket ``{``.
And you have to use ``|`` to separate columns.

For example:

<plantuml>
@startsalt
{
  Login    | "MyName   "
  Password | "****     "
  [Cancel] | [  OK   ]
}
@endsalt
</plantuml>

Just after the opening bracket, you can use a character to define if you want to draw lines or columns of the grid :

| Symbol | Result                                       |
| ------ | -------------------------------------------- |
| ``#``  | To display all vertical and horizontal lines |
| ``!``  | To display all vertical lines                |
| ``-``  | To display all horizontal lines              |
| ``+``  | To display external lines                    |

<plantuml>
@startsalt
{+
  Login    | "MyName   "
  Password | "****     "
  [Cancel] | [  OK   ]
}
@endsalt
</plantuml>


## Group box [^]

<plantuml>
@startsalt
{^"My group box"
  Login    | "MyName   "
  Password | "****     "
  [Cancel] | [  OK   ]
}
@endsalt
</plantuml>

*[Ref. [QA-5840](http://forum.plantuml.net/5840/please-allow-to-create-groupboxes-in-salt?show=5840#q5840)]*


## Using separator [.., ==, ~~, --]

You can use several horizontal lines as separator.

<plantuml>
@startsalt
{
  Text1
  ..
  "Some field"
  ==
  Note on usage
  ~~
  Another text
  --
  [Ok]
}
@endsalt
</plantuml>


## Tree widget [T]

To have a Tree, you have to start with ``{T`` and to use ``+`` to denote hierarchy.

<plantuml>
@startsalt
{
{T
 + World
 ++ America
 +++ Canada
 +++ USA
 ++++ New York
 ++++ Boston
 +++ Mexico
 ++ Europe
 +++ Italy
 +++ Germany
 ++++ Berlin
 ++ Africa
}
}
@endsalt
</plantuml>


## Tree table [T]

You can combine trees with tables.


<plantuml>
@startsalt
{
{T
+Region        | Population    | Age
+ World        | 7.13 billion  | 30
++ America     | 964 million   | 30
+++ Canada     | 35 million    | 30
+++ USA        | 319 million   | 30
++++ NYC       | 8 million     | 30
++++ Boston    | 617 thousand  | 30
+++ Mexico     | 117 million   | 30
++ Europe      | 601 million   | 30
+++ Italy      | 61 million    | 30
+++ Germany    | 82 million    | 30
++++ Berlin    | 3 million     | 30
++ Africa      | 1 billion     | 30
}
}
@endsalt
</plantuml>

And add lines.

<plantuml>
@startsalt
{
..
== with T!
{T!
+Region        | Population    | Age
+ World        | 7.13 billion  | 30
++ America     | 964 million   | 30
}
..
== with T-
{T-
+Region        | Population    | Age
+ World        | 7.13 billion  | 30
++ America     | 964 million   | 30
}
..
== with T+
{T+
+Region        | Population    | Age
+ World        | 7.13 billion  | 30
++ America     | 964 million   | 30
}
..
== with T#
{T#
+Region        | Population    | Age
+ World        | 7.13 billion  | 30
++ America     | 964 million   | 30
}
..
}
@endsalt
</plantuml>


*[Ref. [QA-1265](https://forum.plantuml.net/1265/feature-request-tree-tables)]*


## Enclosing brackets [{, }]

You can define subelements by opening a new opening bracket.

<plantuml>
@startsalt
{
Name         | "                 "
Modifiers:   | { (X) public | () default | () private | () protected
                [] abstract | [] final   | [] static }
Superclass:  | { "java.lang.Object " | [Browse...] }
}
@endsalt
</plantuml>


## Adding tabs [/]

You can add tabs using ``{/`` notation. Note that you can use HTML code to have bold text.

<plantuml>
@startsalt
{+
{/ <b>General | Fullscreen | Behavior | Saving }
{
{ Open image in: | ^Smart Mode^ }
[X] Smooth images when zoomed
[X] Confirm image deletion
[ ] Show hidden images
}
[Close]
}
@endsalt
</plantuml>

Tab could also be vertically oriented:

<plantuml>
@startsalt
{+
{/ <b>General
Fullscreen
Behavior
Saving } |
{
{ Open image in: | ^Smart Mode^ }
[X] Smooth images when zoomed
[X] Confirm image deletion
[ ] Show hidden images
[Close]
}
}
@endsalt
</plantuml>


## Using menu [*]

You can add a menu by using ``{*`` notation.

<plantuml>
@startsalt
{+
{* File | Edit | Source | Refactor }
{/ General | Fullscreen | Behavior | Saving }
{
{ Open image in: | ^Smart Mode^ }
[X] Smooth images when zoomed
[X] Confirm image deletion
[ ] Show hidden images
}
[Close]
}
@endsalt
</plantuml>

It is also possible to open a menu:

<plantuml>
@startsalt
{+
{* File | Edit | Source | Refactor
 Refactor | New | Open File | - | Close | Close All }
{/ General | Fullscreen | Behavior | Saving }
{
{ Open image in: | ^Smart Mode^ }
[X] Smooth images when zoomed
[X] Confirm image deletion
[ ] Show hidden images
}
[Close]
}
@endsalt
</plantuml>

Like it is possible to open a droplist:
<plantuml>
@startsalt
{+
{* File | Edit | Source | Refactor }
{/ General | Fullscreen | Behavior | Saving }
{
{ Open image in: | ^Smart Mode^^Normal Mode^ }
[X] Smooth images when zoomed
[X] Confirm image deletion
[ ] Show hidden images
}
[Close]
}
@endsalt
</plantuml>
*[Ref. [QA-4184](https://forum.plantuml.net/4184)]*


## Advanced table

You can use two special notations for table :
* ``*`` to indicate that a cell with span with left
* ``.`` to denotate an empty cell

<plantuml>
@startsalt
{#
. | Column 2 | Column 3
Row header 1 | value 1 | value 2
Row header 2 | A long cell | *
}
@endsalt
</plantuml>


## Scroll Bars [S, SI, S-]

You can use `{S` notation for [scroll bar](https://en.wikipedia.org/wiki/Scrollbar) like in following examples:

* ``{S``: for horizontal and vertical scrollbars
<plantuml>
@startsalt
{S
Message
.
.
.
.
}
@endsalt
</plantuml>

* ``{SI`` : for vertical scrollbar only
<plantuml>
@startsalt
{SI
Message
.
.
.
.
}
@endsalt
</plantuml>

* ``{S-`` : for horizontal scrollbar only
<plantuml>
@startsalt
{S-
Message
.
.
.
.
}
@endsalt
</plantuml>


## Colors

It is possible to change text [color](color) of widget.

<plantuml>
@startsalt
{
  <color:Blue>Just plain text
  [This is my default button]
  [<color:green>This is my green button]
  [<color:#9a9a9a>This is my disabled button]
  []  <color:red>Unchecked box
  [X] <color:green>Checked box
  "Enter text here   "
  ^This is a droplist^
  ^<color:#9a9a9a>This is a disabled droplist^
  ^<color:red>This is a red droplist^
}
@endsalt
</plantuml>

*[Ref. [QA-12177](https://forum.plantuml.net/12177/change-color-of-salt-button-to-represent-disabled-status)]*


## Creole on Salt

You can use [Creole or HTML Creole](creole) on salt:

<plantuml>
@startsalt
{{^==Creole
  This is **bold**
  This is //italics//
  This is ""monospaced""
  This is --stricken-out--
  This is __underlined__
  This is ~~wave-underlined~~
  --test Unicode and icons--
  This is <U+221E> long
  This is a <&code> icon
  Use image : <img:http://plantuml.com/logo3.png>
}|
{^<b>HTML Creole 
 This is <b>bold</b>
  This is <i>italics</i>
  This is <font:monospaced>monospaced</font>
  This is <s>stroked</s>
  This is <u>underlined</u>
  This is <w>waved</w>
  This is <s:green>stroked</s>
  This is <u:red>underlined</u>
  This is <w:#0000FF>waved</w>
  -- other examples --
  This is <color:blue>Blue</color>
  This is <back:orange>Orange background</back>
  This is <size:20>big</size>
}|
{^Creole line
You can have horizontal line
----
Or double line
====
Or strong line
____
Or dotted line
..My title..
Or dotted title
//and title... //
==Title==
Or double-line title
--Another title--
Or single-line title
Enjoy!
}|
{^Creole list item
**test list 1**
* Bullet list
* Second item
** Sub item
*** Sub sub item
* Third item
----
**test list 2**
# Numbered list
# Second item
## Sub item
## Another sub item
# Third item
}|
{^Mix on salt
  ==<color:Blue>Just plain text
  [This is my default button]
  [<b><color:green>This is my green button]
  [ ---<color:#9a9a9a>This is my disabled button-- ]
  []  <size:20><color:red>Unchecked box
  [X] <color:green>Checked box
  "//Enter text here//   "
  ^This is a droplist^
  ^<color:#9a9a9a>This is a disabled droplist^
  ^<b><color:red>This is a red droplist^
}}
@endsalt
</plantuml>


## Pseudo sprite [<<, >>]

Using `<<` and `>>` you can define a pseudo-sprite or sprite-like drawing and reusing it latter.

<plantuml>
@startsalt
 {
 [X] checkbox|[] checkbox
 () radio | (X) radio
 This is a text|[This is my button]|This is another text
 "A field"|"Another long Field"|[A button]
 <<folder
 ............
 .XXXXX......
 .X...X......
 .XXXXXXXXXX.
 .X........X.
 .X........X.
 .X........X.
 .X........X.
 .XXXXXXXXXX.
 ............
 >>|<color:blue>other folder|<<folder>>
^Droplist^
}
@endsalt
</plantuml>

*[Ref. [QA-5849](https://forum.plantuml.net/5849/support-for-sprites-salt?show=5851#a5851)]*


## OpenIconic

[OpenIconic](https://useiconic.com/open/) is a very nice open source icon set. Those icons have been integrated into the [creole parser](creole), so you can use them out-of-the-box.
You can use the following syntax: ``<&ICON_NAME>``.

<plantuml>
@startsalt
{
  Login<&person> | "MyName   "
  Password<&key> | "****     "
  [Cancel <&circle-x>] | [OK <&account-login>]
}
@endsalt
</plantuml>

The complete list is available on OpenIconic Website, or you can use the following special diagram:


<plantuml>
@startuml
listopeniconic
@enduml
</plantuml>


## Add title, header, footer, caption or legend

<plantuml>
@startsalt
title My title
header some header
footer some footer
caption This is caption
legend
The legend
end legend

{+
  Login    | "MyName   "
  Password | "****     "
  [Cancel] | [  OK   ]
}

@endsalt
</plantuml>

*(See also: [Common commands](commons))*


## Zoom, DPI

### Whitout zoom (by default)
<plantuml>
@startsalt
{
  <&person> Login  | "MyName   "
  <&key> Password  | "****     "
  [<&circle-x> Cancel ] | [ <&account-login> OK   ]
}
@endsalt
</plantuml>

### Scale

You can use the `scale` command to zoom the generated image.

You can use either a number or a fraction to define the scale factor. You can also specify either width or height (in pixel). And you can also give both width and height: the image is scaled to fit inside the specified dimension.
<plantuml>
@startsalt
scale 2
{
  <&person> Login  | "MyName   "
  <&key> Password  | "****     "
  [<&circle-x> Cancel ] | [ <&account-login> OK   ]
}
@endsalt
</plantuml>

*(See also: [Zoom on Common commands](commons#zw5yrgax40mpk362kjbn))*

### DPI
You can also use the `skinparam dpi`command to zoom the generated image.
<plantuml>
@startsalt
skinparam dpi 200
{
  <&person> Login  | "MyName   "
  <&key> Password  | "****     "
  [<&circle-x> Cancel ] | [ <&account-login> OK   ]
}
@endsalt
</plantuml>


## Include Salt "on activity diagram"

You can [read the following explanation](http://forum.plantuml.net/2427/salt-with-minimum-flowchat-capabilities?show=2427#q2427).


<plantuml>
@startuml
(*) --> "
{{
salt
{+
<b>an example
choose one option
()one
()two
[ok]
}
}}
" as choose

choose -right-> "
{{
salt
{+
<b>please wait
operation in progress
<&clock>
[cancel]
}
}}
" as wait
wait -right-> "
{{
salt
{+
<b>success
congratulations!
[ok]
}
}}
" as success

wait -down-> "
{{
salt
{+
<b>error
failed, sorry
[ok]
}
}}
"
@enduml
</plantuml>

It can also be combined with [define macro](preprocessing#macro_definition).

<plantuml>
@startuml
!unquoted procedure SALT($x)
"{{
salt
%invoke_procedure("_"+$x)
}}" as $x
!endprocedure

!procedure _choose()
{+
<b>an example
choose one option
()one
()two
[ok]
}
!endprocedure

!procedure _wait()
{+
<b>please wait
operation in progress
<&clock>
[cancel]
}
!endprocedure

!procedure _success()
{+
<b>success
congratulations!
[ok]
}
!endprocedure

!procedure _error()
{+
<b>error
failed, sorry
[ok]
}
!endprocedure

(*) --> SALT(choose)
-right-> SALT(wait)
wait -right-> SALT(success)
wait -down-> SALT(error)
@enduml
</plantuml>


## Include salt "on while condition of activity diagram"

You can include `salt` on while condition of activity diagram.

<plantuml>
@startuml
start
while (\n{{\nsalt\n{+\nPassword | "****     "\n[Cancel] | [  OK   ]}\n}}\n) is (Incorrect)
  :log attempt;
  :attempt_count++;
  if (attempt_count > 4) then (yes)
    :increase delay timer;
    :wait for timer to expire;
  else (no)
  endif
endwhile (correct)
:log request;
:disable service;
@enduml
</plantuml>

*[Ref. [QA-8547](https://forum.plantuml.net/8547/mixing-wireframes-and-activity-diagrames?show=12221#a12221)]*


## Include salt "on repeat while condition of activity diagram"

You can include `salt` on 'repeat while' condition of activity diagram.

<plantuml>
@startuml
start
repeat :read data;
  :generate diagrams;
repeat while (\n{{\nsalt\n{^"Next step"\n  Do you want to continue? \n[Yes]|[No]\n}\n}}\n)
stop
@enduml
</plantuml>

*[Ref. [QA-14287](https://forum.plantuml.net/14287/salt-in-activity-beta-diagrams)]*


## Skinparam

You can use **[only]** some [skinparam](skinparam) command to change the skin of the drawing.

Some example:

<plantuml>
@startsalt
skinparam Backgroundcolor palegreen
{+
  Login    | "MyName   "
  Password | "****     "
  [Cancel] | [  OK   ]
}
@endsalt
</plantuml>

<plantuml>
@startsalt
skinparam handwritten true
{+
  Login    | "MyName   "
  Password | "****     "
  [Cancel] | [  OK   ]
}
@endsalt
</plantuml>

[[#FFD700#FIXME]] 🚩
FYI, some other skinparam does not work with salt, as:

<plantuml>
@startsalt
skinparam defaultFontName monospaced
{+
  Login    | "MyName   "
  Password | "****     "
  [Cancel] | [  OK   ]
}
@endsalt
</plantuml>


## Style

You can use **[only]** some [style](style-evolution) command to change the skin of the drawing.

Some example:

<plantuml>
@startsalt
<style>
saltDiagram {
  BackgroundColor palegreen
}
</style>
{+
  Login    | "MyName   "
  Password | "****     "
  [Cancel] | [  OK   ]
}
@endsalt
</plantuml>


[[#FFD700#FIXME]] 🚩
FYI, some other style does not work with salt, as:

<plantuml>
@startsalt
<style>
saltDiagram {
  Fontname Monospaced
  FontSize 10
  FontStyle italic
  LineThickness 0.5
  LineColor red
}
</style>
{+
  Login    | "MyName   "
  Password | "****     "
  [Cancel] | [  OK   ]
}
@endsalt
</plantuml>

*[Ref. [QA-13460](https://forum.plantuml.net/13460/there-skinparam-change-font-used-salt-like-other-diagram-types?show=13461#a13461)]*

