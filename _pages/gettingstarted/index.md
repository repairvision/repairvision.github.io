---
layout: page
title:  "Getting Started"
permalink: "/gettingstarted/"
order: 5
---

### Example Project

* Video on Demand System (UML) Project <a href="https://github.com/mohrndorf/revision-example.git" target="new">https://github.com/mohrndorf/revision-example.git</a>

### Download and Installation

* Eclipse Platform: <a href="https://www.eclipse.org/downloads/packages/eclipse-modeling-tools/oxygen1a" target="new">Eclipse Oxygen Modeling Tools</a> (Includes the Eclipse Modeling Framework).

**The newest version of ReVision can be obtained from the following _update site_:**

* _https://pi.informatik.uni-siegen.de/projects/repairvision/updatesite_
* Please install a SVN-Connector for repository integration, e.g.:
* _https://dl.bintray.com/subclipse/releases/subclipse/latest/_

### Quick Introduction

[Quick Introduction](https://repairvision.github.io/_pages/gettingstarted/slider.html)


{% capture folderpath %}
{{ site.url }}/{{ page.path | remove: page.name }}
{% endcapture %}

{% assign fig = 0 %}

In this section we give some minimal examples of model inconsistencies and their repairs collected from literature.

### Step1:...

{% assign fig = fig | plus: 1 %}
{% assign fig_step1 = fig %}

<a href="#fig:{{ fig_step1 }}">Figure {{ fig_step1 }}</a>

<figure class="aligncenter">
	<a href="{{folderpath}}images/01.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step1 }}" src="{{folderpath}}images/01.png""/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step1 }}: LABEL </figcaption>
</figure>
