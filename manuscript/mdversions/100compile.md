# Section 1: Compile

![](images/dataquotebradshaw.png)

Data journalism begins in one of two ways: either you have a question that needs data, or a dataset that needs questioning. Whichever it is, the compilation of data is what defines it as an act of data journalism.

Compiling data can take various forms. At its most simple the data might be:

* Supplied directly to you by an organisation (how long until we see ‘data releases’ alongside press releases?),
* Found through using advanced search techniques to plough into the depths of government websites;
* Compiled by scraping databases hidden behind online forms or pages of results using tools like OutWit Hub and Scraperwiki;
* By converting documents into something that can be analysed, using tools like DocumentCloud;
* By pulling information from APIs;
* Or by collecting the data yourself through observation, surveys, online forms or crowdsourcing.

This compilation stage is the most important – not only because everything else rests on that, but because it is probably the stage that is returned to the most – at each of the subsequent stages – cleaning, contextualising, combining and communicating – it may be that you need to compile further information.

## Compiling data in R

Although you can manually create data from scratch in R by typing it out, most of the time you are going to be pulling data into R from somewhere else. 

These sources can vary. For example, stories I've worked on have involved files ranging from CSV files and Excel spreadsheets to more complicated formats like SPSS or XML or JSON. 

Sometimes those files have been downloaded and stored on my computer (what's called storing the data 'locally') but sometimes there is an advantage to using R to fetch them directly from somewhere online (for example if the data is going to be updated). 

And sometimes the data wasn't in a data file at all, but could only be created by using R to compile it - for example, by extracting it from multiple webpages or documents, pulling it from a live feed, or by 'querying' something called an API for information held in a database (this is the most common way of compiling social media data, for example). 

And then there are the situations where you're dealing with something that doesn't look like data at all: compiling data from pure text, for example, by measuring word frequency or 'sentiment' (positivity and negativity). 

Fetching data from each of those sources involves different challenges and considerations. In the following chapters I will go through the collections of techniques needed to tackle each challenge in turn. 

You will need the first few chapters to get a grasp for the basics, but feel free to skip chapters after those and use the sections that are relevant to the problem facing you - then come back to other chapters later as and when you need them. 
