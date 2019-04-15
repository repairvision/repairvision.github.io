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

In this Section, we illustrate the essential steps to install and work with ReVision. First, we show the [installation](installation) of ReVision. Second, we [setting up a running example](setting up-the-example-project). At the end, we show how to find and repair inconsistencies in the running example by [using ReVision](repairing-inconsistencies-with-revision).

{% capture folderpath %}
{{ site.url }}/{{ page.path | remove: page.name }}
{% endcapture %}

{% assign fig = 0 %}

#### Step 1: Installation

##### Step 1.1: Downlaod Eclipse

To begin with, first [download](#download-and-installation) and open the Eclipse IDE (Modeling Tools).

{% assign fig = fig | plus: 1 %}
{% assign fig_step1 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/01.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step1 }}" src="{{folderpath}}images/01.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step1 }}: Get Started </figcaption>
</figure>

##### Step 1.2: Install the ReVision Plug-in

Now you should install ReVision from the Eclipse Install Manager. Go to 'Help -> Install New Software...' and insert the [URL of the ReVision updatesite](#download-and-installation). To do so, click on Help and select Install New Software from the Options Menu. See <a href="#fig:{{ fig_step4 }}">Figure {{ fig_step2 }}</a> below.

{% assign fig = fig | plus: 1 %}
{% assign fig_step2 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/02.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step2 }}" src="{{folderpath}}images/02.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step2 }}: How to install new Software </figcaption>
</figure>

Afterward, you can proceed with the installation by just selecting all tool components and clicking next. See <a href="#fig:{{ fig_step3 }}"> Figure {{ fig_step3 }}</a> below.

{% assign fig = fig | plus: 1 %}
{% assign fig_step3 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/03.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step3 }}" src="{{folderpath}}images/03.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step3 }}: Download wizard for the Updating websites </figcaption>
</figure>

After finishing the installation, you're supposed to restart the Eclipse IDE to add the Tool to the IDE.

{% assign fig = fig | plus: 1 %}
{% assign fig_step4 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/04.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step4 }}" src="{{folderpath}}images/04.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step4 }}: Restart Eclipse to Save and Apply changes </figcaption>
</figure>

#### Step 2: Setting up the Example Project

##### Step 2.1: Adding the Repository

In the following, we will add the repository to our video-on-demand example model. To do so, click open perspective from the 'Window' menu and select 'SVN Repository Exploring', then click on the 'Open' Button (see <a href="#fig:{{ fig_step5 }}">Figure {{ fig_step5 }}</a>).

{% assign fig = fig | plus: 1 %}
{% assign fig_step5 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/05.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step5 }}" src="{{folderpath}}images/05.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step5 }}: Adding the Repository perspective </figcaption>
</figure>

In this step, you should add the [Example Project](repository URL) by clicking on 'New Repository Location' from 'File' menu. At the end, click on 'Finish' button (see <a href="#fig:{{ fig_step6 }}">Figure {{ fig_step6 }}</a>).

{% assign fig = fig | plus: 1 %}
{% assign fig_step6 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/06.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step6 }}" src="{{folderpath}}images/06.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step6 }}: Set the location of the Repository </figcaption>
</figure>

### Step 3: Repairing inconsistencies with ReVision

Now, it's time to check out the example from the repository. To do so, right click on the project folder and select 'Check Out' from option menu (see <a href="#fig:{{ fig_step7 }}"> Figure {{ fig_step7 }}</a>).

{% assign fig = fig | plus: 1 %}
{% assign fig_step7 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/07.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step7 }}" src="{{folderpath}}images/07.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step7 }}: properties of the UML Example created by RepairVision Tool </figcaption>
</figure>

##### Step 3.1: Opening the Model Editor

<a href="#fig:{{ fig_step8 }}"> Figure {{ fig_step8 }}</a> shows the UML class and sequence diagram of the video-on-demand example' after opening the 'uml.example.vod.di' in papyrus.

{% assign fig = fig | plus: 1 %}
{% assign fig_step8 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/08.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step8 }}" src="{{folderpath}}images/08.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step8 }}: Opening the UML Example </figcaption>
</figure>

##### Step 3.2: Adding the ReVision View

As shown in <a href="#fig:{{ fig_step11 }}"> Figure {{ fig_step11 }}</a> ReVision is placed in an additional view next to the model editor. To open the view, go to 'Show View', then 'Others' (see <a href="#fig:{{ fig_step9 }}"> Figure {{ fig_step9 }}</a>) and search for 'Model Repair' in the 'Show View' wizard (see <a href="#fig:{{ fig_step10 }}"> Figure {{ fig_step10 }}</a>). Finally, select and open the 'Model Repair' view.

{% assign fig = fig | plus: 1 %}
{% assign fig_step9 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/09.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step9 }}" src="{{folderpath}}images/09.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step9 }}: Having the view of the UML Diagram Editor </figcaption>
</figure>

{% assign fig = fig | plus: 1 %}
{% assign fig_step10 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/10.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step10 }}" src="{{folderpath}}images/10.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step10 }}: Adding the ModelRepair Tool Plugin in to the Eclipse Workspace </figcaption>
</figure>

{% assign fig = fig | plus: 1 %}
{% assign fig_step11 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/11.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step11 }}" src="{{folderpath}}images/11.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step11 }}: Showing the ModelRepair Tool Window panel in the Eclipse workspace </figcaption>
</figure>

##### Step 3.3: Validating and Searching for Repairs

In this step, we will validate the video-on-demand example model. In the view of ReVision (on right side in <a href="#fig:{{ fig_step12 }}"> Figure {{ fig_step12 }}</a>) click the bulb icon (in the toolbar) to start the validation of the currently opened model editor. After the validation is finished the recognized inconsistencies are shown in a list at the bottom of the view. Select the checkbox next to the inconsistency to start the repair calculation process. (This may take a few second the first time as ReVision will download and analyze the model history to provide an index of all past inconsistencies.)

{% assign fig = fig | plus: 1 %}
{% assign fig_step12 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/12.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step12 }}" src="{{folderpath}}images/12.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step12}}: Validation of the Input UML Example Class Diagram </figcaption>
</figure>

##### Step 3.4: Resolving Inconsistencies

<a href="#fig:{{ fig_step13 }}"> Figure {{ fig_step13 }}</a> shows the the ranked list of repairs that were generated by ReVision. Each repair contains 3 sets of information: 

* __Parameters:__ Some of the repairs have parameters that need to be supplied with additional arguments. For example, go to the parameter 'newLifeline' of the repair 'Move Operation And Sync Message'. Select the argument '<Lifeline> mirror' and then select 'Set Parameter' form the context menu or from the toolbar.
* __Recognized Changes:__ ReVision recognized these changes as origin of the defect of the inconsistency. Those changes were extracted from the version history of the model.
* __Complementing Changes:__ The changes that are proposed by ReVision to repair the selected inconsistency. The set of both change (Recognized and Complementing) refer to the consistency-preserving edit operation 'Move Operation And Sync Message'.

You can select the change sets or parameters and ReVision will highlight them in model editor.

{% assign fig = fig | plus: 1 %}
{% assign fig_step13 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/13.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step13 }}" src="{{folderpath}}images/13.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step13 }}: Recognizing inconsistencies by means of RepairVision Tool and showing the detailed specifications in its panel  </figcaption>
</figure>

Finally, you can apply the repair for resolving the inconsistency and soon after checking the results (see <a href="#fig:{{ fig_step17 }}">Figure {{ fig_step17 }}</a>).

{% assign fig = fig | plus: 1 %}
{% assign fig_step17 = fig %}

<figure class="aligncenter">
	<a href="{{folderpath}}images/14.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step17 }}" src="{{folderpath}}images/14.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step17 }}: Appying the recommended model changes by the RepairVision Tool</figcaption>
</figure>
