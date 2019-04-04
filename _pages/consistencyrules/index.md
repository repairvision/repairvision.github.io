---
layout: page
title:  "Consistency Rules"
permalink: "/consistencyrules/"
order: 2
---

{% capture folderpath %}
{{ site.url }}/{{ page.path | remove: page.name }}
{% endcapture %}

In this Section, we demonstrate the set of consistency rules for Ecore which we have yet defined and evaluated with ReVision. In the following, we represent the rules and their descriptions by two kind of grammars: the Object Constraint Language (OCL) as defined by the [Object Managment Group](https://www.omg.org/spec/OCL/About-OCL/) and our First-Order Logic Language (FOL) that we defined for ReVision.

* [The Attribute is not Transient So it must have a Data Type that is Serializable](#the-attribute-is-not-transient-so-it-must-have-a-data-type-that-is-serializable)

### The Attribute is not Transient So it must have a Data Type that is Serializable

<figure class="aligncenter">
	<a href="{{folderpath}}images/Folie10.PNG" target="_blank">
		<img style="width: 100%" src="{{folderpath}}images/Folie10.PNG"/>
	</a>
	<figcaption style="text-align: center">Example with Abstract Syntax Graph</figcaption>
</figure>

#### OCL Grammar
 
#### FOL Grammar

