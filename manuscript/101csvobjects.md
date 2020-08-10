# Importing data into R and understanding different data types

![This Telegraph story establishes the scale of the gender pay gap](images/genderpaygaptelegraph.png)

In this chapter we will deal with a simple scenario: an annual update on some numbers.

New figures on gender pay at thousands of companies has been released, and after some editorial discussion you've decided to lead on the angle of how many companies have a gap in favour of men (you can [read an exåmple of a story taking this angle here](https://www.telegraph.co.uk/business/2018/04/05/final-gender-pay-gap-figures-revealed78pc-10015-firms-have-gap/) - it's always useful to do this to help you structure your own approach).

The data is available from a government website: the [gender pay gap service](https://gender-pay-gap.service.gov.uk/). Their website allows you to search for any individual company, but you can also click on a *[Download all gender pay gap data](https://gender-pay-gap.service.gov.uk/viewing/download)* link to get the data for any financial year.

That data comes in a format called CSV. We'll use that data to explore a number of core concepts in dealing with data using coding, including:

* Functions
* Variables
* 'Object' types, such as text strings, numbers, tables and lists
* Basic analysis and calculations

## Fetching data from a CSV

CSV is probably the most simple data format that you might deal with in R. CSVs are simple text files that can be read by any text-editing software - the file consists simply of rows of text where each piece of data is separated by a comma (CSV is short for Comma Separated Values). 

Unlike Excel spreadsheets, CSVs cannot contain multiple sheets, or information about any formulae - only the resulting values are kept.

We will look at spreadsheets and other data formats soon, but the CSV is a good file format to begin with in order to explore how data is imported and analysed in R, without having to deal with some of the additional challenges that more advanced formats bring with them.

## Introducing functions

To import a CSV into R, you need to use a **function**, called `read_csv()`.


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
