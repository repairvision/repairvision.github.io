---
layout: page
title:  "Consistency Rules"
permalink: "/consistencyrules/"
order: 2
---

### Consistency Rules

In this Section, we demonstrate the set of Consistency Rules which have been defined in our tool called "ReVision". As it can be seen in the following content, We represent the Rules and their descriptions by two state of the art Grammars comprising the OCL and FOL.

{% capture folderpath %}
{{ site.url }}/{{ page.path | remove: page.name }}
{% endcapture %}

#### 1 Rule1 
##### 1.1 OCL Grammar

[The Attribute is not Transient So it must have a Data Type that is Serializable](eattributetransientandserializable.md)

##### 1.2 Description

{% assign fig = fig | plus: 1 %}
{% assign fig_step1 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/Folie10.PNG" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step1 }}" src="{{folderpath}}images/Folie10.PNG"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step1 }}: Description of the Rule1 </figcaption>
</figure>

 
##### 1.3 FOL Grammar

