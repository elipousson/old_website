---
layout:     post
title:      How to create a property information system for your neighborhood
date:       2016-06-06
summary:    Using open data to track housing and community development issues in Baltimore.
categories: data
---

This tutorial explains how you can use data collected by Baltimore Housing and other city agencies to help maintain an effective information system about vacant properties in your neighborhood. This is my first draft so please share your comments with me [@elipousson](https://twitter.com/elipousson) or pousson@baltimoreheritage.org.

This tutorial uses [Socrata](https://www.socrata.com/products/open-data/) (the web application that powers the [Open Baltimore](https://data.baltimorecity.gov/) website), Google Sheets, and a CartoDB (an online mapping tool). You also must have an email address to set up an account with Open Baltimore, CartoDB and Google Drive.

Google Sheets is free but you may want to apply for [Google Apps for Nonprofits](https://support.google.com/nonprofits/answer/3367223?hl=en) for your organization. CartoDB also is free to use but you may want to apply for a special [nonprofit account](https://cartodb.com/solutions/non-profits/) for your organization which makes some useful features available.

# About property information systems

In Bringing Buildings Back, urban policy scholar Alan Mallach argues that any “successful strategy for dealing with problem properties begins with a good **information system**.” An information system is a tool or set of tools that can keep track of key information about both **individual properties** and **neighborhoods**.

This isn’t just high-tech record-keeping. An information system should help elected officials, city staff, and neighborhood leaders make good decisions about what to do about vacant and distressed buildings. Of course, city officials are responsible for every property with their jurisdiction. Neighborhood organizations may want to focus on a smaller category of properties, such as vacant buildings, designated historic landmarks, or “nuisance” properties.

For example, Mallach suggests that an effective information system can work as an **early warning system**: “spotting potential problem properties and areas before it is too late to handle them effectively” and providing “timely information to individuals or organizations responsible for taking action.” At the neighborhood level, a system can be used to **evaluate market conditions** by tracking housing price trends and vacancy rates; enabling leaders to use that information to design cost-effective strategies for revitalization and adjust their strategies regularly to changing market conditions.

Neighborhood organizations can already access detailed information about their neighborhoods through the [Baltimore Neighborhood Indicators Alliance Community Profiles](http://bniajfi.org/vital_signs/cprofiles/). We have listed several other services that provide relevant information about properties across the city in the resources at the end of this tutorial. The purpose of this tutorial is to show you how to filter public datasets for information relevant for your neighborhood and how to display that data on a map.

## Getting started with Open Baltimore

![Create a new Socrata ID](/assets/images/open-baltimore-create-id.png)

1. [Set up an account](https://data.baltimorecity.gov/signup) on Open Baltimore. You may want to set up the account using your own name and email or you may want to set up an account using the name of your community organization.
2. Sign in to your account.
3. **Optional**: If you signed up for an account as an organization, you may want to fill in the basic information about your organization under account settings, including a short description and links to your website or social media profiles. Take a look at the [Baltimore Heritage account](https://data.baltimorecity.gov/profile/Baltimore-Heritage/b3vn-663r) on Open Baltimore to see an account with this information filled in.

**Note**: Baltimore City updates some of the datasets on Open Baltimore regularly. Others are years out of date. When you are browsing or searching Open Baltimore, it is easy to confuse the “filtered views” set up by users to show a subset of the data alongside the original dataset. Some datasets list “Neighborhood” as a column which makes it easy for you to filter relevant information. In other cases, you may find it more difficult to

## Finding and filtering data from Open Baltimore

![Housing and Community Development Data](/assets/images/open-baltimore-housing-development.png)

1. Find a dataset that is relevant for your neighborhood. For this project we will be working with the [Baltimore Housing Permit](https://data.baltimorecity.gov/Housing-Development/Housing-Permits/fesm-tgxf) dataset. You can find the dataset by browsing in the [Housing and Community Development category](https://data.baltimorecity.gov/browse?category=Housing%20&%20Development). The full list of categories on Open Baltimore include:
	- City Government
	- City Services
	- Culture & Arts
	- Financial
	- Geographic
	- Health
	- Housing & Development
	- Neighborhoods
	- Public Safety
	- Public Works
	- Transportation
2. Look at how the Baltimore Housing organizes the permit data. You can filter or sort the table of permit data using any of the column headers. In this tutorial, we will look at filtering permits by existing use and by neighborhood.
3. Click on the dark blue Filter button to open the Filter menu. In the right side menu, Click on the grey button labeled "Add a New Filter Condition". To select a column to filter by, click on the drop-down labeled "CaseNum".
4. To see housing permits for **vacant buildings**, select "Existing\_Use". In the next row, add the text "VAC" (short for vacant) and check the adjacent box.
5. To see housing permits in **your neighborhood**, select "Neighborhood". In the next row, add the name of your neighborhood as defined by the city.
6. The filter operation is set to "is" by default. This requires you to use the exact term used in the table. For example, "Sandtown Winchester" returns zero results. Only "Sandtown-Winchester" (using the hyphen) works as expected.
7. Click on the light blue Export button. In the right side menu, under the "Download As" heading, right-click on the link labeled CSV. Copy the link address. We can use this link to import data from Open Baltimore into Google Sheets.

_Example_: [Housing Permits Issued for Vacant Buildings since January 1, 2016](https://data.baltimorecity.gov/Housing-Development/Housing-Permits-Issued-for-Vacant-Buildings-since-/4udu-6w4h)

## Importing data from Open Baltimore to Google Sheets

**Note**:  If you do not need to keep this data up to date, you can also export the data from Open Baltimore and [import the data set](https://support.google.com/docs/answer/40608?hl=en) into Google Sheets. You can also make similar changes to the CSV data using Microsoft Excel or Numbers for Mac and then import the revised data into CartoDB.

1.  Open Google Drive and [create a new spreadsheet](https://support.google.com/docs/answer/49114?hl=en&ref_topic=20329). Make sure to give your spreadsheet a descriptive name, e.g. “Building Permits in Howard Park”.
2. In the top-left cell, insert a formula using the [IMPORTDATA function](https://support.google.com/docs/answer/3093335?hl=en). By using the link to your filtered view of the data in Open Baltimore, your Google Sheet will be kept in sync with the Open Baltimore data. If a new permit is issued, you will see the change reflected in an updated spreadsheet.
3. You may want to [freeze](https://support.google.com/docs/answer/54813?hl=en) the top row of headers and the address column. Freezing rows and columns keeps them in view as you scroll through the spreadsheet. Open the View menu and the Freeze submenu. Select the option to freeze 1 row. Select the column where addresses are listed. Open the Freeze submenu again and select the option to freeze up to the current column (D).
4. When you first import the data from Open Baltimore, the dates show up  as short numbers (known as serial dates).  Select the column labeled "Date Issued". Open the [Format menu and the Number submenu](https://support.google.com/docs/answer/56470?hl=en). Select "Date". Select the column labeled "Date Expired" and change the format to Date again.
5. Before you use the data with CartoDB, you need to separate the "Location" column into two separate columns for latitude and longitude. To do this, you need two formulas using the [SPLIT](https://support.google.com/docs/answer/3094136?hl=en) and [SUBSTITUTE](https://support.google.com/docs/answer/3094215?hl=en) functions.
  6. First, use this formula ""=SPLIT(O2,",")" to split the column into two around the comma.
  7. Second, use this formula "=SUBSTITUTE(Q2,"(","")" to remove the open parentheses from the latitude coordinate (Q2 is the Location field). Then, use the formula  "=SUBSTITUTE(Q2,")","")" to remove the close parentheses from the longitude coordinates. Make sure to label these columns latitude and longitude.
6. After moving the latitude and longitude into separate columns, you can use those same values to create a link to Google Street View. You can use a this formula "="https://maps.google.com/?layer=c&cbll="&R2&","&S2" to create the URL (R2 is latitude and S2 is longitude). [StackOverflow](http://stackoverflow.com/questions/387942/google-street-view-url) provides more detail on how this works.

_Example_: [Housing Permits for Vacant Buildings (2016)](https://docs.google.com/spreadsheets/d/10LpagmZana6lxO0aVemoDfrPjXPvTdLdTCPr9It09Jo/edit?usp=sharing)

## Syncing Google Sheets to CartoDB

**Note:** To automatically sync your Google Sheet with CartoDB, you need a [non-profit account](https://cartodb.com/solutions/non-profits/) or a paid account. You can also sync your data manually by exporting a CSV file from Google Sheets and importing the data in CartoDB. Learn more about sync tables in this CartoDB video tutorial: [Real-time map with CartoDB sync tables](https://docs.cartodb.com/tutorials/realtime_maps_sync/).

1. [Login to CartoDB](https://cartodb.com/login) or [create a new account](https://cartodb.com/signup) and then login.
2. Select the green button labeled New Map.
3. Select the Connect dataset menu then select Google Drive. Select the Connect button to connect CartoDB to your Google Drive account. Find the Google Sheet you created from the Open Baltimore data feed and import the sheet as a “sync table” in CartoDB. Read more from CartoDB about [syncing datasets](https://docs.cartodb.com/cartodb-editor/datasets/#syncing-datasets).
6. Create a map with the data.
7. Use the Map layer wizard to customize the appearance of the map markers. You can change the color of the markers or substitute icons for the circular dots. Read more from CartoDB [on the map wizard](https://docs.cartodb.com/cartodb-editor/maps/#wizards).
7. Update the info window to show the property address, link to Google Street View, and any additional relevant information from your spreadsheet. Exclude any distracting or irrelevant information such as the latitude and longitude. Read more from CartoDB [on the infowindow](https://docs.cartodb.com/cartodb-editor/maps/#infowindows).
8. Add any additional data layers that may be relevant or useful. These could include City Council Districts, state legislative Districts, or the boundaries for a local historic district.

_Example_: [Where are permits being issued for vacant buildings in 2016?](https://elipousson.cartodb.com/viz/88fd2156-1b0e-11e6-9627-0e674067d321/public_map)

## Turning property information into awareness and action

Why is organizing data about properties in your neighborhood useful? Here are a few reasons:

- **Fewer surprises**. Following a continually updated set of data on your neighborhood can supplement existing forms of public notice (such as posted signage on a building)
- **Visual and engaging**. Maps offer a visual look housing and development issues that may be more accessible and engaging for your neighbors. Data in Google Sheets can be annotated with comments or used to create charts or tables.

With a better awareness of building permits in your neighborhood, you could alert Baltimore Housing if an owner appears to be doing work outside the limits of the approved permit. Or you could help connect local homeowners to useful resources on rehabilitation projects.

With a better awareness of vacant building notices in your neighborhood, you could help Baltimore Housing keep vacant building secure by calling 311 if the boards are removed. You could also document problems with nuisance properties to build the documentation required to assign a vacant building notice.

## Other ways to track properties in your neighborhood

You can use **real estate listing websites** to track when properties are listed for sale or when they are sold.

[Zillow](http://www.zillow.com/), [Trulia](http://www.trulia.com/), [Redfin](https://www.redfin.com/) and other real estate listing websites offer you the option of receiving email alerts for new listings and recent sales in your neighborhood or zip code. These better known websites specialize in residential properties. Other real estate websites specialize in listing commercial properties [LoopNet](http://www.loopnet.com/ "http://www.loopnet.com"). Some local real estate firms specialize in a specific category of properties: [Gold and Company](http://goldcommercial.net/) for commercial properties, [Praise Buildings](http://www.praisebuildings.com/) on religious properties, and [A.J. Billing & Co. Auctioneers](http://www.ajbillig.com/) who sell properties at auction. 

You can use **[Google Alerts](https://www.google.com/alerts)** to track when a property makes the news. 

By searching for an address or a building name on Google News, you can set up an alert to receive regular emails whenever the address or property name appears in a news article or blog post. Searches for specific terms like an address may return less information than a more general for a neighborhood or street name. Buildings often make news for major changes. Examples include when a business opens or closes, a building is damaged by a fire, or a building is sold.

## Related Resources

- [Baltimore Foreclosure Data 2011-2013](http://foreclosures.bniajfi.org/)
- [Central Maryland Development Tracker](http://realestate.bniajfi.org/interactive-map.php)
- [Search Condemned Properties – Baltimore Housing](http://cels.baltimorehousing.org/Search_DEM_Map.aspx)