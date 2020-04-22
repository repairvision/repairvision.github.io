---
layout: page
title:  "Getting Started"
permalink: "/gettingstarted/"
order: 5
---

{% capture folderpath %}{{ site.url }}/{{ page.path | remove: page.name }}{% endcapture %}

{% assign eclipseversion = '2020-03' %}
{% assign eclipseversionurl = 'https://www.eclipse.org/downloads/packages/release/2020-03/r/eclipse-modeling-tools' %}

{% assign subclipseupdatesite = 'https://dl.bintray.com/subclipse/releases/subclipse/latest/' %}
{% assign papyrusupdatesite = 'http://download.eclipse.org/modeling/mdt/papyrus/updates/releases/2019-03' %}

{% assign revisionupdatesite = 'https://repairvision.github.io/updatesite/releases/latest' %}

{% assign exampleproject = 'https://github.com/mohrndorf/revision-example.git' %}

### Download and Installation

1. Download Eclipse Platform: <a href="{{ eclipseversionurl }}" target="new">Eclipse {{ eclipseversion }} Modeling Tools</a><br/>(includes the Eclipse Modeling Framework):
1. The newest version of __ReVision__ can be obtained from the following update site:
   * __{{ revisionupdatesite }}__
   * Provides an All-In-One update including SVNKit (for repository integration) and Papyrus (for UML modeling) from the following update sites:
    * {{ subclipseupdatesite }}
    * {{ papyrusupdatesite }}
     
### Example Project

1. Import Video on Demand System (UML) Project via SVN repository:
   * __{{ exampleproject }}__

### Quick Introduction

In this Section, we illustrate the essential steps to install and work with ReVision. First, we show the [installation](#step-1-installation) of ReVision. Second, we [setting up a running example](#step-2-setting-up-the-example-project). At the end, we show how to find and repair inconsistencies in the running example by [using ReVision](#step-3-repairing-inconsistencies-with-revision).

{% assign fig = 0 %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step1 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step2 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step3 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step4 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step5 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step6 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step7 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step8 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step9 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step10 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step11 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step12 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step13 = fig %}

{% assign fig = fig | plus: 1 %}
{% assign fig_step14 = fig %}

#### Step 1: Installation

##### Step 1.1: Downlaod Eclipse

To begin with, first [download](#download-and-installation) and open the Eclipse IDE (Modeling Tools).

<figure class="aligncenter">
	<a href="{{folderpath}}images/01.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step1 }}" src="{{folderpath}}images/01.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step1 }}: New installation of Eclipse</figcaption>
</figure>

##### Step 1.2: Install the ReVision Plug-in

Now you should install ReVision from the Eclipse Install Manager. Go to 'Help -> Install New Software...' and insert the URLs of the update sites and follow the installation process for required tools and ReVision. To do so, click on Help and select Install New Software from the Options Menu. See <a href="#fig:{{ fig_step2 }}">Figure {{ fig_step2 }}</a> below.

<figure class="aligncenter">
	<a href="{{folderpath}}images/02.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step2 }}" src="{{folderpath}}images/02.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step2 }}: Install new software </figcaption>
</figure>

Afterward, you can proceed with the installation of the ReVision selecting the the plug-ins from the update site (__{{ revisionupdatesite }}__). See <a href="#fig:{{ fig_step3 }}"> Figure {{ fig_step3 }}</a> below.

<figure class="aligncenter">
	<a href="{{folderpath}}images/03.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step3 }}" src="{{folderpath}}images/03.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step3 }}: Instllation Wizard for ReVision</figcaption>
</figure>

After finishing the installations, you're supposed to restart the Eclipse IDE to add the Tool to the IDE.

<figure class="aligncenter">
	<a href="{{folderpath}}images/04.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step4 }}" src="{{folderpath}}images/04.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step4 }}: Restart Eclipse to save and apply changes </figcaption>
</figure>

#### Step 2: Setting up the Example Project

##### Step 2.1: Adding the Repository

In the following, we will add the repository to our video-on-demand example model. To do so, click open perspective from the 'Window' menu and select 'SVN Repository Exploring', then click on the 'Open' Button (see <a href="#fig:{{ fig_step5 }}">Figure {{ fig_step5 }}</a>).

<figure class="aligncenter">
	<a href="{{folderpath}}images/05.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step5 }}" src="{{folderpath}}images/05.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step5 }}: Adding the Repository perspective </figcaption>
</figure>

In this step, you should add the [Example Project](repository URL) by clicking on 'New Repository Location' from 'File' menu. At the end, click on 'Finish' button (see <a href="#fig:{{ fig_step6 }}">Figure {{ fig_step6 }}</a>).

<figure class="aligncenter">
	<a href="{{folderpath}}images/06.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step6 }}" src="{{folderpath}}images/06.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step6 }}: Setup the location of the repository </figcaption>
</figure>

### Step 3: Repairing inconsistencies with ReVision

Now, it's time to check out the example from the repository. To do so, right click on the project folder and select 'Check Out' from option menu (see <a href="#fig:{{ fig_step7 }}"> Figure {{ fig_step7 }}</a>).

<figure class="aligncenter">
	<a href="{{folderpath}}images/07.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step7 }}" src="{{folderpath}}images/07.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step7 }}: Check-out the example project</figcaption>
</figure>

##### Step 3.1: Opening the Model Editor

<a href="#fig:{{ fig_step8 }}"> Figure {{ fig_step8 }}</a> shows the UML class and sequence diagram of the video-on-demand example' after opening the 'uml.example.vod.di' in papyrus.

<figure class="aligncenter">
	<a href="{{folderpath}}images/08.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step8 }}" src="{{folderpath}}images/08.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step8 }}: Opening the UML class and sequence diagram editor</figcaption>
</figure>

##### Step 3.2: Adding the ReVision View

As shown in <a href="#fig:{{ fig_step11 }}"> Figure {{ fig_step11 }}</a> ReVision is placed in an additional view next to the model editor. To open the view, go to 'Show View', then 'Others' (see <a href="#fig:{{ fig_step9 }}"> Figure {{ fig_step9 }}</a>) and search for 'Model Repair' in the 'Show View' wizard (see <a href="#fig:{{ fig_step10 }}"> Figure {{ fig_step10 }}</a>). Finally, select and open the 'Model Repair' view.

<figure class="aligncenter">
	<a href="{{folderpath}}images/09.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step9 }}" src="{{folderpath}}images/09.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step9 }}: Open the ReVision view</figcaption>
</figure>

<figure class="aligncenter">
	<a href="{{folderpath}}images/10.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step10 }}" src="{{folderpath}}images/10.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step10 }}: Search for the ReVision view</figcaption>
</figure>

<figure class="aligncenter">
	<a href="{{folderpath}}images/11.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step11 }}" src="{{folderpath}}images/11.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step11 }}: Opened ReVision view (on the right side)</figcaption>
</figure>

##### Step 3.3: Validating and Searching for Repairs

In this step, we will validate the video-on-demand example model. In the view of ReVision (on right side in <a href="#fig:{{ fig_step12 }}"> Figure {{ fig_step12 }}</a>) click the bulb icon (in the toolbar) to start the validation of the currently opened model editor. After the validation is finished the recognized inconsistencies are shown in a list at the bottom of the view. Select the checkbox next to the inconsistency to start the repair calculation process. (This may take a few second the first time as ReVision will download and analyze the model history to provide an index of all past inconsistencies.)

<figure class="aligncenter">
	<a href="{{folderpath}}images/12.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step12 }}" src="{{folderpath}}images/12.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step12}}: Validation of the video-on-demand sytem example</figcaption>
</figure>

##### Step 3.4: Resolving Inconsistencies

<a href="#fig:{{ fig_step13 }}"> Figure {{ fig_step13 }}</a> shows the the ranked list of repairs that were generated by ReVision. Each repair contains 3 sets of information: 

* __Parameters:__ Some of the repairs have parameters that need to be supplied with additional arguments. For example, go to the parameter 'newLifeline' of the repair 'Move Operation And Sync Message'. Select the argument '<Lifeline> mirror' and then select 'Set Parameter' form the context menu or from the toolbar.
* __Recognized Changes:__ ReVision recognized these changes as origin of the defect of the inconsistency. Those changes were extracted from the version history of the model.
* __Complementing Changes:__ The changes that are proposed by ReVision to repair the selected inconsistency. The set of both change (Recognized and Complementing) refer to the consistency-preserving edit operation 'Move Operation And Sync Message'.

You can select the change sets or parameters and ReVision will highlight them in model editor (see <a href="#fig:{{ fig_step14 }}">Figure {{ fig_step14 }}</a>).

<figure class="aligncenter">
	<a href="{{folderpath}}images/13.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step13 }}" src="{{folderpath}}images/13.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step13 }}: Binding repair parameters to values</figcaption>
</figure>

Finally, you can apply the repair for resolving the inconsistency and soon after checking the results (see <a href="#fig:{{ fig_step14 }}">Figure {{ fig_step14 }}</a>).

<figure class="aligncenter">
	<a href="{{folderpath}}images/14.png" target="_blank">
	<img style="width: 400px" id="fig:{{ fig_step14 }}" src="{{folderpath}}images/14.png"/></a>
	<figcaption style="text-align: center">Fig. {{ fig_step14 }}: Appying the repair</figcaption>
</figure>
