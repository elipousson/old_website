---
layout:     post
title:      Customizing the P2PU course-in-a-box Jekyll template for the Local Preservation School
date:       2016-02-15
summary: Bells and whistles for online education.
categories: localpast
published: true
---

**Note:** This is a public draft – just thinking out loud.

I first encountered the Peer-2-Peer University Course-in-a-Box Jekyll template last May while researching open source approaches for teaching MOOCs. I was immediately inspired by the project and set out to learn how to use Jekyll and GitHub Pages so we could adapt the template for our Local Preservation School project.

By October 2015, I started development on our first course—Explore Baltimore Heritage 101—using the template. I started to wonder how I could integrate a variety of interactive elements into the course pages that could help us engage potential learners and showcase the collaborative work created by people who completed exercises through the class.

Here are the features I have working:

- [Juxtapose JS](https://github.com/NUKnightLab/juxtapose) available as an include (see [this gist for the code](https://gist.github.com/elipousson/90a078721b2634813d98))
- [Timeline JS](http://timeline.knightlab.com/) available as an include (see [this gist for the code](https://gist.github.com/elipousson/1b02f519d546e8d0dd67))
- [AnchorJS](http://bryanbraun.github.io/anchorjs/) links

Here are the features I'd like to add:

- [Mother Jones News Quiz](https://github.com/motherjones/newsquiz)
- [Annotorious](http://annotorious.github.io/)
- Mapping with CartoDB.js or GeoJSON (e.g. [Jekyll GeoJSON weaver](http://katydecorah.com/code/weaving-geojson/))
- [Search with lunr.js](http://katydecorah.com/code/lunr-and-jekyll/)
- [gifplayer](http://rubentd.com/gifplayer/)

Here are other things I'd like to change:

- I'd like to define the order of the sub-modules with the page meta or with some additional index file.
- I'd like to figure out if using collections may be better than using posts.
- Fix some problems I'm encountering with prose.io
