---
layout: page
title:  "Publications"
permalink: "/publications/"
order: 7
---

<style>
.tx:hover{
color:  #1abc9c;
}
</style>


<style>
.button {
  display: inline-block;
  border-radius: 10px;
  background-color: #1abc9c;
  border: none;
  color: white;
  text-align: center;
  font-size: 15px;
  width: 200px;
  transition: all 0.5s;
  cursor: pointer;
  margin: 5px;
}
.button:hover {
  background-color: white; 
  color: white; 
  border: 2px solid #1abc9c;
}

.button span {

  cursor: pointer;
  display: inline-block;
  position: relative;
  transition: 0.5s;
}

.button span:after {
  content: '\00bb';
  position: absolute;
  opacity: 0;
  top: 0;
  right: -20px;
  transition: 0.5s;

}

.button:hover span {
color: #1abc9c;
  padding-right: 25px;
}

.button:hover span:after {
  opacity: 1;
  right: 0;
}
</style>  

<style>
.dv {
  border: 2px solid lightgray;
  border-radius: 20px;
  margin: 2px 2px 2px;
  padding: 15px;
  background-color: white;
}
</style>
 
 
 
<div class="tx">
<b><p>ReVision: A Tool for History-Based Model Repair Recommendations</p></b>
</div>
   <ul>  
      <li>Manuel Ohrndorf, Christopher Pietsch, Udo Kelter, Timo Kehrer</li>
      <li>In: 2018 IEEE/ACM 40th International Conference on Software 
          Engineering: Companion (ICSE-Companion). Gothenburg, Sweden. May 27 - 
          June 3, 2018.</li>  
   </ul>

<details>
<summary>Read Abstract: </summary>
<br></br>
<div class=dv>
<p align="JUSTIFY"> Models in Model-Driven Engineering are heavily edited in all stages of software development and can become temporarily inconsistent. In general, there are many alternatives to fix an inconsistency, the actual choice is left to the discretion of the developer. Model repair tools should support developers by proposing a short list of repair alternatives. Such recommendations will be only accepted in practice if the generated proposals are plausible and understandable. Current approaches, which mostly focus on fully automatic, non-interactive model repairs, fail in meeting these requirements. This paper proposes a new approach to generate repair proposals for inconsistencies that were introduced by incomplete editing processes which can be located in the version history of a model. Such an incomplete editing process is extended to a full execution of a consistency-preserving edit operation. We demonstrate our repair tool \toolname using a simplified multi-view UML model of a video on demand system, a screencast is provided at http://pi.informatik.uni-siegen.de/projects/SiLift/icse2018/.</p>
</div>
 
</details>

<br></br>

<img src="test1.gif" itemprop="image" style="margin:auto; width:200px; height:200px">

<br></br>
<button class="button" style="vertical-align:middle" onclick="window.location.href = 'https://ieeexplore.ieee.org/abstract/document/8449456';"><span>Read Paper</span></button>
<br></br>


<div class="tx">
<b><p>Behandlung
 von Inkonsistenzen in der verteilten Bearbeitung materialisierter 
Sichten im Kontext der modellbasierten Softwareentwicklung</p></b>
</div>
    <ul>
      <li>Manuel Ohrndorf</li>
      <li>Master’s Thesis. University of Siegen. 2017.</li>
    </ul>
     

<details>
<summary>Read Abstract:  </summary>
<br></br>
<div class=dv>
  <p align="JUSTIFY"> In software development, models are used for system analysis and de-sign. In model-driven software development, models are primary artifacts and the formalbasis for the system implementation. A model is an abstraction layer which conceals thetechnical target platform. This increases the re-usability of the developed components.However, this requires the definition of a formal syntax and semantics for the modelinglanguage. Models are usually expressed from various viewpoints, e.g. the data struc-ture and a user interaction. A multi-view modeling environment can be used to buildcomplex system models. A viewpoint can also be constructed by slicing a specific partof the model. This can be helpful in distributing and processing large models acrossa development team. However, a developer can inadvertently introduce inconsistenciesbetween different views. Ensuring the correctness of a model is a key task of the devel-opment process. Therefor, the developers need fully-fledged tool support to deal withinconsistencies.  This work presents an approach to the repair of inconsistencies in adistributed multi-view modeling environment. The introduced tool determines repairsbased on user-defined edit rules. To understand the cause of an inconsistency, the repairalgorithm considers the modifications which have introduced the inconsistency.</p>
</div>
</details>

<br></br>

<img src="test2.png" itemprop="image" style="margin:auto; width:200px; height:200px">

<br></br>
<button class="button" style="vertical-align:middle" onclick="window.location.href = 'http://pi.informatik.uni-siegen.de/mohrndorf/downloads/2017-04-29_mohrndorf_MA2017.pdf';"><span>Read Paper</span></button>
<br></br>

