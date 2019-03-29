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

<!-- Load jQuery -->
<script src="{{ site.url }}/assets/js/jquery-1.12.2.min.js"></script>
<!-- Load Nivo Slider files -->
<script src="{{ site.url }}/assets/js/jquery.nivo.slider.pack.3.2.js"></script>
<script src="{{ site.url }}/assets/js/nivo-inner-zoom-min.js"></script>
<link rel="stylesheet" href="{{ site.url }}/assets/css/demo34-nivo-slider.css" type="text/css">

<!-- Nivo slider -->
<div style="text-align: center">    
	<div id="NivosliderD34oo" style="display: inline-block; width:90%; border:1px solid #611543;">
		<div class="nivoSlider" > 
			<img src="{{ folderpath }}images/01.png" title="<strong>Installation:</strong> Download the Eclipse Modeling Tools" alt=""/>
			<img src="{ folderpath }}images/02.png" title="Install New Software..." alt=""/>
			<img src="{ folderpath }}images/03.png" title="Copy and past the update site URL" alt=""/>
			<img src="{ folderpath }}images/04.png" title="Install ReVision (and required projects)" alt=""/>
			<img src="{ folderpath }}images/05.png" title="Open the version control system SVN perspective" alt=""/>
			<img src="{ folderpath }}images/06.png" title="Copy and past the VoD example repository URL" alt=""/>
			<img src="{ folderpath }}images/07.png" title="Check out the UML project" alt=""/>
			<img src="{ folderpath }}images/08.png" title="Open the Papyrus diagrams" alt=""/>
			<img src="{ folderpath }}images/09.png" title="Go to Window -> Show View -> Other..." alt=""/>	
			<img src="{ folderpath }}images/10.png" title="Open the Model Repair View" alt=""/>
			<img src="{ folderpath }}images/11.png" title="Validate the opened UML model" alt=""/>
			<img src="{ folderpath }}images/12.png" title="Select the inconsistency to be repaired" alt=""/>
			<img src="{ folderpath }}images/13.png" title="Set the repair parameters" alt=""/>
			<img src="{ folderpath }}images/14.png" title="Apply the repair" alt=""/>
		</div>
	</div>
</div>

<script>
<!-- Nivo Slider Load-->
$(window).load(function() {
	$('.nivoSlider').nivoSlider({
		effect:'boxRandom',
      boxCols:2,                     
      boxRows:2,
		pauseOnHover:true,
      afterLoad:function () {NivoInnerZoom()},
      beforeChange:function () {IZhide()},
		afterChange:function () {NivoInnerZoom()}
	});
});

$('.noFooter').on('click', function() {window.location.href ='http://www.soslignes-ecrivain-public.fr/Inner-zoom-plugin-Nivo-Slider.html';});
</script>
