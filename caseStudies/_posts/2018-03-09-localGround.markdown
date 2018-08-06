---
layout: post
title:  Local Ground
date:   2018-03-10 11:15:38 -0800
type: casestudy
tags:
  - UX
  - Visual + Front End Design
  - HTML/CSS/JS

where: UC Berkeley Research

image: /assets/home-images/localground.png

overview: Local Ground is an open source tool for collaboratively creating map visualizations and stories built for an education research project at Berkeley. It features a combination of qualitative (photos, narrative, hand drawings overlaid on the map), and quantitative (numerical) data to tell powerful stories and solve problems. Past Local Ground projects include <a href = 'http://dl.acm.org/citation.cfm?id=1926194'>youth led urban planning</a> and <a href = 'http://tap2k.org/papers/ICLS2016.pdf'>elementary school science</a>. 

tagline: Story map builder for UC Berkeley education research

outsideurl: http://people.ischool.berkeley.edu/~ejvw/lg-redesign/media.html

outsidetitle: Interactive Prototype

---

<div class="design-feature">
	<img class="broswer-screenshot" src = "/assets/LOCALGROUND/header2.png">
</div>


## The Problem and Needs



V1 of Local Ground had already been used for a few research projects. While the researchers had found that their users engaged with location data in novel ways, and served existing needs, the app had usability issues that slowed down the process and interfered with learning goals. They also wanted to expand the capabilities to support storytelling better.

<div class="design-feature">
	<img src = "/assets/LOCALGROUND/localground-usecases.png">
</div>

Use cases clockwise from left: 
* **[Five Dollar Challenge:](http://www.code510.org/yri/fdc/#)** NPR listeners across the country submitted their five dollar meals to compare food prices across the country.
* **[Elementary Science:](http://tap2k.org/papers/ICLS2016.pdf)** Students conducted a biology experiment. They measured soil moisture and compared that with the numbers and kinds of bugs they found, as a way of building spatial reasoning and learning about correlation.
* **[Participatory GIS:](http://tap2k.org/papers/localground_dev10.pdf)** High schoolers documented their experiences with their community as part of a park designing project. 


## Heuristic Evaluation + Research
<div class="row design-feature-split">
  <div class = "col-sm-6">

  </div>
 </div>


<div class="row design-feature-split">
  <figure class = "col-sm-6">
  	<img src="/assets/LOCALGROUND/competitive-analysis.png" alt = "competitive analysis screenshot" >
  	 <figcaption class = "center"><span>A sample of my competitive research, where I describe pros and cons and lay out an annotated walk through </span></figcaption>
  </figure>
  <div class = "col-sm-6"> 
	<p>I started the redesign by researching the existing use cases and usability feedback, speaking with stakeholders, and conducting a <span class = "skill">heuristic evaluation</span>.</p>
	<p>I also conducted <span class = "skill">competitive research</span> in order to better define Local Ground as a product and to understand common UI patterns. My findings include the following:</p>
  </div>
</div>
* **Increase Accessibility:** The existing Local Ground UI was modeled after the database representation of data. While this can be useful pedagogically, it presents a high barrier to entry and excludes some users.			
* **Improve Storytelling:** Local Ground doesn't support turning individual data points into a coherent story.

The competitive analysis inspired possible layouts for the redesign

<div class="design-feature row">
  <figure class = "col-sm-4">
  	<img src="/assets/LOCALGROUND/pin-sketches.jpg" alt = "competitive analysis screenshot" >
  	 <figcaption class = "center"><span><strong>Pin and detail:</strong> Considering how to display the details of a location </span></figcaption>
  </figure>
  <figure class = "col-sm-4">
  	<img src="/assets/LOCALGROUND/layout-sketches.jpg" alt = "competitive analysis screenshot" >
  	 <figcaption class = "center"><span><strong>Layout:</strong> Different options for how to navigate data display.s</span></figcaption>
  </figure>
  <figure class = "col-sm-4">
  	<img src="/assets/LOCALGROUND/project-sketches.jpg" alt = "competitive analysis screenshot" >
  	 <figcaption class = "center"><span><strong>Project toggle options</strong> </span></figcaption>
  </figure>
</div>

## Wireframing

Through the process of sketching, wireframing, and getting feedback from our developer/researcher, I formalized the wireframes which included the following large structural changes:


* **Support media and browsing better:** Move the description/media display to panel on the right instead of a popover. The popover supports short descriptions well, but long descriptions obscured the map. The right panel also achieves our goal of foregrounding media and content.
<div class="change-illustration"><img src="/assets/LOCALGROUND/wireframe-1.png" alt = "illustration showing the original popup and then the proposed right panel ">
</div>
	
* **Clean up map:**Initially, media were plotted on the map as their media type. This meant that multiple photos for a single location might be stacked on top of each other as individual instances. Since the photo thumbnails were used for the map pins, this created additional visual confusion. I proposed requiring each photo to be contained in a site in order to be plotted on the map.
<div class="change-illustration">
	<img src="/assets/LOCALGROUND/wireframe-2.png" alt = "illustration showing a cluster of photos then a single pin">
</div>
	
* **Use "Projects" to organize:** In the existing version, users switch between projects by turning on and off datasets, and the map preferences (such as map skin and center) are saved as cookies. I recommended making a separate page for each project to better facilitate work on a single project and fit common mental models.

My team went out into the city of Berkeley and photographed public artwork. Using real data helps me design for the worst case scenarios, and resulted in an interesting mini project to present at the Local Ground workshop.

Below are some key screens from the site.

<div class="design-feature">
	<img src="/assets/LOCALGROUND/lg-prototype.png"  title="IMAGE: SITS TAB  In this view, users can edit their data, including media, in bulk. Media and sites can be presented as either a card or spreadsheet view">
</div>

Once I had resolved the overall layout in the wireframes, I turned it into a <a href="http://people.ischool.berkeley.edu/~ejvw/lg-redesign-old/index.html">prototype</a> for usability testing. There would be a lot of interaction that would be hard to maintain with static mockups, and would make Axure very slow, so I chose HTML/CSS/JS.

## 2 Rounds of User Testing

I conducted 2 rounds of testing with 5 participants each. Research sessions included an <span class = "skill">interview</span> on previous exposure to map making software and Local Ground, and then a series of <span class = "skill">tasks</span>. Our main findings included the following:

* **Improved workflow:** Overall, users who had experience with the old design found that the new design better foregrounded the tasks they needed to complete.
	
* **Fix Terminology and hierarchy:** We confirmed that some of our labeling terminology and the hierarchy was confusing and seemed arbitrary. I began to conduct additional research on mapping and GIS terminology for inspiration.

* **Visible feedback:** Initially, the dialogue for creating a visualization happened in a modal window; a pattern used in other GIS software. However, users weren't sure what they were actually doing when trying to complete tasks. So I moved the modal to a panel, and subsequent users did not experience the same problems.
<div class="change-illustration">
	<img src="/assets/LOCALGROUND/wireframe-3.png" alt = "illustration showing the original popup and then the proposed right panel ">
</div>

* **Separate out data** There are use cases for displaying both data and sites on the map. However these activites are separate, and should be moved into separate tabs

* **Offer Greater Flexibility:** While the idea of sites is helpful, there is no reason to limit the options for the display of media and sites. This means bringing the map view to the data tab, and allowing the detail view and edits there.

* **Foreground Collaboration** In my prototype, combining layers was an afterthought in the modal when sharing. Users wanted to know where this was, so we moved it to the right pane to be a "core" feature

* **Logical Hierarchy:** It makes more sense to start with the overview on the left, which opens the detail view on the right.



## Visual Design

I used material design guidelines to guide the visual design. This is appropriate for Local Ground's origins as a tool that overlays hand drawn maps onto digital maps. In to foreground user content and avoid pandering to younger users, I used a simple, light, and modern color palette.




## Final Design with Test Notes



<div class="design-feature">
	<img src="/assets/LOCALGROUND/lg-final.png"  title="IMAGE: SITS TAB  In this view, users can edit their data, including media, in bulk. Media and sites can be presented as either a card or spreadsheet view">
</div>
<!--<img class = "displayed full-width" 
src = "/assets/lg-wireframe1.png">-->
