---
layout:     post
title:      How to create a property information system for your neighborhood
date:       2016-06-02
summary:    Using open data to track housing and community development issues in Baltimore.
categories: data
---

This tutorial explains how you can use data collected by Baltimore Housing and other city agencies to help maintain an effective information system about vacant properties in your neighborhood.

This tutorial uses [Socrata](https://www.socrata.com/products/open-data/) (the web application that powers the [Open Baltimore](https://data.baltimorecity.gov/) website), Google Sheets, and a CartoDB (an online mapping tool). You also must have an email address to set up an account with Open Baltimore, CartoDB and Google Drive.

Google Sheets is free but you may want to apply for [Google Apps for Nonprofits](https://support.google.com/nonprofits/answer/3367223?hl=en) for your organization. CartoDB also is free to use but you may want to apply for a special [nonprofit account](https://cartodb.com/solutions/non-profits/) for your organization which makes some useful features available.

# About property information systems

In Bringing Buildings Back, urban policy scholar Alan Mallach argues that any “successful strategy for dealing with problem properties begins with a good **information system**.” An information system is a tool or set of tools that can keep track of key information about both **individual properties** and **neighborhoods**.

This isn’t just high-tech record-keeping. An information system should help elected officials, city staff, and neighborhood leaders make good decisions about what to do about vacant and distressed buildings.

For example, Mallach suggests that an effective information system works as an **early warning system**: “spotting potential problem properties and areas before it is too late to handle them effectively” and providing “timely information to individuals or organizations responsible for taking action.” At the neighborhood level, a system can be used to **evaluate market conditions** by tracking housing price trends and vacancy rates; enabling leaders to use that information to design cost-effective strategies for revitalization and adjust their strategies regularly to changing market conditions.

Neighborhood organizations can access detailed information about their neighborhoods through the [Baltimore Neighborhood Indicators Alliance Community Profiles](http://bniajfi.org/vital_signs/cprofiles/). We have listed several other services that provide relevant information about properties across the city in the resources at the end of this tutorial. The purpose of this tutorial is to show you how to build a custom collection of data for your neighborhood.

## Getting started with Open Baltimore

![Create a new Socrata ID](/images/open-baltimore-create-id.png)

1. [Set up an account](https://data.baltimorecity.gov/signup) on Open Baltimore. You may want to set up the account using your own name and email or you may want to set up an account using the name of your community organization.
2. Sign in to your account.
3. **Optional**: If you signed up for an account as an organization, you may want to fill in the basic information about your organization under account settings, including a short description and links to your website or social media profiles. Take a look at the [Baltimore Heritage account](https://data.baltimorecity.gov/profile/Baltimore-Heritage/b3vn-663r) on Open Baltimore to see an account with this information filled in.

**Note**: Baltimore City updates some of the datasets on Open Baltimore regularly. Others are years out of date. When you are browsing or searching Open Baltimore, it is easy to confuse the “filtered views” set up by users to show a subset of the data alongside the original dataset. Some datasets list “Neighborhood” as a column which makes it easy for you to filter relevant information. In other cases, you may find it more difficult to

## Finding and filtering data from Open Baltimore

![Housing and Community Development Data](/images/open-baltimore-housing-development.png)

1. Find a dataset that is relevant for your neighborhood. For this project we will be working with the [Baltimore Housing Permit](https://data.baltimorecity.gov/Housing-Development/Housing-Permits/fesm-tgxf) dataset. You can find the dataset by browsing in the [Housing and Community Development category](https://data.baltimorecity.gov/browse?category=Housing%20%26%20Development). The full list of categories on Open Baltimore include:
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
4. To see housing permits for **vacant buildings**, select "Existing_Use". In the next row, add the text "VAC" (short for vacant) and check the adjacent box.
5. To see housing permits in **your neighborhood**, select "Neighborhood". In the next row, add the name of your neighborhood as defined by the city.
6. The filter operation is set to "is" by default. This requires you to use the exact term used in the table. For example, "Sandtown Winchester" returns zero results. Only "Sandtown-Winchester" (using the hyphen) works as expected.
7. Click on the light blue Export button. In the right side menu, under the "Download As" heading, right-click on the link labeled CSV. Copy the link address. We can use this link to import data from Open Baltimore into Google Sheets.

_Example_: [Housing Permits Issued for Vacant Buildings since January 1, 2016](https://data.baltimorecity.gov/Housing-Development/Housing-Permits-Issued-for-Vacant-Buildings-since-/4udu-6w4h)

## Importing data from Open Baltimore to Google Sheets

1.  Open Google Drive and [create a new spreadsheet](https://support.google.com/docs/answer/49114?hl=en&ref_topic=20329).
2. In the top-left cell, insert a formula using the [IMPORTDATA function](https://support.google.com/docs/answer/3093335?hl=en). By using the link to your filtered view of the data in Open Baltimore, your Google Sheet will be kept in sync with the Open Baltimore data. If a new permit is issued, you will see the change reflected in an updated spreadsheet.
3. You may want to [freeze](https://support.google.com/docs/answer/54813?hl=en) the top row of headers and the address column. Freezing rows and columns keeps them in view as you scroll through the spreadsheet. Open the View menu and the Freeze submenu. Select the option to freeze 1 row. Select the column where addresses are listed. Open the Freeze submenu again and select the option to freeze up to the current column (D).
4. When you first import the data from Open Baltimore, the dates show up  as short numbers (known as serial dates).  Select the column labeled "Date Issued". Open the [Format menu and the Number submenu](https://support.google.com/docs/answer/56470?hl=en). Select "Date". Select the column labeled "Date Expired" and change the format to Date again.
5. Before you use the data with CartoDB, you need to separate the "Location" column into two separate columns for latitude and longitude. To do this, you need two formulas using the [SPLIT](https://support.google.com/docs/answer/3094136?hl=en) and [SUBSTITUTE](https://support.google.com/docs/answer/3094215?hl=en) functions.
  - First, use this formula ""=SPLIT(O2,",")" to split the column into two around the comma.
  - Second, use this formula "=SUBSTITUTE(Q2,"(","")" to remove the open parentheses from the latitude coordinate (Q2 is the Location field). Then, use the formula  "=SUBSTITUTE(Q2,")","")" to remove the close parentheses from the longitude coordinates. Make sure to label these columns latitude and longitude.
6. After moving the latitude and longitude into separate columns, you can use those same values to create a link to Google Street View. You can use a this formula "="https://maps.google.com/?layer=c&cbll="&R2&","&S2" to create the URL (R2 is latitude and S2 is longitude). [StackOverflow](http://stackoverflow.com/questions/387942/google-street-view-url) provides more detail on how this works.

**Note:** If you do not need to keep the data from Open Baltimore in sync with the Google Spreadsheet, you can also download the CSV from Open Baltimore and [import the data set](https://support.google.com/docs/answer/40608?hl=en) into Google Sheets. You can also make similar changes to the CSV data using Microsoft Excel or Numbers for Mac and then import the revised data into CartoDB.

_Example_: [Housing Permits for Vacant Buildings (2016)](https://docs.google.com/spreadsheets/d/10LpagmZana6lxO0aVemoDfrPjXPvTdLdTCPr9It09Jo/edit?usp=sharing)

## Syncing Google Sheets to CartoDB

To learn more about sync tables, watch the CartoDB video tutorial: [Real-time map with CartoDB sync tables](https://docs.cartodb.com/tutorials/realtime_maps_sync/).

_Example_: [Where are permits being issued for vacant buildings in 2016?](https://elipousson.cartodb.com/viz/88fd2156-1b0e-11e6-9627-0e674067d321/public_map)

## Other ways to track properties in your neighborhood

- **Real estate websites**: [Zillow](http://www.zillow.com/), [Trulia](http://www.trulia.com/), [Redfin](https://www.redfin.com/) and other real estate listing websites offer you the option of receiving email alerts for new listings and recent sales in your neighborhood or zip code.

- **[Google Alerts](https://www.google.com/alerts)**: By searching for an address or a building name, you can set up an alert to receive regular emails whenever the address or property name appears in a news article or blog post. Searches for specific terms like an address may return less information than a more general for a neighborhood or street name.

## Related Resources

- [Baltimore Foreclosure Data 2011-2013](http://foreclosures.bniajfi.org/)
- [Central Maryland Development Tracker](http://realestate.bniajfi.org/interactive-map.php)
- [Search Condemned Properties – Baltimore Housing](http://cels.baltimorehousing.org/Search_DEM_Map.aspx)
