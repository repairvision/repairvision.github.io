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
ReVision provides project setup wizards for the configuration of consistency rules (aka. constraints) and edit rules (aka. consistency-preserving edit operations) plug-in projects.

- [Definition of Edit Rules](#definition-of-edit-rules)
- [Definition of Consistency Rules](#definition-of-consistency-rules)

In general, the project wizards can be found in Eclipse: 

- `File -> New -> Other... -> ReVision`
    - `Constraint Plug-in Project`
    - `Edit Rule Plug-in Project`

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
{% assign fig_step34 = fig %}

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

- `File -> New -> Other... -> ReVision -> Constraint Plug-in Project`

<figure class="aligncenter">
	<a href="{{folderpath}}images/2_1_constraint_wizard.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step21 }}" src="{{folderpath}}images/2_1_constraint_wizard.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step21 }}: ReVision Configuration </figcaption>
</figure>

Select the `Constraint Plug-in Project` wizard and click `Next`.
Specify a `Project name`, e.g., `io.repairvision.github.<modeling language name>.constraints`.
The remaining settings should look similar to Fig. {{ fig_step22 }}.

<figure class="aligncenter">
	<a href="{{folderpath}}images/2_2_constraint_wizard.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step22 }}" src="{{folderpath}}images/2_2_constraint_wizard.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step22 }}: ReVision Configuration </figcaption>
</figure>

In the project wizard, click `Next`.
Specify a plug-in `Name`, e.g., `Constraints <Modeling Language Name>`.
The remaining settings should look similar to Fig. {{ fig_step23 }}.

<figure class="aligncenter">
	<a href="{{folderpath}}images/2_3_constraint_wizard.png.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step23 }}" src="{{folderpath}}images/2_3_constraint_wizard.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step23 }}: ReVision Configuration </figcaption>
</figure>

On the `Next` page, specify the `Document Types`, i.e., the meta-model of the modeling language.
Use the search field to find the meta-model by its namespace URI.

- - -

`(!)` Please note that this assumes that your meta-model is registered in the Eclipse instance you are currently running.
If you are in the workspace in which you develop your meta-model, you have to run a second Eclipse instance with that meta-model registered and loaded, e.g., from the plugin.xml -> Overview (Tab) -> Testing (Section) -> Launch an Eclipse application.

- - -

<figure class="aligncenter">
	<a href="{{folderpath}}images/2_4_constraint_wizard.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step24 }}" src="{{folderpath}}images/2_4_constraint_wizard.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step24 }}: ReVision Configuration </figcaption>
</figure>

Clicking `Finish` initializes your new plug-in in the Eclipse Workspace (check your Project Explorer).
If not automatically opened, go to and open the constraint definition file (see Fig. {{ fig_step34  }} and {{ fig_step31 }}):

- `io.repairvision.github.<modeling language name>.constraints -> src -> io.repairvision.github.<modeling language name>.constraints -> <modeling language name>.fol`

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

The `*.fol` file first specifies the modeling language by the `domain` keyword and the namespace URI of the modeling language's Ecore meta-model.
This line should have been already inserted by the project wizard.

After that, you can define the consistency rules.
As shown in Fig. {{ fig_step32 }}, a consistency rule definition starts with the `constraint` keyword, followed by a unique name for the constraint and a colon `:`.
The second keyword `message` defines a description for the developer that is shown if the constraint is violated.
Next, after the `context` keyword the context type is specified, i.e., the type of the context element in a model's abstract syntax tree starting from which the constraint is validated.
For example, in Fig. {{ fig_step32 }}, the context type is `DFA` and the variable `dfa` refers to the context element (similar to `self` in OCL).
Moreover, as shown in Fig. {{ fig_step32 }}, the editor supports auto-completion (`ctrl+space`) for meta-model types and syntax fragments.

<figure class="aligncenter">
	<a href="{{folderpath}}images/3_2_constraint_editor.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step32 }}" src="{{folderpath}}images/3_2_constraint_editor.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step32 }}: ReVision Configuration </figcaption>
</figure>

The constraint must be a Boolean expression that is validated on the context element. 
A constraint can be constructed using the following grammar.
For the sake of readability, terminals in the following grammar definition are enclosed with a space rather than quotation marks:

````
<Constraint> ::= constraint <RuleName> message <String> context <Variable> : <Formula>
<RuleName> ::= <ID>
<Variable> ::= <EClassifier> <VarName>
<VarName> ::= <ID>
````

In general, IDs are unique names that can be referenced in a certain scope.
IDs that conflict with keywords can be escaped by a `^` prefix.
Strings are surrounded by `'` or `"` quotation marks with the escape sequences `\"` and `\'`. 
Escape sequences starting with `\ ` are only allowed for the literals`\b`, `\t`, and so on.

````
<ID> ::= ( ^ )?( a..z | A..Z | _ )( a..z | A..Z | _ | 0..9 )*
<String> ::= " ( \b | \t | \n | \f | \r | \u | \" | \' | \\ | !( \ | " ))* "
           | ' ( \b | \t | \n | \f | \r | \u | \" | \' | \\ | !( \ | ' ))* '
<Integer> ::= ( 0..9 )+
<Boolean> ::= true | false
````

A formula computes a Boolean value; 
a binary formula combines two Boolean formula results; 
a predicate computes a Boolean value from a term; 
and a quantifier computes a Boolean value by evaluating a formula on all elements in a given set.

````
<Formula> ::= <Boolean> | <BinaryFormula> | <Predicate> | <Quantifier> 
            | not( <Formula> ) | ( <Formula> )

<BinaryFormula> ::= <Formula> = <Formula> 
                  | <Formula> implies <Formula> 
                  | <Formula> xor <Formula> 
                  | <Formula> or <Formula> 
                  | <Formula> and <Formula>

<Predicate> ::= isEqual( <Term> , <Term> ) 
              | isGreater( <Term> , <Term> )
              | isGreaterEqual( <Term> , <Term> )
              | isSmaller( <Term> , <Term> )
              | isSmallerEqual( <Term> , <Term> )
              | isEmpty( <Term>)
              | isInstanceOf( <Term> , <EClassifier> )
              | isValueLiteralOf( <Term> , <EDataType> )

<Quantifier> ::= forAll( <Variable> in <Term> : <Formula> )
               | exists( <Variable> in <Term> : <Formula> )
````

A navigation expression starts at a variable, e.g., `state`, followed by the name of the attribute or reference (`EStructuralFeature`) in the meta-model, e.g., `state.isStart`.
A type cast is performed by `::` followed by the type's name (`EClassifier`) in the meta-model, e.g., `transition.to::State.name` if `transition.to` would return an abstract type like `Vertex`.

````
<Term> ::= <VarName>< . <<EClassifier> :: >?<EStructuralFeature>>+
         | getContainer( <Term> )
         | getContainments( <Term > )
         | getClosure( <Term> , <EStructuralFeature> )
         | size( <Term> )
         | indexOf( <Term> , <EStructuralFeature> , <Term> )
         | concatenate( <Term> , <Term> )
         | capitalize( <Term> )
         | asClassifier( <Term> )
         | asDataType( <Term> )
         | <Integer> | <String> | <Boolean>
````

Fig. {{ fig_step34 }} shows a meta-model for a simple Deterministic Finite Automaton (DFA).
Please note that a navigation expression term that returns an EBoolean, e.g., `state.isStart`, (currently) has to be converted explicitly to a Boolean, e.g., `isEqual(state.isStart, true)`.

<figure class="aligncenter">
	<a href="{{folderpath}}images/0_5_metamodel.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step34 }}" src="{{folderpath}}images/0_5_metamodel.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step34 }}: ReVision Configuration </figcaption>
</figure>

Fig. {{ fig_step33 }} shows some example consistency rules for this DFA.

<figure class="aligncenter">
	<a href="{{folderpath}}images/3_3_constraint_editor.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step33 }}" src="{{folderpath}}images/3_3_constraint_editor.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step33 }}: ReVision Configuration </figcaption>
</figure>


##### Definition of Edit Rules

The next step is to create a plug-in project that specifies the edit rule (aka. consistency-preserving edit operations) for an existing modeling language, i.e., a meta-model defined using the Ecore modeling language.

- - -

`(!)` Please note that this assumes that your meta-model is registered in the Eclipse instance you are currently running.
If you are in the workspace in which you develop your meta-model, you have to run a second Eclipse instance with that meta-model registered and loaded, e.g., from the plugin.xml -> Overview (Tab) -> Testing (Section) -> Launch an Eclipse application.

`(!)` Moreover, if you want to initialize the edit rules based on the specified constraints, the constraint plug-in must be registered in the Eclipse instance you are currently running.
If you are in the workspace in which you developed your constraints, you have to run a second Eclipse instance with that constraint plug-in registered and loaded, e.g., from the plugin.xml -> Overview (Tab) -> Testing (Section) -> Launch an Eclipse application.

`(!)` To avoid nesting multiple Eclipse workspace instances (`meta-model development -> constraint development -> edit rule development`), you can import (`File -> Import -> Existing Projects into Workspace`) the constraint plug-in into your primary `meta-model development` workspace.
You can link the project instead of copying it.

- - -

To initialize an edit rule plug-in project, go to:

- `File -> New -> Other... -> ReVision -> Edit Rule Plug-in Project`

<figure class="aligncenter">
	<a href="{{folderpath}}images/4_1_edit_rule_generator.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step41 }}" src="{{folderpath}}images/4_1_edit_rule_generator.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step41 }}: ReVision Configuration </figcaption>
</figure>

Select the `Edit Rule Plug-in Project` wizard and click `Next`.
Specify a `Project name`, e.g., `io.repairvision.github.<modeling language name>.editrules`.
The remaining settings should look similar to Fig. {{ fig_step42 }}.

<figure class="aligncenter">
	<a href="{{folderpath}}images/4_2_edit_rule_generator.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step42 }}" src="{{folderpath}}images/4_2_edit_rule_generator.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step42 }}: ReVision Configuration </figcaption>
</figure>

In the project wizard, click `Next`.
Specify a plug-in `Name`, e.g., `Edit Rules <Modeling Language Name>`.
The remaining settings should look similar to Fig. {{ fig_step43 }}.

<figure class="aligncenter">
	<a href="{{folderpath}}images/4_3_edit_rule_generator.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step43 }}" src="{{folderpath}}images/4_3_edit_rule_generator.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step43 }}: ReVision Configuration </figcaption>
</figure>

On the `Next` page, specify the `Document Types`, i.e., the meta-model of the modeling language.
Use the search field to find the meta-model by its namespace URI.

<figure class="aligncenter">
	<a href="{{folderpath}}images/4_4_edit_rule_generator.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step44 }}" src="{{folderpath}}images/4_4_edit_rule_generator.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step44 }}: ReVision Configuration </figcaption>
</figure>

On the same page (see Fig. {{ fig_step45 }}), if registered consistency rules are found, you can select the constraints for which the wizard will infer simple initial edit rules. 

<figure class="aligncenter">
	<a href="{{folderpath}}images/4_5_edit_rule_generator.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step45 }}" src="{{folderpath}}images/4_5_edit_rule_generator.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step45 }}: ReVision Configuration </figcaption>
</figure>

ReVision can generate edit rules from concrete modeling examples.
A modeling example is translated into a graph pattern, which can be further modified and annotated by an edit rule developer.
Such graph patterns are then combined into edit rules.
Fig. {{ fig_step46 }} shows the catalog for the graph patterns, which can be opened for editing in a graphical editor.
Details about this concept are described in our journal paper [History-based Model Repair Recommendations](https://dl.acm.org/doi/abs/10.1145/3419017).

<figure class="aligncenter">
	<a href="{{folderpath}}images/4_6_edit_rule_generator.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step46 }}" src="{{folderpath}}images/4_6_edit_rule_generator.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step46 }}: ReVision Configuration </figcaption>
</figure>

As shown in Fig. {{ fig_step47 }}, the project contains the following files:

- __editrules:__ The [EMF Henshin](https://projects.eclipse.org/projects/modeling.emft.henshin) graph transformation rules representing the edit rules.
- __examples:__ The folder structure and the contained concrete modeling examples are automatically transformed into graph patterns (assuming Eclipse's `Project -> Build Automatically` is enabled).
- __patterns:__ Contains the graph patterns and an intermediate representation of the edit rules.
    - patterns.aird: The graphical representation of the graph patterns.
    - patterns.graphpattern: The model storing the graph patterns.
    - editrules.graphpattern: An intermediate representation of the edit rules that are translated into Henshin rules.

<figure class="aligncenter">
	<a href="{{folderpath}}images/4_7_edit_rule_generator.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step47 }}" src="{{folderpath}}images/4_7_edit_rule_generator.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step47 }}: ReVision Configuration </figcaption>
</figure>

- - -

`(!)` In order for ReVision to discover your edit rules, the constraint plug-in must be registered in the Eclipse instance in which you running the ReVision repair tool.
If you are in the workspace in which you developed your edit rules, you have to run a second Eclipse instance with that edit rule plug-in registered and loaded, e.g., from the plugin.xml -> Overview (Tab) -> Testing (Section) -> Launch an Eclipse application.

`(!)` To avoid nesting multiple Eclipse workspace instances (`meta-model development -> constraint development -> edit rule development`), you can import (`File -> Import -> Existing Projects into Workspace`) the edit rules plug-in into your primary development workspace.
You can link the project instead of copying it.

`(!)` For production, plug-ins can be deployed as drop-ins (`File -> Export -> Plug-in Development -> Deployable plug-ins and fragments -> Destination: <the dropins folder of the Eclipse installation>`) or as part of an Eclipse update site.

- - -
