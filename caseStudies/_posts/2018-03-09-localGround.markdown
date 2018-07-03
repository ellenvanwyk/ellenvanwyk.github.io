---
layout: post

title:  Local Ground

date:   2018-03-10 11:15:38 -0800

tags:
  - UX
  - Visual + Front End Design
  - Research
  - HTML/CSS/JS

image: /assets/home-images/localground.png

overview: Local Ground is an open source tool for collaboratively creating map visualizations and stories built for an education research project at Berkeley. It features a combination of qualitative (photos, narrative), and quantitative (numerical) data to tell powerful stories and solve problems. Past Local Ground projects include <a href = 'http://dl.acm.org/citation.cfm?id=1926194'>youth led urban planning</a> and <a href = 'http://tap2k.org/papers/ICLS2016.pdf'>elementary school science</a>. 

tagline: Story map builder for UC Berkeley education research


---

<div class="design-feature">
	<img class="broswer-screenshot" src = "/assets/LOCALGROUND/header2.png" style = "width:100%;">
</div>


## The Problem and Needs



V1 of Local Ground had already been used for a few research projects. While the researchers had found that their users engaged with location data in novel ways, and served existing needs, the app had usability flaws that slowed down the process and interfered with learning goals.

## Heuristic Evaluation + Research

I started the redesign by researching the existing use cases and usability feedback, speaking with stakeholders, and conducting a <span class = "skill">heuristic evaluation</span>. I also conducted <span class = "skill">competitive research</span> in order to better define Local Ground as a product and to understand common UI patterns. My findings include the following:

* <span class = "bullet-lead">Increase Accessibility: </span>The existing Local Ground UI was modeled after the database representation of data. While this can be useful pedagogically, it presents a high barrier to entry and excludes some users.
* <span class = "bullet-lead">Market Opportunity: </span>Map making tools fall under one of the following categories: quantitative and story/visuals oriented. We have the unique opportunity and challenge to straddle these two spaces. The former systems tend towards technical power users, while the latter are easy to learn and use. None of these tools feature decentralized data collection.


## Wireframing

When I felt comfortable with the existing product, usability issues, and landscape, I began to create <span class = "skill">wireframes in Sketch</span> to communicate my suggestions, which included the following large structural changes:


* <span class = "bullet-lead">Support media and browsing better: </span>Move the description/media display to panel on the right instead of a popover. The popover supports short descriptions well, but long descriptions obscured the map. The right panel also achieves our goal of foregrounding media and content.
<div style="text-align: center;"><img src="/assets/LOCALGROUND/wireframe-1.png" style="width:80%;margin: auto;padding: 20px 0 40px;" alt = "illustration showing the original popup and then the proposed right panel ">
</div>
	
* <span class = "bullet-lead">Clean up map: </span>Initially, media were plotted on the map as their media type. This meant that multiple photos for a single location might be stacked on top of each other as individual instances. Since the photo thumbnails were used for the map pins, this created additional visual confusion. I proposed requiring each photo to be contained in a site in order to be plotted on the map.
<div style="text-align: center;">
	<img src="/assets/LOCALGROUND/wireframe-2.png" style="width:80%;margin: auto;padding: 20px 0 40px;" alt = "illustration showing a cluster of photos then a single pin">
</div>
	
* <span class = "bullet-lead">Use "Projects" to organize: </span>In the existing version, users switch between projects by turning on and off datasets, and the map preferences (such as map skin and center) are saved as cookies. I recommended making a separate page for each project to better facilitate work on a single project and fit common mental models.

Below is an iteration of the wireframe for choosing styles of sites, like a powerpoint presentation.
<div class = "design-feature localground">
	<img src="/assets/LOCALGROUND/wireframe.png" style="margin: 40px;width:calc(100% - 80px);">
</div>

	
## Choosing a Prototyping Tool

Once our team had aligned on the structure and we had validated it with some key users, I began to prototype the interaction details. I chose <span class = "skill">HTML/CSS/Javascript</span> because I knew that prototyping software becomes slow and difficult to use with complex systems.



## Initial User Testing

I recruited 5 users for our first round of testing. Research sessions included an <span class = "skill">interview</span> on previous exposure to map making software and Local Ground, and then a series of <span class = "skill">tasks</span>. Our main findings included the following:

* <span class = "bullet-lead">Improved workflow: </span>Overall, users who had experience with the old design found that the new design better foregrounded the tasks they needed to complete.
	
* <span class = "bullet-lead">Fix Terminology: </span>We confirmed that some of our labeling terminology was confusing. While this design improved on the previous version, where icons were unlabeled, I began to conduct additional research on mapping and GIS terminology for inspiration.




## Iterations and Visual Design

Once we had validated the overall structure of the site, I started to prototype <span class = "skill">interaction</span> details and iterate on the <span class = "skill">visual design</span>. My team went out into the city of Berkeley and photographed public artwork. Using real data helps me design for the worst case scenarios, and resulted in an interesting mini project to present at the Local Ground workshop.

I used material design guidelines to guide the visual design. This is appropriate for Local Ground's origins as a tool that overlays hand drawn maps onto digital maps. In to foreground user content and avoid pandering to younger users, I used a simple, light, and modern color palette.

## User Testing and Design Critique

I completed a second round of usability testing with 5 participants who had a range of experience with Local Ground. I also showed Local Ground to an experienced design mentor. These informed the final stage of the prototype that I am now focusing on implementing.

* <span class = "bullet-lead">Visible feedback: </span>Initially, the dialogue for creating a visualization happened in a modal window; a pattern used in other GIS software. However, users weren't sure what they were actually doing when trying to complete tasks. So I moved the modal to a panel, and subsequent users did not experience the same problems.
<div style="text-align: center;">
	<img src="/assets/LOCALGROUND/wireframe-3.png" style="width:80%;margin: auto;padding: 20px 0 40px;" alt = "illustration showing the original popup and then the proposed right panel ">
</div>
	

<p class = "desktop" style = "margin-bottom:40px;">Below are some pages from the current iteration of the prototype
<div id = "lg-map-view" class = "design-feature localground" title = "IMAGE: SITS TAB  In this view, users can edit their data, including media, in bulk. Media and sites can be presented as either a card or spreadsheet view"></div>
<div id = "lg-media-view" class = "design-feature localground" title = "Image: MEDIA VIEW In the map view, users can create sites 1 at a time. They can also style the map pins according to properties of the data. Users can create custom sites, including media, properties, descriptions, and tags, in this panel "></div>
<div id = "lg-maps-view" class = "design-feature localground" title = "Image: MAP VIEW "></div>
<div id = "lg-presentation-view" class = "design-feature" title = "Image: PUBLISHED VIEW"></div>

<!--<img class = "displayed full-width" 
src = "/assets/lg-wireframe1.png">-->
