---
layout: post
title:  Visualising Drone Wars for the Bureau of Investigative Journalism
permalink: tbij-drone-wars-viz
date:   2015-04-25 16:27:00
---
_On 6-17 April, I've been on a work placement at the Bureau of Investigative Journalism. The legends says, the Bureau has never taken on board any other student but Investigative MA. But everything changed on one historic day in November 2014, when I, desperate, entered their office boldly and asked for a work placement (I can do data was my arguement). They were so shocked by this shamelessness that agreed._

I worked with [Jack Serie](https://twitter.com/jackserle) on Drone Wars data – an exclusive collection of information that is being gathered and updated for five years. Much has been already written based on these valuable datasets but only four major visualisations has been produced (in cooperation with other agencies). During my internship, I tried to provide a fresh digital outlook, which is generally in demands in TBIJ now, and suggested a number of visualisations.

**My visualisation of the nationalities of people killed during CIA drone attacks in Pakistan and Yemen [made it to the TBIJ website](http://www.thebureauinvestigates.com/2015/05/07/counting-cost-us-drones-local-wars-killing-local-people/).**

Here it is:

<div class="juxtapose" data-startingposition="50" data-showlabels="true" data-showcredits="true" data-animate="true" data-mode="horizontal">
<img src="https://dl.dropboxusercontent.com/u/80627489/Pakistan_8.png" data-label="Pakistan" data-credit="">
<img src="https://dl.dropboxusercontent.com/u/80627489/Yemen_8.png" data-label="Yemen" data-credit="">
</div>
<link rel="stylesheet" href="//s3.amazonaws.com/cdn.knightlab.com/libs/juxtapose/latest/css/juxtapose.css">
<style>
.juxtapose .jx-control, .juxtapose .jx-controller { background: #323232; }
.juxtapose .jx-arrow.jx-left { border-color: transparent #323232 transparent transparent; }
.juxtapose .jx-arrow.jx-right { border-color: transparent transparent transparent #323232; }
</style>
<script type="text/javascript" src="//s3.amazonaws.com/cdn.knightlab.com/libs/juxtapose/latest/js/juxtapose.js"></script>


###A story in brief

The map illustrates that the majority of the drone and air strike attacks were local population, despite the US officials’ claims that the highly accurate drone attacks are targeting only high profile al Qaeda fighters.

CIA, backed by the US, has pictured their targets as international terrorists. Multinational origin of al Qaeda military men has also been proven by the Bureau of Investigative Journalism in-depth research of the strikes in Pakistan, Yemen and Somalia.

The latest investigation by the Bureau found that at least 1,379 of the 2,213 identified or partially identified individuals killed by drone attacks in Pakistan (62 per cent) were locals. Further 137 people have been described as Pashtun which is an ethnic group of tribal population living on the Pakistani and Afghan territories.

In Yemen, potentially 81 per cent of deaths were caused to local population who were unlikely terrorists.

###My idea and methodology

1. Data is being collected by the Bureau of Investigative Journalism since 2011. Naming the Dead project identified who were some of the victims, including their countries of origin.

2. I mapped the nationalities of victims for Pakistan and Yemen in CartoDB. The darker the area on the map is, the more people targeted by the US strikes originated from that country. 

3. I used [Juxtapose.js tool](http://juxtapose.knightlab.com) developed by Knight Lab to get both maps in the same place. Since the tool can only work with static images, I had to sacrifice the interactivity and take screenshots of both maps with great accuracy. But the benefit is bigger – an easy visual comparison.

###Extras

Some victims in Pakistan (21 per cent) have been only described by a broader region of their origin – arab, central Asian, Western, etc. I combined this data with the data on particular nationalities (subjective clustering) and created a treemap in Tableau that confirms the prevalence of either Pakistani or Pashtun victims.

<script type='text/javascript' src='https://public.tableau.com/javascripts/api/viz_v1.js'></script><div class='tableauPlaceholder' style='width: 704px; height: 569px;'><noscript><a href='#'><img alt='People from local tribes – 70% of US drone attack victims in Pakistan ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Dr&#47;DroneattacksPakistan&#47;Dashboard1&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz' width='704' height='569' style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='site_root' value='' /><param name='name' value='DroneattacksPakistan&#47;Dashboard1' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Dr&#47;DroneattacksPakistan&#47;Dashboard1&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='showVizHome' value='no' /><param name='showTabs' value='y' /><param name='bootstrapWhenNotified' value='true' /></object></div>

I also suggested to highlight the story's thesis by showing the Al Qaeda fighters killed in those countieres – the official targets of the US and CIA – were indeed mostly international and not locals. I produced a Tableau packed bubbles graph to show this. It wasn't published however, because Jack has already made a story with a similar angle (about Al Qaeda fighters) recently.

<script type='text/javascript' src='https://public.tableau.com/javascripts/api/viz_v1.js'></script><div class='tableauPlaceholder' style='width: 704px; height: 619px;'><noscript><a href='#'><img alt='Dashboard 1 ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Or&#47;OriginsofAlQaedafighterskilledbyUSdroneattacksinPakistan&#47;Dashboard1&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz' width='704' height='619' style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='site_root' value='' /><param name='name' value='OriginsofAlQaedafighterskilledbyUSdroneattacksinPakistan&#47;Dashboard1' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;Or&#47;OriginsofAlQaedafighterskilledbyUSdroneattacksinPakistan&#47;Dashboard1&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='showVizHome' value='no' /><param name='showTabs' value='y' /><param name='bootstrapWhenNotified' value='true' /></object></div>

I keep in touch with the Bureau. Currently, I am working on a map-based timeline story about Drone Wars that will show how the statements of the officials on drones didn't correlate with the reality. I plan to use either StoryMap or Odyssey.js.