---
layout: page
title:  "Publications and Literature"
permalink: "/publications/"
exclude: false
order: 6
---

{% capture folderpath %}{{ site.url }}/{{ page.path | remove: page.name }}{% endcapture %}

<style>

.button {
  display: inline-block;
  border-radius: 4px;
  background-color: #1abc9c;
  border: 2px solid #1abc9c;
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

.dv {
  border: 2px solid lightgray;
  border-radius: 20px;
  margin: 2px 2px 2px;
  padding: 15px;
  background-color: white;
}

</style>

#### A History-based Approach for Model Repair Recommendations in Software Engineering

In: 2023, Inauguraldissertation der Philosophisch-naturwissenschaftlichen Fakultät der Universität Bern

_Manuel Ohrndorf_

<details>
<summary><strong>Read Abstract:</strong></summary>
<div class="dv">
<p align="justify"> 
Software is an everyday companion in today’s technology society that need to be evolved and maintained over long time periods. To manage the complexity of software projects, it has always been an effort to increase the level of abstraction during software development. Model-Driven Engineering (MDE) has shown to be a suitable method to raise abstraction levels during software development. Models are primary development artifacts in MDE that describe complex software systems from different viewpoints.
</p>
<p align="justify"> 
In MDE software projects, models are heavily edited through all stages of the development process. During this editing process, the models can become inconsistent due to uncertainties in the software design or various editing mistakes. While most inconsistencies can be tolerated temporarily, they need to be resolved eventually. The resolution of an inconsistency affecting a model’s design is typically a creative process that requires a developer’s expertise. Model repair recommendation tools can guide the developer through this process and propose a ranked list of repairs to resolve the inconsistency. However, such tools will only be accepted in practice if the list of recommendations is plausible and understandable to a developer. Current approaches mainly focus on exhaustive search strategies to generate improved versions of an inconsistent model. Such resolutions might not be understandable to developers, may not reflect the original intentions of an editing process, or just undo former work. Moreover, those tools typically resolve multiple inconsistencies at a time, which might lead to an incomprehensible composition of repair proposals.
</p>
<p align="justify">
This thesis proposes a history-based approach for model repair recommendations. The approach focuses on the detection and complementation of incomplete edit steps, which can be located in the editing history of a model. Edit steps are defined by consistency-preserving edit operations (CPEOs), which formally capture complex and error-prone modifications of a specific modeling language. A recognized incomplete edit step can either be undone or extended to a full execution of a CPEO. The final inconsistency resolution depends on the developer’s approval. The proposed recommendation approach is fully implemented and supported by our interactive repair tool called ReVision. The tool also includes configuration support to generate CPEOs by a semi-automated process.
</p>
<p align="justify"> 
The approach is evaluated using histories of real-world models obtained from popular open-source modeling projects hosted in the Eclipse Git repository. Our experimental results confirm our hypothesis that most of the inconsistencies, namely 93.4%, can be resolved by complementing incomplete edits. 92.6% of the generated repair proposals are relevant in the sense that their effect can be observed in the models’ histories. 94.9% of the relevant repair proposals are ranked at the topmost position. Our empirical results show that the presented history-based model recommendation approach allows developers to repair model inconsistencies efficiently and effectively.
</p>
</div>
</details>

<img src="{{folderpath}}images/2021tosem.png" itemprop="image" style="margin:auto; width:100%">

<button class="button" style="vertical-align:middle" onclick="window.open('https://ubbern.swisscovery.slsp.ch/permalink/41SLSP_UBE/17e6d97/alma99117481803805511', '_blank')"><span>Read Paper</span></button>

#### A Summary of ReVision: History-based Model Repair Recommendations

In: : Software Engineering 2023

_Manuel Ohrndorf, Christopher Pietsch, Udo Kelter, Lars Grunske, Timo Kehrer_

<details>
<summary><strong>Read Abstract:</strong></summary>
<div class="dv">
<p align="justify"> 
This work reports recent research results on history-based model repair recommendations in Model-Driven Engineering (MDE), originally published in Reference [Oh21]. Models in MDE are primary development artifacts that are heavily edited in all software development stages and can become temporarily inconsistent during editing. Model repair tools can support developers by proposing a list of the most promising repairs. Such repair recommendations will only be accepted in practice if the generated proposals are plausible and understandable and the set as a whole is manageable. 
</p>
<p align="justify"> 
Our interactive repair tool ReVision [Oh18], aims at generating repair proposals for inconsistencies introduced by past incomplete edit steps. Such an incomplete edit step is either undone or extended to the full execution of a consistency-preserving edit operation. We evaluate our approach using histories of real-world models from popular open-source modeling projects. Our experimental results confirm our hypothesis that most of the inconsistencies can be resolved by complementing incomplete edits. In fact, 92.2% of the proposed complementations could be observed in the model history.
</p>
</div>
</details>

<button class="button" style="vertical-align:middle" onclick="window.open('https://dl.gi.de/server/api/core/bitstreams/66b308f5-cf4c-433f-98fa-ed6ec3099ab9/content', '_blank')"><span>Read Paper</span></button>

#### History-based Model Repair Recommendations

In: 2021 ACM Transactions on Software Engineering and Methodology (TOSEM), Vol. 30, No. 2, Article 15.

_Manuel Ohrndorf, Christopher Pietsch, Udo Kelter, Lars Grunske, Timo Kehrer_

<details>
<summary><strong>Read Abstract:</strong></summary>
<div class="dv">
<p align="justify"> 
Models in Model-driven Engineering are primary development artifacts that are heavily edited in all stages of software development and that can become temporarily inconsistent during editing. In general, there are many alternatives to resolve an inconsistency, and which one is the most suitable depends on a variety of factors. As also proposed by recent approaches to model repair, it is reasonable to leave the actual choice and approval of a repair alternative to the discretion of the developer. Model repair tools can support developers by proposing a list of the most promising repairs. Such repair recommendations will be only accepted in practice if the generated proposals are plausible and understandable, and if the set as a whole is manageable. Current approaches, which mostly focus on exhaustive search strategies, exploring all possible model repairs without considering the intention of historic changes, fail in meeting these requirements.
</p>
<p align="justify"> 
In this article, we present a new approach to generate repair proposals that aims at inconsistencies that have been introduced by past incomplete edit steps that can be located in the version history of a model. Such an incomplete edit step is either undone or it is extended to a full execution of a consistency-preserving edit operation. The history-based analysis of inconsistencies as well as the generation of repair recommendations are fully automated, and all interactive selection steps are supported by our repair tool called ReVision. We evaluate our approach using histories of real-world models obtained from popular open-source modeling projects hosted in the Eclipse Git repository, including the evolution of the entire UML meta-model. Our experimental results confirm our hypothesis that most of the inconsistencies, namely, 93.4%, can be resolved by complementing incomplete edits. 92.6% of the generated repair proposals are relevant in the sense that their effect can be observed in the models’ histories. 94.9% of the relevant repair proposals are ranked at the topmost position.
</p>
</div>
</details>

<img src="{{folderpath}}images/2021tosem.png" itemprop="image" style="margin:auto; width:100%">

<button class="button" style="vertical-align:middle" onclick="window.open('https://dl.acm.org/doi/pdf/10.1145/3419017', '_blank')"><span>Read Paper</span></button>
  
#### ReVision: A Tool for History-based Model Repair Recommendations

In: 2018 IEEE/ACM 40th International Conference on Software Engineering: Companion (ICSE-Companion). Gothenburg, Sweden. May 27 - June 3, 2018.

_Manuel Ohrndorf, Christopher Pietsch, Udo Kelter, Timo Kehrer_

<details>
<summary><strong>Read Abstract:</strong></summary>
<div class="dv">
<p align="justify"> 
Models in Model-Driven Engineering are heavily edited in all stages of software development and can become temporarily inconsistent. In general, there are many alternatives to fix an inconsistency, the actual choice is left to the discretion of the developer. Model repair tools should support developers by proposing a short list of repair alternatives. Such recommendations will be only accepted in practice if the generated proposals are plausible and understandable. Current approaches, which mostly focus on fully automatic, non-interactive model repairs, fail in meeting these requirements. This paper proposes a new approach to generate repair proposals for inconsistencies that were introduced by incomplete editing processes which can be located in the version history of a model. Such an incomplete editing process is extended to a full execution of a consistency-preserving edit operation. We demonstrate our repair tool ReVision using a simplified multi-view UML model of a video on demand system, a screencast is provided at http://pi.informatik.uni-siegen.de/projects/SiLift/icse2018/.
</p>
</div>
</details>

<img src="{{folderpath}}images/2018icse.png" itemprop="image" style="margin:auto; width:100%">

<button class="button" style="vertical-align:middle" onclick="window.open('https://ieeexplore.ieee.org/abstract/document/8449456', '_blank')"><span>Read Paper</span></button>

#### Repair Examples

[Examples of model inconsistencies and their repairs collected from the literature.](/repairexamples/)

#### Behandlung von Inkonsistenzen in der verteilten Bearbeitung materialisierter Sichten im Kontext der modellbasierten Softwareentwicklung

Master's Thesis. University of Siegen. 2017.

_Manuel Ohrndorf_

<details>
<summary><strong>Read Abstract:</strong></summary>
<div class="dv"><p align="justify"> 
In software development, models are used for system analysis and design. In model-driven software development, models are primary artifacts and the formal basis for the system implementation. A model is an abstraction layer which conceals the technical target platform. This increases the reusability of the developed components.However, this requires the definition of a formal syntax and semantics for the modeling language. Models are usually expressed from various viewpoints, e.g. the data structure and a user interaction. A multi-view modeling environment can be used to build complex system models. A viewpoint can also be constructed by slicing a specific part of the model. This can be helpful in distributing and processing large models across a development team. However, a developer can inadvertently introduce inconsistencies between different views. Ensuring the correctness of a model is a key task of the development process. Therefore, the developers need fully-fledged tool support to deal with inconsistencies.  This work presents an approach to the repair of inconsistencies in a distributed multi-view modeling environment. The introduced tool determines repairs based on user-defined edit rules. To understand the cause of an inconsistency, the repair algorithm considers the modifications which have introduced the inconsistency.
</p></div>
</details>

<img src="{{folderpath}}images/2017thesis.png" itemprop="image" style="margin:auto; text-align:left; width:100%">

<button class="button" style="vertical-align:middle" onclick="window.open('http://pi.informatik.uni-siegen.de/mohrndorf/downloads/2017-04-29_mohrndorf_MA2017.pdf', '_blank')"><span>Read Thesis</span></button>
