---
layout: post
date: 2019-03-27 14:28
title: "History-based Model Repair Recommendations"
description: Introduction to ReVision
comments: false
---

Models in Model-Drive nEngineering are heavily edited in all stages of software development and can become temporarily inconsistent. In general, there are many alternatives to fix an inconsistency, the actual choice is left to the discretion of the developer. Model repair tools should support developers by proposing a short list of repair alternatives. Such recommendations will be only accepted in practice if the generated proposals are plausible and understandable. Current approaches, which mostly focus on fully automatic, non- interactive model repairs, fail in meeting these requirements. This paper proposes a new approach to generate repair proposals which is based on the assumption that inconsistencies are introduced by incomplete editing processes which can be located in the version history of a model. Such an incomplete editing process is either  undone or it is extended to a full execution of a consistency-preserving edit operation. We showcase the usage and benefits of our repair tool ReVision using a simplified multi-view UML model of a video on demand system.

# Tooldemo

* <a href="https://youtu.be/k2OaGVwBnf8" target="new">Watch on YouTube</a>
* <strong>Introduction: &#91;0:35&#93;:</strong> <a href="https://youtu.be/k2OaGVwBnf8?t=35" target="new">Running Example VoD-System</a>
* <strong>History Analysis: &#91;2:03&#93;:</strong> <a href="https://youtu.be/k2OaGVwBnf8?t=123" target="new">Understanding the Inconsistency</a>
* <strong>First Corrective Edit Step: &#91;3:45&#93;:</strong> <a href="https://youtu.be/k2OaGVwBnf8?t=225" target="new">Correction of the Message Receiver</a>
* <strong>Second Corrective Edit Step:&#91;4:21&#93;:</strong> <a href="https://youtu.be/k2OaGVwBnf8?t=261" target="new">Correction of the Message Sender</a>

<iframe width="560" height="315" src="https://www.youtube.com/embed/k2OaGVwBnf8" frameborder="0" allowfullscreen></iframe>
