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

{% capture folderpath %}
{{ site.url }}/{{ page.path | remove: page.name }}
{% endcapture %}

{% assign fig = 0 %}



#### Step 1: Installation

##### Step 1.1: Downlaod Eclipse

{% assign fig = fig | plus: 1 %}
{% assign fig_step1.1 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/01.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step1.1 }}" src="{{folderpath}}images/01.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step1.1 }}: Get Started </figcaption>
</figure>

To begin with, first open Eclipse IDE as the following figure <a href="#fig:{{ fig_step1.1 }}">Figure {{ fig_step1.1 }} target="_blank" </a> in which you see the welcome Screen and Get Started Features...

##### Step 1.2:

{% assign fig = fig | plus: 1 %}
{% assign fig_step1.2 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/02.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step1.2 }}" src="{{folderpath}}images/02.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step1.2 }}: How to install new Software </figcaption>
</figure>

Now you should install the RepairVision Tool from the Eclipse Downloader wizard which includes update websites of various tools and frameworks. To do so, click on Help and select Install New Software from the Options Menu. See figure below <a href={{folderpath}}images/02.png target="_blank" >Figure {{ fig_step1.2 }} </a>

##### Step 1.3:...

{% assign fig = fig | plus: 1 %}
{% assign fig_step1.3 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/03.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step1.3 }}" src="{{folderpath}}images/03.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step1.3 }}: Download wizard for the Updating websites </figcaption>
</figure>

Now, you should see an installation wizard within which you can search for the RepairVision Tool or you can copy the url link of the update website and straightly paste it in the browsing field. Afterward, you can proceed the installation by just selecting the tool and clicking next... See figure below <a href="#fig:{{ fig_step1.3 }}" target="_blank"> Figure {{ fig_step1.3 }} </a>

##### Step 1.4:...

{% assign fig = fig | plus: 1 %}
{% assign fig_step1.4 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/04.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step1.4 }}" src="{{folderpath}}images/04.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step1.4 }}: Restart Eclipse to Save and Apply changes </figcaption>
</figure>
tep1:
After finishing the installation of the Revision Tool, you're supposed to restart the Eclipse IDE to apply the changes and adding the Tool to the IDE... See figure below <a href="#fig:{{ fig_step1.4 }}" target="_blank">Figure {{ fig_step1.4 }} </a>


#### Step 2: Setting up the Example Project

##### Step 2.1:...
tep1:
{% assign fig = fig | plus: 1 %}
{% assign fig_step2.1 = fig %}

tep1:
<figure class="aligncenter">
	<a href="{{folderpath}}images/05.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step2.1 }}" src="{{folderpath}}images/05.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step2.1 }}: Adding the Repository perspective </figcaption>
</figure>

In this step, you should add the Repository. To do so, click open perspective from "Window" menu and select "SVN Repository Exploring", then click on "Open" Button. As shown if figure below <a href="#fig:{{ fig_step2.1 }}" target="_blank">Figure {{ fig_step2.1 }} </a>

##### Step 2.2:...

{% assign fig = fig | plus: 1 %}
{% assign fig_step2.2 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/06.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step2.2 }}" src="{{folderpath}}images/06.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step2.2 }}: Set the location of the Repository </figcaption>
</figure>

In this step, you should add the Repository url link in "Github" by clicking on "New Repository Location" from "File" menu. At the end, click on "Finish" button. See figure below  <a href="#fig:{{ fig_step2.2 }}" target="_blank">Figure {{ fig_step2.2 }} </a>

### Step3: Testing an Example

{% assign fig = fig | plus: 1 %}
{% assign fig_step3 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/07.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step3 }}" src="{{folderpath}}images/07.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step3 }}: properties of the UML Example created by RepairVision Tool </figcaption>
</figure>

Now, It's time to check out the example you've inserted from Github Repository. To do so, right click on the Uml Example and select "Check Out" from option menu. Afterwards, you'll see the specifications of the example on the "SVN Repository Browser" window pane in the bottom of the Eclipse IDE... See figure below <a href="#fig:{{ fig_step3 }}" target="_blank"> Figure {{ fig_step3 }} </a>


##### Step 3.1:...

{% assign fig = fig | plus: 1 %}
{% assign fig_step3.1 = fig %}

<a href="#fig:{{ fig_step3.1  }}">Figure {{ fig_step3.1  }}</a>

<figure class="aligncenter">
	<a href="{{folderpath}}images/08.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step3.1 }}" src="{{folderpath}}images/08.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step3.1 }}: Opening the UML Example </figcaption>
</figure>

Here, the representations of the UML Example's Class Diagram are shown in different window panes in the editor... See figure below <a href="#fig:{{ fig_step3.1 }}" target="_blank"> Figure {{ fig_step3.1 }} </a>

### Step 3.2:...

{% assign fig = fig | plus: 1 %}
{% assign fig_step3.2 = fig %}

<a href="#fig:{{ fig_step3.2 }}">Figure {{ fig_step3.2 }}</a>

<figure class="aligncenter">
	<a href="{{folderpath}}images/09.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step3.2 }}" src="{{folderpath}}images/09.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step3.2 }}: Having the view of the UML Diagram Editor </figcaption>
</figure>

For having the view of the UML Example's Class Diagram, you should go to "Window" and "Show View", then "Other" and select the Editor to be added in the EClipse IDE just like shown in the figure... <a href="#fig:{{ fig_step3.2 }}" target="_blank">Figure {{ fig_step3.2 }} </a>

### Step 3.3:...

{% assign fig = fig | plus: 1 %}
{% assign fig_step3.3 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/10.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step3.3 }}" src="{{folderpath}}images/10.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step3.3 }}: Adding the Model Repair Tool Plugin in to the Eclipse Workspace </figcaption>
</figure>

Now, It's time to start using the "RepairVision" tool by just adding the "ModelRepair" Plugin in the "Show View" wizard... See figure below <a href="#fig:{{ fig_step3.3 }}" target="_blank">Figure {{ fig_step3.3 }} </a>


### Step 3.4:...

{% assign fig = fig | plus: 1 %}
{% assign fig_step3.4 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/11.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step3.4 }}" src="{{folderpath}}images/11.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step3.4 }}: Showing the Model Repair Tool Window panel in the Eclipse workspace </figcaption>
</figure>

After inserting the "Model Repair" Plugin, the "Model Repair" window pane with the detailed tool features is appeared in the right side panel of the Eclipse IDE... See figure below <a href="#fig:{{ fig_step3.4 }}" target="_blank"> Figure {{ fig_step3.4 }} </a>

### Step 3.5:...

{% assign fig = fig | plus: 1 %}
{% assign fig_step3.5 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/12.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step3.5 }}" src="{{folderpath}}images/12.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step3.5}}: Validation of the Input UML Example Class Diagram </figcaption>
</figure>

In this step, you can validate the input UML Example's Class Diagram and observe its status and result (Failure or Success!) in the right panel of the EClipse IDE... See figure below <a href="#fig:{{ fig_step3.5 }}"  target="_blank"> Figure {{ fig_step3.5 }} </a>

### Step 3.6:...

{% assign fig = fig | plus: 1 %}
{% assign fig_step3.6 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/13.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step3.6 }}" src="{{folderpath}}images/13.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step3.6 }}: Recognizing inconsistencies by means of RepairVision Tool and showing the detailed specifications in its panel  </figcaption>
</figure>

In this step you can follow the recognized inconsistencies if there is any and all the details and specifications of the inconsistencies and the needed changes to resolve them are depicted in terms of High-Level Edit Operations... See figure below <a href="#fig:{{ fig_step3.6 }}" target="_blank"> Figure {{ fig_step3.6 }} </a>


### Step 3.7:...

{% assign fig = fig | plus: 1 %}
{% assign fig_step3.7 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/14.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step3.7 }}" src="{{folderpath}}images/14.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step3.7 }}: Appying the recommended model changes by the RepairVision Tool</figcaption>
</figure>

Finally, You can Apply the recommended changes for resolving the consistencies and soon after checking the results. As shown in the following figure <a href="#fig:{{ fig_step3.7 }}"  target="_blank">Figure {{ fig_step3.7 }} </a>




