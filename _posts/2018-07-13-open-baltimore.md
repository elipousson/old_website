---
layout: post
title: "Baltimore Data Day: How are people using data on Open Baltimore?"
summary: "A presentation for Baltimore Data Day 2018."
date: 2018-07-13
modified: 2018-07-18
categories: presentation
---

I had the opportunity to participate in Baltimore Data Day again this year as part of a panel discussion on Open Baltimore, the city's seven-year-old open data portal. The narrative notes from my presentation are below and should (mostly) match up with [my Google Slides](https://docs.google.com/presentation/d/18acVed8lYoFREfHrJ7SZKwD4onk4gYYeRXgIhyjo0xI/edit?usp=sharing).

The presentation is based in part on my rough analysis of the Open Baltimore public asset inventory including a look at just the [community or custom views of data](https://docs.google.com/spreadsheets/d/1lyEHlaM-9hPfp38h8K_IMuK7kG9OD9_T9wfTuwXkAZ8/edit?usp=sharing) created by registered Open Baltimore users and the [official datasets](https://docs.google.com/spreadsheets/d/1URIuecV0SMCQN0NAkzZjH6O89qaZ4c3JL6yNh5aj7nk/edit?usp=sharing) (excluding derived views like maps or visualization). I used a [Twitter search for mentions of @OpenBaltimore](https://twitter.com/search?f=tweets&vertical=default&q=%40OpenBaltimore&src=typd) to collect examples of past reactions and complaints. And, I also [shared my initial findings on Twitter](https://twitter.com/elipousson/status/1014888840388104192) while soliciting feedback from local residents who have used Open Baltimore. I combined this recent history with a closer look at the history of GIS that I compiled into a [rough timeline](https://cdn.knightlab.com/libs/timeline3/latest/embed/index.html?source=1pflqm9xKafOmsGlSVyL4ORdr1A65v0EnTTChMid8TQM&font=Default&lang=en&initial_zoom=2&height=650) (also available in an [open Google Sheet](https://docs.google.com/spreadsheets/d/1pflqm9xKafOmsGlSVyL4ORdr1A65v0EnTTChMid8TQM/edit#gid=0)).

---

I'm here today because I'm a data nerd and Baltimore City resident who is equally enthusiastic about using, praising, and criticizing Open Baltimore. Like many others, I'm frustrated by all the ways in which Open Baltimore doesn't work. And I'll be talking about those frustrations today. But I also want to start by urging everyone to see fixing these problems as a shared responsibility. By listening to one another's experiences, I think we can make Open Baltimore better and make Baltimore better at the same time.

So let's start with a look at the recent history of people using Open Baltimore.

The first data set uploaded to Open Baltimore—a GIS shapefile of building footprints—was added on January 21, 2011. Northeast Baltimore resident Rob Walshe created the first custom view on Open Baltimore just five days later when he created a list of 311 service requests for graffiti removal in the neighborhoods of Hamilton and Gardenville.

Over seven years have passed and eight hundred people have created accounts on Open Baltimore to create their own custom views of the city's open data. This group of users include residents in Medfield, Oliver, Violetville, Homeland, and Howard Park. Some use Open Baltimore to learn about their neighborhoods. Others use the data in their work as journalists, educators, organizers, and researchers. While most people only ever create a single custom view, some create multiple views—often on behalf of a community group.

You can judge the popularity of Open Baltimore data sets by page views or downloads but I am more interested in the people who are trying to *do something* with the data beyond just looking at it. So today, we are looking at these users and the data they're using including:

- victim-based crimes
- 311 customer service requests
- vacant building notices
- arrests
- and 911 calls

Together, people have created nearly fourteen hundred custom views based on just these five data sets—totalling over seventy percent of the custom views created on Open Baltimore since 2011.

But, despite their consistent interest in using the data published on Open Baltimore, resident experiences with the service are a mix of education, empowerment, and aggravation.

One Howard Park resident, John Schladen, started using Open Baltimore in November 2012 and started working with his neighbors to document vacant buildings in their neighborhood. In a [March 2015 interview](http://darkroom.baltimoresun.com/2015/03/howard-park-exploring-baltimores-neighborhoods/#1) with the *Baltimore Sun*, John noted the importance of data on housing for residents in Howard Park: 

>“If we can begin to understand our own condition as a community, we’re going to have much more power.”

Between January 2014 and November 2015, Samantha Armacost created twenty-five custom views on Open Baltimore on behalf of the Medfield Community Assoication. But, in 2015, she grew frustrated after changes in the availability of victim-based crime data undermined her efforts make sense of public safety in her community. She no longer uses the site.

Unpredictable coverage wasn't the only concern for residents or researchers. In an [August 2014 report](https://www.urban.org/sites/default/files/publication/22921/413219-Partner-s-Perspective-NNIP-and-Open-Data-in-Baltimore.PDF) Eric Burnstein and Seema Iyer, noted the difficulty of using the “rounded address” (the unit block number and street name) to assign incidents to neighborhoods. As a result, the 2014 publication of BNIA-JFI’s annual "Vital Signs" report "excluded many crime indicators for the first time since its inception."

Journalist Danielle Sweeney started using Open Baltimore in August 2015 as part of her reporting for the Baltimore Brew on [police responses to property crime](https://baltimorebrew.com/2015/08/26/a-burglar-in-your-bedroom-a-mugger-with-a-gun/). By April 2017, when she turned to Twitter in frustration, writing: "No one ever answers my questions." Fortunately, Danielle was not disuaded and actually expanded her use of the site in 2017 and 2018.

While Open Baltimore may not be responsible for the errors and inconsistency in the data provided by city agencies, poor communication does little to correct any misconceptions. User comments on [911 call data point](https://data.baltimorecity.gov/Public-Safety/911-Police-Calls-for-Service/xviu-ezkt/data) out missing and incorrect information without any offiial reponse.

The footer of Open Baltimore encourages people to ["nominate a dataset"](https://data.baltimorecity.gov/nominate) but the published comments highlight the confusion experienced by many individuals using the site. People are looking for data sets that are [already available](https://data.baltimorecity.gov/nominate/6302) and wondering what happened to data that has [disappeared from public view](https://data.baltimorecity.gov/nominate/6609). People report issues with incorrect or [missing data](https://data.baltimorecity.gov/nominate/3458). Few comments of any kind have been published lately. No "dataset suggestions" have been marked as "approved" since February 18, 2014. Users submitted 148 suggestions over the first five years of Open Baltimore's operation. Over the last two and a half years, only twenty-one suggestions have been submitted. Given the lack of response to prior submissions, people could be forgiven for deciding that trying to request new data on Open Baltimore may not be worth the trouble.

Of course, Open Baltimore isn't the only source for data and public information from city agencies. And these other sources have their own challenges: confusing interfaces, inaccessible web design, and dated technical infrastructure. You don't need take my word for it. Please try finding data and information on a few of these sites:

- Baltimore City Health Department [Food Facility Inspection Reports database](http://baltimore.foodinspectionreports.com)
- The Department of Planning's [Community Association Directory](https://planning.baltimorecity.gov/maps-data/online-community-association-directory)
- The [database of applications, inspection reports, and other documents](https://bllcrecords.baltimorecity.gov) from the Board of Liquor License Commissioners for Baltimore City
- Baltimore Housing's [codeMap](http://cels.baltimorehousing.org/codemap/codeMap.html)

Can you find the information you need using these sites? Do you feel like the information is accurate and up to date? If not, why not? <!-- Add a mention for Councilman Brandon Scott's role in getting the health department and 911 data up online. -->

All to often, residents searching for essential public information run into frustrating and disappointing road blocks. [Open Budget Baltimore](http://openbudget.baltimorecity.gov/) created by the Bureau of the Budget and Management Research is just one revealing example of this problem. The site tells visitors that the "data that powers Open Budget" is  "available to you." But my recent attempt to follow the link data led back to Open Baltimore where I was confronted by a message tell me to go "Back to where you came from." Is this what it feels like to have your own city gas-lighting you?

I truly don't want to spend our time together on a re-visiting past complaints. Instead, I'd like to find a way to bridge the gap between the aspirations and dreams we've brought to Open Baltimore and the experiences it offers for people in Baltimore today.

For people who believe in the power of data to make the city a better place, you should remember that you are part of a long tradition.

In February 1907, Theodore Marburg, founder and president of the Municipal Art Society, gathered "City and State officials, heads of city departments, City Councilmen and leaders of the thought of a great university" for a "round table" and "smoker" in the Hotel Rennert (where the Charles Center parking lot stands today) to listen to "expositions of the advantages and benefits to be derived" from the city's new Legislative Reference Department headed by Dr. Horace E. Flack. Before a group of twenty-five White men who sat around a table sipping cups of punch and smoking "fragrant cigars" in the hotel's "cafe clubroom," Marburg proclaimed:

> "In this hour of change, the most thorough investigation into a city problem made today may be out of date tomorrow. The price of intelligent action is constant investigation. ...The money value of adequate data on things we are about to do is difficult to measure."

![Hotel Rennert, c. 1896. Published by Alfred S. Campbell. Courtesy [Library of Congress](http://www.loc.gov/pictures/item/2005680842/).](/assets/images/1s12943u-hotel-rennert-1896.jpg)

The costs of ignorance may be difficult to measure but we've lived with them for as long as Baltimore has been around. For people who are frustrated with the state of open data in Baltimore today, you are also part of a long tradition.

It shouldn't be a surprise to learn that the Citizen's Planning and Housing Association (CPHA), for example, has created one hundred and fifty custom views on Open Baltimore—more than any other single user. CPHA has a long history of advocating for city staff and elected officials to improve the ways they organize and share data about housing, transportation, and countless other issues. In one 1965 editorial that sounds all too familiar, the organization observed:

>“No one person knows how many vacant houses are owned by the city, how many should be razed, how many have a known owner, how many are needed for other uses and how many are involved in some stage of the law enforcement process.”

CPHA's advocacy led to the creation of the Department of Housing and Community Development in 1968 and, by the mid-1970s, the creation of the city's first "Vacant House File"—a collection of punch cards created for use with a mainframe computer. Today, using [codeMap](http://cels.baltimorehousing.org/codemap/codeMap.html), anyone can find answers to at least some of these questions.

What can we take away from this recent history and the much longer history that preceded it? Here are a few ideas for what the staff reponsible for Open Baltimore and everyone who plays a part in opening access to public data online could consider:

- The limits or quirks of Socrata may be one source of the problems with Open Baltimore. But don't fool yourself into thinking that it is the only part or even the most important part.
- Consistent location data is key to ensuring inter-operability and ease of reuse by residents and researchers alike.
- Open Baltimore and all of the city's online services need to put a higher priority on accessibility and education.
- Open Baltimore needs meaningful and useful opportunities for feedback that can be used by both city staff and residents.