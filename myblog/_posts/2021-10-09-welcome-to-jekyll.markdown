---
layout: post
title:  "Operations for Autonomous Spacecraft"
date:   2021-10-09 13:36:32 -0700
timePeriod: 6 months
Roles: Lead designer
Responsibility1: Architected ops tool suite of 8 tools and implemented UI designs
Responsibility2: Designed Operations Concept
Responsibility3: Produced 3 day simulation of operations, leading a team of 2
Summary: Develop operations concept and tool suite for an autonomous mission, then simulate operations with a team of operators in order to evaluate and improve on design decisions
ProblemStatement: Onboard autonomy has the potential to increase the science return of JPL missions, but the impact of autonomy to operations is not well understood and considered risky and overly complicated for missions to adopt. 
---


<h2 class="pt-2">Background and Motivations</h2>
<div class="row pb-5">
	<div class="col-sm-8">
		<p>Currently, to collect science, operators program a linear sequence of behaviors and time them based on worst case. Goal based operations means the spacecraft has the flexibility to create a schedule using its knowledge of state. As a result the spacecraft has no flexibility to shuffle them around or lengthen or shorten times based on its environment.</p>
	</div>
	<div class="col-sm-4">
		<img class="img-fluid" src="/assets/images/test_1.png">
	</div>
</div>
<div class="row pb-5">
	<div class="col-sm-8">
		<blockquote class="h1">	&ldquo;I don’t want to have to call in [world expert on autonomy] to debug my spacecraft &rdquo; (paraphrased)</blockquote>
	</div>
	<div class="col-sm-4">
		<p>The goal based paradigm has limited traction on JPL because of its complexity and unknown impact to operations. This limits exploration at far away targets and targets with rapidly changing environments, such as the Neptune System</p>
	</div>
</div>

<h2 class="pt-2">Design Foundation</h2>
<div class="row pb-5">
	<div class="col-sm-8">
		<p>I’m trying to understand the impact of and best practices for autonomy through prototyping and user studies. I led 2 workshops bring technologists and users together to imagine the new paradigm. Downlink Workshop - Identified need for autonomy engineer and phase for debugging spacecraft behavior. Given our time constraints, I conducted historical research to leverage existing work. Additional research identifies resource conflicts between scientists as the fundamental tension. Other design reports at JPL have discussed how siloed tools give limited visibility into changes that could impact the mission</p>
	</div>
	<div class="col-sm-4">
		<img class="img-fluid" src="/assets/images/test_1.png">
	</div>
</div>








