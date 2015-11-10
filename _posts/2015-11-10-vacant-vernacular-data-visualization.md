---
layout:     post
title:      Explaining Baltimore's vacant houses with data visualizations
date:       2015-11-10
summary:    How I am using data visualization tools to understand and explain the social, economic and political context for Baltimore's problems with vacant housing.
categories: resources
published: true
---

Data visualization? I've always thought it is very interesting but a bit out of reach for my limited technical abilities. I learned a bit about SPSS and ArcGIS in graduate school but rarely use them professionally. I have made the occasional bar chart in Excel but I almost never feel the need to make a chart or graph to accompany my work.

My recent research on vacant housing, however, has pushed me to recognize the value of data-driven analysis and interpretation to explain issues related to the economy and population that are difficult to understand with narrative tools alone.

**Please note:** I'm planning to update this post throughout the week as I continue to develop materials for my November 21 workshop at the Baltimore Museum of Art. Stay tuned for updates! Suggestions or questions are both welcome. Find me [@elipousson](http://twitter.com/elipousson). 

## What questions am I trying to answer?

Although I may be a novice at data visualization, I know enough to realize that I need clear goals for what I want the visualization to accomplish (rather than letting an sense of gee-wiz wonder take over). I'm trying to answer these questions both for myself and for Baltimore area residents who likely have less familiarity with the specifics of the city's historical development:

- How has the regional distribution of Baltimore's population changed over time?
- How has the regional distribution of Baltimore's employers (particularly industrial firms) changed over time?
- How did the city's borders change through annexation during the 19th and early 20th century?
- When were Baltimore's houses built? How has the pace and character of home-building responded to broader changes in the economy and society?
- What are the broad factors (and specific triggers) that contribute to the abandonment of housing? How have those changed over time?

## What tools am I using?

- [Github](https://github.com/elipousson/vacant-vernacular) and GitHub Gists
- Google Sheets: See my working documents on [Historical Housing Data (Baltimore)](https://docs.google.com/spreadsheets/d/18tYYlfv7wU4WMOauIwLx9IfTs7juzfnr1emLOg-6fE0/edit?usp=sharing) and [Vacant Housing Workshop Data](https://docs.google.com/spreadsheets/d/1d5bZjBektbpz6Xs2pLHRK2xfzRx4QKZZS1WLKoB3_Pk/edit?usp=sharing) 
- [Chartbuilder](https://github.com/Quartz/Chartbuilder) - available as a [hosted tool](http://quartz.github.io/Chartbuilder/build/) or as a [desktop version](https://github.com/mhkeller/chartbuilder-electron)
- [RAW from Density Design](http://raw.densitydesign.org)
- [bl.ocks.org](http://bl.ocks.org/) (with or without [D3.js](http://d3js.org/))
- [Atom.io](atom.io) with packages - learn more about [Atom Packages](https://atom.io/docs/v1.1.0/using-atom-atom-packages)
  - [tablr](https://atom.io/packages/tablr)
  - [json-converter](https://atom.io/packages/json-converter)

## What am I reading?

- Bringing Buildings Back (2006), Alan Mallach
- Preservation and Rightsizing Report, Advisory Council on Historic Preservation
- U.S. Civil Rights Commission Reports

## What have I made so far?

- Manufacturing Firm Moves Within the Baltimore SMSA, 1955-1965 (Alluvial Diagram chart): presented as an SVG in this [workshop visualization round-up in progress](http://bl.ocks.org/elipousson/805c2f1150928174ac8e))
- [Abandoned Property Types/Triggers (D3.js tree diagram)](http://bl.ocks.org/elipousson/ad787f9c9beb4cc48cd7) based on Table 1.1 from Bringing Buildings Back (2006), Alan Mallach.
- **Not working yet!** [Property Demolition Decision Tree (Simple vertical d3.js tree diagram)](http://bl.ocks.org/elipousson/58c2ddbfbe695893f460) based on Figure 13.1 from Bringing Buildings Back (2006), Alan Mallach.

