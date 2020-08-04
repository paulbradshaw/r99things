# Importing data into R and understanding different data types

![A simple numbers story by the Anadolu Agency](images/covidcasestoryanadolu.png)

Almost all data stories have two beginnings: the first is a conceptual beginning; the second is a technical one.

In a book on the technical skills of data journalism it is easy to overlook the editorial steps that come before the technical ones. So, although our book starts with technical processes, I should emphasise that before starting up RStudio, or even downloading data, it is important to complete some editorial preparation. 

In this chapter we will deal with a simple scenario: a daily or weekly update on some numbers.

In this scenario we are reacting to the latest numbers of coronavirus cases in particular countries.

But even though we are *reacting* to new data, an editorial process still exists. For example, as an organisation or a team we have decided that these numbers are newsworthy enough to report on a regular basis, and to monitor new data releases. This has involved a certain amount of **forward planning**.

As part of that we will have made an editorial judgement on the **authority and reliability** of that data, including any **caveats** we will need to include in reporting. 

Finally, we have considered our **audience** and the aspects of the data which we believe will be most relevant or interesting to them. 

[There are a number of dimensions at play here], called news values, which have been identified and explored in a range of research. These include **proximity** (people are more interested in their own country than others), **impact** or **unexpectedness** (a big spike or drop, even in a distant country, for example) and 'currency' or **topicality** (an issue or area that is already in the news is more likely to be newsworthy. For example, if the president of Brazil is in the news already then his or her country's situation may have more topicality than other countries who haven't been in the news).

So with those conceptual beginnings done with, it's time to start the technical work.

In this chapter we will cover a number of core concepts in dealing with data using coding, but rather than start with those, we will start instead by fetching the data itself, and using that to explore those concepts in turn.

## Fetching data from a CSV




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
