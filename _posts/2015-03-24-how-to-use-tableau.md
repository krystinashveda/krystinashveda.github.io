---
layout: post
title:  How to find peace with Tableau
permalink: how-to-use-tableau
date:   2015-03-24 18:49:00
---

**Tableau has become a golden standard among data journalists who cannot code (d3.js) – for its wide range of visualisation possibilities that do not require a high technical knowledge from its user. However, I've heard many complaints from colleagues that the tool is not intuitive and heard to start with. After having been asked by [a Belarusian IT news site dev.by](http://dev.by/) to produce some visualisations for them, I spent about a month playing around with [Tableau 9.0](http://www.tableau.com/).  And so I share my conclusions and tips below.**

![My map in Tableau](https://dl.dropboxusercontent.com/u/80627489/krystinashveda.com/Screen%20Shot%202015-05-08%20at%2013.40.33.png)
_(A Tableau workbook with one of the infographics I produced for dev.by)_

##To use or not to use

Tableau is called a tool for **visual analytics** because  it has an enhanced **filtering/pivoting mechanism** in its core. So the way to conquer it is to know your data well. I tried - it’s not going to give you a sensible outcome if you just try to click on random dimensions hoping everything can correlate with everything magically, like in other data viz tools. 

>>Tableau will refuse to output even the simplest bar chart correctly if you don’t know what you are looking for. 

Actually, for a simple graph with a single value I would recommend sticking to [Datawrapper](https://datawrapper.de/) and the like - it’s a good quick-story tool with just enough interactivity to be better than Excel charts but simple enough to do magic (automated visualisations). I often use Datawrapper for initial visual analytics, aka to see the big picture.

Say, you have a dataset of all crimes committed in London in 2014 and want to find out what crime types are the most common (i.e. see how many cases of each crime type happened in 2014). So easy, hah? Datawrapper will do a bar chart automatically. But in Tableau, you first need to figure out how you build a pivot table out of the dataset, because if you simply put "crime type” into columns and number of records into rows, it will show you a useless block with a number of total crimes on top. If you also add crime type to the MARK panel - e.g. in _Colour_, it will differentiate each crime type with colour - that’s better - but within the same dull block. And only after you change the Mark type into a bar chart will it give you the bar chart you were looking for. 

##The dataset behind a Tableau viz is king

With Tableau, you first need to **have a table in mind**. You'll work out of spreadsheet anyway _(only Excel, no csv for the free Tableau Public)_. As the [intoductory Tableau tutorials](https://public.tableau.com/s/resources) say, for the best result, each row in a dataset should represent **a unique data unit** (e.g. a person, a sold item, a crime case) and each column should add **a new characteristic** across all the units. Start your table in A1 and make sure there is nothing extra like explanatory text (everything will be treated as a value). It’s important to understand that Tableau treats data horizontally, row by row. No totals.

![Data source](https://dl.dropboxusercontent.com/u/80627489/krystinashveda.com/Screen%20Shot%202015-05-08%20at%2014.07.07.png)
_A typical data source_

If you have downloaded a good dataset, it will already be organised correctly. But sometimes you'll need to **build a table from scrath for visualisation** (still in Excel), e.g. to compare values from different datasets when you received a number of FOI replies to the same question from different organisations or if you want to compare data for different years that is stored in separate tabs in Excel). It is crucial to give a descriptive name to each column - it should summarise what values are contained in it; so don’t name columns across the header row, like 1,2,3 or 2010,2011,2012 -> School places 2010, School places 2011, School places 2011. 

It's important because you will only see the names of the columns in a workbook and it's helpful if the names correspond to what they contain. Remember that if your table doesn't have a header row, Tableau will nominate each column a nominal number (F1, F2 ... F13), which becomes quite a mess.

##What the hell are those panels

Tableau divides data (imagine each column is a mini dataset) into two types:

**Dimentions** store categorical data, like yes/no/don't know or heads/tails or tables/chairs/cupboards. You can compare the number of records for different categoties and visualise it by choosing various types of _Graphs_ ("Show me") and _Marks_ (usually marks add an exta layer of data to the graph by differentiating via colour coding, shape, size, label or detail).

![Types of data viz in Tableau](https://dl.dropboxusercontent.com/u/80627489/krystinashveda.com/Screen%20Shot%202015-05-08%20at%2014.41.23.png)
_Types of data viz in Tableau_

Remember, blank cells aka “No response”/“Unknown" are also data - try to keep them in the final viz.

**Measures** are columns with numberical data. The calculations possibilities are wider. For example, you can do a beloved one scatter plot to compare two sets of data. 

<script type='text/javascript' src='https://public.tableau.com/javascripts/api/viz_v1.js'></script><div class='tableauPlaceholder' style='width: 604px; height: 719px;'><noscript><a href='#'><img alt='Dashboard 1 ' src='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;My&#47;MyTwitterfollowers&#47;Dashboard1&#47;1_rss.png' style='border: none' /></a></noscript><object class='tableauViz' width='604' height='719' style='display:none;'><param name='host_url' value='https%3A%2F%2Fpublic.tableau.com%2F' /> <param name='site_root' value='' /><param name='name' value='MyTwitterfollowers&#47;Dashboard1' /><param name='tabs' value='no' /><param name='toolbar' value='yes' /><param name='static_image' value='https:&#47;&#47;public.tableau.com&#47;static&#47;images&#47;My&#47;MyTwitterfollowers&#47;Dashboard1&#47;1.png' /> <param name='animate_transition' value='yes' /><param name='display_static_image' value='yes' /><param name='display_spinner' value='yes' /><param name='display_overlay' value='yes' /><param name='display_count' value='yes' /><param name='showVizHome' value='no' /><param name='showTabs' value='y' /><param name='bootstrapWhenNotified' value='true' /></object></div>
_An example of a simple scatter plot. Note this data viz has filter functionality. It's very easy to add them  to a Dashboard (see below)._

But **beware of false correlations** – they don't always (usually don't) mean causation. ([Check this to have some laugh](http://www.tylervigen.com/), thanks to James Ball for showing us this).

Oh, and do read this book, it's amazing: [How To Lie With Statistics](http://books.google.co.uk/books/about/How_to_Lie_with_Statistics.html?id=5oSU5PepogEC), written by Darrell Huff in 1954 – all still true! (Thanks to Paul Bradshaw for referring to it and to City Library for putting it in the books display for me to find it).

Back to Tableau, you can change the data types manually as well as copy or move columns between Dimensions and Measures.

Note that as a default Tableau will show the distribution of data (COUNT or SUM), not some sort of summarisation. This will immediately show all the limitations of your data, e.g. a small sampling, so it is harder to lie with Tableau than with Excel (totals, averages, etc.). Yet, if you work with numerical data, you can play around with calculation types.

![calculation types](https://dl.dropboxusercontent.com/u/80627489/krystinashveda.com/Screen%20Shot%202015-05-08%20at%2015.07.19.png)
_Calculation types_

##Make it pretty

Visual analytics is a powerful thing indeed. Sometimes a graph or a set of graphs suddently start to make sense only after they've been refurbished to look pretty (if serious, it is very true for colour coding - keep on playing with colours to focus the attention on what is important).

Use Filters in a worksheet to hide data that is not very relevant but distorts the main insights.

Anyway, the best thing to make your visualisation look neat is to add it to a _Dashboard_.

Dashboard is like a puzzle. As a default and for your convenience, all elemenets will be added as tiles next to each other, with no possibility to overlap (New objects: Tiled). Try adding _Blank_ spaces if you feel like the dashboard is too crammed. Add text, images, hyperlinks – it sometimes makes sense to add those smaller objects as _Floating_, i.e. they can overlap the other.

Define the needed size of a dashboard in the lower left panel called _Dashboard_ (choose _Exactly_ to be very precise; _Range_ for mobile optimised version).

![Typical dashboard](https://dl.dropboxusercontent.com/u/80627489/krystinashveda.com/Screen%20Shot%202015-05-08%20at%2015.20.40.png)
_What you can do in a Dashboard_

You can add _Quick filters_ to a dashboard to allow the user to change views by filtering by a certain category.

##Comparing data across datasets

Say, you want to compare values for a certain characteristic (column) across a number of Excel tabs. For example, school marks of the same group in each grade. Make sure data units (rows) are the same/in the same quantity (=same number of records) in all tabs. Otherwise, you will lie with statistics.

But if the units have been different each year (e.g. a random sample of people surveyed with the same question each year), you can only compare how the proportions of the asnwers changed, i.e. show all values in persentages rather than absolute numbers.

You don't always need to build a new table to compare data from different sources. Tableau has a _Story_ functionality, so you can add worksheets and even dashboards from built from different datasources on one page, with a dedicated button for each.

![Example of a story](https://dl.dropboxusercontent.com/u/80627489/krystinashveda.com/Screen%20Shot%202015-05-08%20at%2014.59.38.png)
_Example of a story_

##Conclusion

Check what other have done in Tableau. In public galleries, you can download any workbook by any author and play around - isn't it a great way to learn?

Or, when you look at a beautiful Tableau viz, try to guess what columns in a dataset are being compared/correlated/illustrated. This will help you develop data thinking - what exactly you can visualise in your data.

**[This free Whitepaper written by Tableau is very very helpful in improving your processes and styling.](https://www.tableau.com/learn/whitepapers/tableau-visual-guidebook)**