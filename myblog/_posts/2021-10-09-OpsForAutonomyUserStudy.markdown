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


<h2 class="pt-5">Background and Motivations</h2>
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

<h2 class="pt-5">Design Foundation</h2>
<div class="row pb-5">
	<div class="col-sm-8">
		<p>I’m trying to understand the impact of and best practices for autonomy through prototyping and user studies. I led 2 workshops bring technologists and users together to imagine the new paradigm. Downlink Workshop - Identified need for autonomy engineer and phase for debugging spacecraft behavior. Given our time constraints, I conducted historical research to leverage existing work. Additional research identifies resource conflicts between scientists as the fundamental tension. Other design reports at JPL have discussed how siloed tools give limited visibility into changes that could impact the mission</p>
	</div>
	<div class="col-sm-4">
		<img class="img-fluid" src="/assets/images/test_1.png"> 
	</div>
</div>
<div class="row">
	<div class="col">
		<img class="img-fluid" src="/assets/images/EarlyStoryboard.png"> 
	</div>
</div>

<h2 class="pt-5">Tools and Design Principles</h2>
<div class="row pb-5">
	<div class="col-sm-8">
		<p>I produced a set of tools and an operations framework based on the findings. We did not focus on polish at this stage, because we expected them to continue to evolve as a result of the study.</p>
	</div>
</div>
<div class="row">
	<div class="col-sm-6"> 
		<p>Performance and fidelity tradeoff</p>
	</div>
	<div class="col-sm-6"> 
		<p>Predictability and control trade off</p>
	</div>
</div>
<div class="row">
	<div class="col-sm-6"> 
		<img class="img-fluid" src="/assets/images/ScreenshotSciencePlanning.png"> 
	</div>
	<div class="col-sm-6"> 
		<img class="img-fluid" src="/assets/images/ScreenshotMissionPlanning.png"> 
	</div>
</div>
<div class="row">
	<div class="col-sm-6"> 
		<img class="img-fluid" src="/assets/images/ScreenshotGoalDesign.png"> 
	</div>
	<div class="col-sm-6"> 
		<img class="img-fluid" src="/assets/images/ScreenshotTasknet.png"> 
		<span class="footnote">Our intern Bennett Huffman designed this tool based on initial sketches from previous work</span>
	</div>
</div>
<div class="row">
	<div class="col-sm-6"> 
		<p>Support correlation</p>
		<img class="img-fluid" src="/assets/images/ScreenshotTasknetCorrelation.png"> 
	</div>
	<div class="col-sm-6"> 
		<p>Support visibility across plans and emergent properties</p>
		<img class="img-fluid" src="/assets/images/ScreenshotObservationSearch.png"> 
	</div>
</div>

<h2 class="pt-5">User Study</h2>
<div class="row">
	<div class="col-sm-4"> 
		<p>Our design team produced a 3 day study to evaluate our concept and answer our research questions</p>
	</div>
	<div class="col-sm-8"> 
		<ul>
			<li>Are operators given the right software tools and very rough draft ops con for modeling autonomous behaviors? </li>
			<li>During downlink, can operators understand enough about the autonomous decisions to ensure the health and safety of the spacecraft?</li>
			<li>Are operators able to conclude what happened onboard and why?</li>
			<li>Do operators understand the predicted outcome of their plan given the predictions of autonomous behaviors? </li>
			<li>Do operators trust the predicted outcome of their plan given the predictions?</li>
		</ul>
	</div>
</div>
<div class="row">
	<div class="col-sm-6"> 
		<p>I brought together Subject Experts in another workshop to ideate on stories for the study and reach a consensus</p>
	</div>
</div>
<div class="row">
	<div class="col"> 
		<img class="img-fluid" src="/assets/images/UserStudyStory2.png"> 
	</div>
</div>
<div class="row">
	<div class="col-sm-6"> 
		<img class="img-fluid" src="/assets/images/UserStudyStory1.png"> 
	</div>
	<div class="col-sm-6"> 
		<img class="img-fluid" src="/assets/images/PlumeX.png"> 
	</div>
</div>

<h2 class="pt-5">User Study Results</h2>
<div class="row pb-5 mb-5">
	<div class="col-sm-6"> 
		<p>In general, participants relied on the tools as we expected, confirming our workflow. We identified some opportunities for improvement and interesting user behavior.</p>
		<ul>
			<li>While low fidelity was helpful, we should explore the spectrum more to find the sweet spot</li>
			<li>Scientists who had a lower probability of observing their plume saw it as an overall loss</li>
			<li>The team used clusters of plans to structure their discussion</li>
		</ul>
	</div>
	<div class="col-sm-6"> 
		<img class="img-fluid" src="/assets/images/ZoomParticipants.png"> 
		<p class="footnote">Image Credit: Erin Murphy</p>
	</div>
</div>







