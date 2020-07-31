# Compile: importing data into R

Although you can manually create data from scratch in R by typing it out, most of the time you are going to be pulling data into R from somewhere else. 

These sources can vary. For example stories I've worked on have involved all of the following:

* A CSV file on your computer
* The second sheet in an Excel workbook
* A data file in a format like SPSS or XML or JSON
* Any of the above fetched from a URL
* Data stored in a table on a webpage
* Data published across a series of webpages
* Data gathered from social media
* Data fetched from a live data feed
* Data fetched from an API (a way of querying datasets, such as a crimes API)
* Data compiled from pure text (e.g. word frequency)

Fetching data from each of those sources involves challenges and considerations specific to it. In the following chapters I will go through different groups of techniques and challenges in turn. 

You will need the first few chapters to get a grasp for the basics, but feel free to skip chapters after those and use the sections that are relevant to the problem facing you - then come back to other chapters later as and when you need them. 

## Storing data in variables

Like most programming languages, R allows you to import and store data in 'objects' called **variables**.

*Note: you cannot use an underscore in R, which instead tends to use a dot to separate words in variables. You should also avoid using one-letter functions as these already have special meanings in R: c, q, s, t, C, D, F, I, and T.*

The easiest way to import data is to put it in the same folder as your project. This way you don't have to describe a path to data somewhere else.

If you've created a project in R Studio, and got it open, in the *console* on the left you should see a `>` and a flashing cursor.

To import data into a variable, type something like this:

`yourvariable <- read.csv('yourdata.csv')`

The bit that says `'yourdata.csv'` should obviously be the name of your file: note that it should be placed in inverted commas. In this example I'm using a spreadsheet in CSV format. (More on other formats below.)

The bit that says `yourvariable` is just a name that you choose. It can be almost anything, but choose something meaningful.

The bit that says `read.csv` is a **function**. Functions are basically recipes: the `read.csv` function is a recipe for reading CSV files. If you wanted to read other formats you can use other functions but I'll come onto that below.

The `<-` bit is taking the result of reading that CSV and putting it into your variable. You can actually just use `=` if you're used to that from other languages, but `<-` has a certain appeal.

You can add extra parameters when you import. One important one is `stringsAsFactors=FALSE`. This prevents character columns being treated as 'factors', or numeric columns containing non-numeric values (like #N/A) being treated as 'factors' when you want them to be treated as numbers. ([more on factors here](https://blog.exploratory.io/why-factor-is-one-of-the-most-amazing-things-in-r-e967fe27d292))

Add it with a comma inside the parentheses like so:

`yourvariable <- read.csv('yourdata.csv', stringsAsFactors=FALSE)`

If you don't know where the file is you can use:

`file.choose()`

This will make a window pop up which you can then use to navigate to the file that you need. The result will be a path to that file that you can copy and paste into a command like the `read.csv()` command shown above. However, note that this path may stop working later on if you move or change the file or any of the folders involved - it's always best to keep your data files in the same directory as your R project.

For importing other files see Sharon Machlis's article [Great R packages for data import, wrangling and visualization](http://www.computerworld.com/article/2921176/business-intelligence/great-r-packages-for-data-import-wrangling-visualization.html).

Once you've got it into a variable you can do all sorts of other things with it, as we'll see...
