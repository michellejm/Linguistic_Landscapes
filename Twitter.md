# Using Twitter in the classroom 

## Introduction
The purpose of this tutorial is to illustrate how to find tweets from a given location for use in the classroom. Twitter allows users to search for tweets in 34 languages across the world. This is invaluable for teaching and learning languages as it provides an opportunity for students to engage with authentic language and compare language usage in different areas. 

Possible assignments include:

1. Translating tweets
2. Researching the lingusitic and cultural context of a tweet
3. Comparing language use in different areas.
  1. Degree of formality
  2. Topics
  3. Use of non-textual features
4. Reflect on the role of this language in this area (is it a minority or majority language, high or low prestige?)
5. Who are these tweets written for?
  1. People physically close?
  2. Socially close?
6. And many more

## Basic Approach
*Best for exploring what is available. You will not be able to save the results of your search, but will get a sense of what data is available. You do NOT need a Twitter account for this approach.*

1. Navigate to [Twitter Advanced Search](https://twitter.com/search-advanced).
2. Under 'Words' is an option to search by language. For this tutorial, we will use "Spanish"
3. Under 'Places' is an option to search 'Near this place.' By default, Twitter will search within 15 miles of that place regardless if it is an address, city, or country. You cannot change this. You can make your area of searching larger or smaller by selecting a larger or smaller geographic unit. 
Twitter will show you all of the tweets in Tweet form, ordered using their algorithm (promoted tweets first followed by all tweets in reverse chronological order). To reorder this list chronologically, select 'Live' at the top of the page. You cannot save this output.

4. You can save this search and return to it later. To do this, select 'Save this Search"

## Intermediate Approach
*Best for saving a list of tweets using Twitter's default settings in the advanced search. This method will require the use of a Google Spreadhseet Template and involve editing some javascript. Step-by-step instructions follow.*

For this method, you will need a [Twitter account](https://twitter.com/), a [Google Account](https://www.google.com/), and either Firefox, Google Chrome, or Safari (do not use Internet Explorer). We will be using the [TAGS (Twitter Archiving for Google Spreadsheets)](https://tags.hawksey.info/) Template to save our results.

Before getting started, decide what language and what location you are interested in. Find the language code from Twitter's [list](https://dev.twitter.com/web/overview/languages). Find the latitude and longitude by finding your location on Google Maps and clicking on a point on the map. On the left side will appear an information bar with latitude and longitude information. Make a note of both of these (or keep these tabs open).

1. Navigate to the [TAGS](https://tags.hawksey.info/) Template and 'Get' it. At the time of writing, get v6.1
  1. If you are not yet logged in to your Google Account, log in now.
2. Follow the setup prompts (Make a Copy)
3. Once the sheet opens, there will be a user-friendly interface. We won't be using this very much.
4. Select 'TAGS' from the menu bar, and 'Set Up Twitter Access'
5. Follow the Setup Prompts (Authorize Google, 'Yes' to setup twitter access)
  1. Select 'Easy Setup' This will generate all the Keys and Codes you need
  2. If you are not logged in to your Twitter account, log in now
6. Return to the Spreadsheet we are working with 'Copy of TAGS v6.1'
  1. At this point, I want to rename it with the language and location I am interested in. So, I will call mine "French_ToubaSenegal". 
7. We are now going to edit some of the code that makes this spreadsheet run
  1. Select Tools > Script Editor
  2. On line 33, you should see "//var advParams = {"geocode": " and the latitude and longitude of where you are located plus a radius.
  3. Change the latitude and longitude to the location you are interested in (be sure to keep all the quotation marks in the same place).
    //var advParams = {"geocode": "14.863901, -15.877656,30mi"};
  4. Add a line below this line. This line tells TAGS what language to search for. Replace "fr" with your [Twitter language code](https://dev.twitter.com/web/overview/languages). 
    //var advParams = {"lang": "fr"}
  4. Save this file.
  5. Return to the Spreadsheet we are working with. 
8. In the search box on the spreadsheet, type a word to search for. If you are just looking for anything, choose a preposition or an article ('of', 'a', 'the' are good choices for English, for example). 
9. To run this search, select 'TAGS' > Run Now!
10. To recreate this for another language, go back to your Sheets and find the 'Copy of TAGS 6.1v' file, and repeat steps 6-9. 

You should now have two spreadsheets full of tweets that students can use to analyze language use on twitter.

