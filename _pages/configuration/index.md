---
layout: page
title:  "Tool Configuration"
permalink: "/configuration/"
exclude: false
order: 2
---

{% capture folderpath %}{{ site.url }}/{{ page.path | remove: page.name }}{% endcapture %}

#### Experimental Tool Configuration

[The tool configuration (including consistency rules and edit rules for Ecore) which we have been defined and evaluated with ReVision can be found here.](/evaluation/)

#### Tool Configuration Demonstration

The configuration of ReVision is provided by so-called Eclipse plug-in projects.
ReVision provides project setup wizards for the configuration of consistency rules (aka. constraints) and edit rules (aka. consistency-preserving edit operations).
In general, the project wizards can be found in Eclipse: 

- File -> New -> Other... -> ReVision
    - Constraint Plug-in Project
    - Edit Rule Plug-in Project

{% assign fig = 0 %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step21 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step22 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step23 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step23 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step24 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step34 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step31 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step32 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step33 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step33 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step41 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step42 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step43 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step44 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step45 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step46 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step47 = fig %}

##### Definition of Consistency Rules

As the first step, we create a plug-in project that specifies the consistency rules for an existing modeling language, i.e., a meta-model defined using the Ecore modeling language.
In Eclipse go to:

- File -> New -> Other... -> ReVision -> Constraint Plug-in Project

<figure class="aligncenter">
	<a href="{{folderpath}}images/2_1_constraint_wizard.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step21 }}" src="{{folderpath}}images/2_1_constraint_wizard.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step21 }}: ReVision Configuration </figcaption>
</figure>

Select the 'Constraint Plug-in Project' wizard and click 'Next'.
Specify a 'Project name', e.g., 'io.repairvision.github.<modeling language name>.constraints'.
The remaining settings should look similar to Fig. {{ fig_step22 }}.

<figure class="aligncenter">
	<a href="{{folderpath}}images/2_2_constraint_wizard.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step22 }}" src="{{folderpath}}images/2_2_constraint_wizard.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step22 }}: ReVision Configuration </figcaption>
</figure>

In the project wizard click 'Next'.
Specify a plug-in 'Name', e.g., 'Constraints <Modeling Language Name>'.
The remaining settings should look similar to Fig. {{ fig_step23 }}.

<figure class="aligncenter">
	<a href="{{folderpath}}images/2_3_constraint_wizard.png.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step23 }}" src="{{folderpath}}images/2_3_constraint_wizard.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step23 }}: ReVision Configuration </figcaption>
</figure>

On the 'Next' page specify the 'Document Types', i.e., the meta-model of the modeling language.
Use the search field to find the meta-model by its namespace URI.

<figure class="aligncenter">
	<a href="{{folderpath}}images/2_4_constraint_wizard.png.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step24 }}" src="{{folderpath}}images/2_4_constraint_wizard.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step24 }}: ReVision Configuration </figcaption>
</figure>

Clicking 'Finish' initializes your new plug-in in the Eclipse Workspace (check your Project Explorer).
If not automatically opened, go to and open the constraint definition file (see Fig. {{ fig_step34  }} and {{ fig_step31 }}):

- io.repairvision.github.<modeling language name>.constraints -> src -> io.repairvision.github.<modeling language name>.constraints -> <modeling language name>.fol

<figure class="aligncenter">
	<a href="{{folderpath}}images/3_4_constraint_editor.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step34 }}" src="{{folderpath}}images/3_4_constraint_editor.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step34 }}: ReVision Configuration </figcaption>
</figure>

<figure class="aligncenter">
	<a href="{{folderpath}}images/3_1_constraint_editor.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step31 }}" src="{{folderpath}}images/3_1_constraint_editor.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step31 }}: ReVision Configuration </figcaption>
</figure>

The *.fol file first specifies the modeling language by the 'domain' keyword and the namespace URI of the Ecore meta-model.
This line should have been already be inserted by the project wizard.

After that you can define the consistency rules.
As shown in Fig. {{ fig_step32 }}, a consistency rule definition starts with the 'constraint' keyword, followed by unique name for the constraint and a colon ':'.
The second keyword 'message' defines a description for the developer that is shown if the constraint is violated.
Next, after the the 'context' keyword the context type is specified, i.e., the type of the context element in a model's abstract syntax tree starting from which the constraint is validated.
For example, in Fig. {{ fig_step32 }}, the context type is 'DFA' and the variable 'dfa' refers to the context element (similar to 'self' in OCL).

<figure class="aligncenter">
	<a href="{{folderpath}}images/3_2_constraint_editor.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step32 }}" src="{{folderpath}}images/3_2_constraint_editor.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step32 }}: ReVision Configuration </figcaption>
</figure>

The constraint must be a Boolean expression that is validated on the context element:

- constraint <RuleName> message <String> context <Variable> : <Formula>
- <RuleName> ::= <ID>
- <Variable> ::= <EClassifier> <VarName>
- <VarName> ::= <ID>
- <ID> ::= ^?<a..z|A..Z|_><a..z|A..Z|_|0..9>*;

IDs that conflict with keywords can be escaped by a ^ prefix.
Strings are surrounded by ' or " quotation marks.

- <Formula> ::= <Boolean> | <BinaryFormula> | <Predicate> | <Quantifier> | not( <Formula> ) | ( <Formula> )
- <Boolean> ::= true | false

- <BinaryFormula> ::= <Formula> = <Formula> 
    - | <Formula> implies <Formula> 
    - | <Formula> xor <Formula> 
    - | <Formula> or <Formula> 
    - | <Formula> and <Formula>

- <Predicate> ::= isEqual(<Term>, <Term>) 
    - | isGreater(<Term>, <Term>)
    - | isGreaterEqual(<Term>, <Term>)
    - | isSmaller(<Term>, <Term>)
    - | isSmallerEqual(<Term>, <Term>)
    - | isEmpty(<Term>)
    - | isInstanceOf(<Term>, <EClassifier>)
    - | isValueLiteralOf(<Term>, <EDataType>)

- <Quantifier> ::= forAll(<Variable> in <Term> : <Formula>)
    - | exists(<Variable> in <Term> : <Formula>)

A navigation expression starts at a variable, e.g., 'state', followed by the name of the attribute or reference (EStructuralFeature) in the meta-model, e.g., 'state.name'.
A type cast is performed by '::' followed by the type's name (EClassifier) in the meta-model, e.g., transition.source::State.name.

- <Term> ::= <VarName><.<<EClassifier>::>?<EStructuralFeature>>+
    - | getContainer(<Term>)
    - | getContainments(<Term>)
    - | getClosure(<Term>, <EStructuralFeature>)
    - | size(<Term>)
    - | indexOf(<Term>, <EStructuralFeature>, <Term>)
    - | concatenate(<Term>, <Term>)
    - | capitalize(<Term>)
    - | asClassifier(<Term>)
    - | asDataType(<Term>)
    - | <Integer> | <String> | <Boolean>

<figure class="aligncenter">
	<a href="{{folderpath}}images/3_3_constraint_editor.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step33 }}" src="{{folderpath}}images/3_3_constraint_editor.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step33 }}: ReVision Configuration </figcaption>
</figure>

##### Definition of Edit Rules

<figure class="aligncenter">
	<a href="{{folderpath}}images/4_1_edit_rule_generator.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step41 }}" src="{{folderpath}}images/4_1_edit_rule_generator.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step41 }}: ReVision Configuration </figcaption>
</figure>

<figure class="aligncenter">
	<a href="{{folderpath}}images/4_2_edit_rule_generator.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step42 }}" src="{{folderpath}}images/4_2_edit_rule_generator.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step42 }}: ReVision Configuration </figcaption>
</figure>

<figure class="aligncenter">
	<a href="{{folderpath}}images/4_3_edit_rule_generator.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step43 }}" src="{{folderpath}}images/4_3_edit_rule_generator.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step43 }}: ReVision Configuration </figcaption>
</figure>

<figure class="aligncenter">
	<a href="{{folderpath}}images/4_3_edit_rule_generator.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step43 }}" src="{{folderpath}}images/4_3_edit_rule_generator.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step43 }}: ReVision Configuration </figcaption>
</figure>

<figure class="aligncenter">
	<a href="{{folderpath}}images/4_4_edit_rule_generator.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step44 }}" src="{{folderpath}}images/4_4_edit_rule_generator.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step44 }}: ReVision Configuration </figcaption>
</figure>

<figure class="aligncenter">
	<a href="{{folderpath}}images/4_5_edit_rule_generator.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step45 }}" src="{{folderpath}}images/4_5_edit_rule_generator.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step45 }}: ReVision Configuration </figcaption>
</figure>

<figure class="aligncenter">
	<a href="{{folderpath}}images/4_6_edit_rule_generator.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step46 }}" src="{{folderpath}}images/4_6_edit_rule_generator.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step46 }}: ReVision Configuration </figcaption>
</figure>

<figure class="aligncenter">
	<a href="{{folderpath}}images/4_7_edit_rule_generator.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step47 }}" src="{{folderpath}}images/4_7_edit_rule_generator.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step47 }}: ReVision Configuration </figcaption>
</figure>
