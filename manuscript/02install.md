# Installing R and RStudio

Before starting this book you will need to install R - the programming language - and RStudio (software that makes it easier to write and run R scripts).

You can install R [on your PC](https://cran.r-project.org/bin/windows/base/) [or Mac](https://cran.r-project.org/bin/macosx/) from the links below:

* [Install R on a Windows PC](https://cran.r-project.org/bin/windows/base/)
* [Install R on a Mac](https://cran.r-project.org/bin/macosx/)

Installing R will also install the **R Console**, which *can* be used to work with R. Most people, however, use R within the more user-friendly [RStudio](https://www.rstudio.com/), and that's what I'll be using throughout this book:

* [Download and install RStudio from here](https://www.rstudio.com/products/rstudio/download2/).

Installation should be straightforward but if you need a guide to installation I recommend [this first video from a YouTube playlist about R](https://www.youtube.com/watch?v=WJDrYUqNrHg&index=1&list=PLvhG5FRoq78otMp0WbWuJsFOarEAchMek) by Gordon Anthony Davis. The rest of the playlist is a good introduction, too, if you like to learn by watching.

## Creating a new project

One of the advantages of RStudio is that it works with '**projects**' that can save the history of all your actions. 

This means not only can you trace back what you have done, but you can share that history with others. 

So if an editor, colleague or reader asks 'How did you do that?', you can show them.

Before you start a new project **create a folder** for it to sit in. 

This might be within a broader project folder where you're storing other material related to your story, it might be within a folder where you do all your R work. Or you might be one of those people who puts everything on their desktop and then wonders why it takes so long for their computer to boot up (*ahem.*).

Then, to create a new project in R Studio click on **File > New project...**, click **Existing Directory** on the window that appears, then browse to the folder you have created for your project and select it.

Once you've created a new project R will create a new file in that folder ending with the extension *.Rproj*. This is where all the history is stored, and something you can share with others or store as a backup.

## Notebooks and RMarkdown

Throughout this book I will be using **notebooks** to keep a record of the code that we use - and I'm going to encourage you to do the same.

Notebooks are part of what is called **literate programming**. This is where code is accompanied by a narrative that explains what you are doing (and perhaps why). 

[Donald Knuth argues](https://www-cs-faculty.stanford.edu/~knuth/lp.html) that literate programming makes code "more robust, more portable, more easily maintained, and arguably more fun to write". I would certainly agree with that: it's difficult enough to remember why *you* wrote a particular piece of code, let along understanding someone else's - writing your code in a notebook that includes information about what each chunk of code is doing will help both yourself (when you look back at code you want to return to or reuse) and others (when trying to explain to them what your code does).

Notebooks in R (and in Python) allow you to actually *run* the code, not just read it. 

Here's how to use them.

To create a notebook in R select **File > New File > R Notebook**. 

The upper left corner of your screen should now show the notebook. It will be filled with some example text, including a title, some narrative, and a code block.

These are written in a very simple language called RMarkdown - there isn't a lot to learn about this language and most of it you can see in the example text that's given to you, including:

* Code blocks start with ```{r} (the `r` specifies the language it's written in) and ends with ```
* Asterisks around a word (without spaces) make it italic. Two asterisks make it bold, and three asterisks make it bold *and* italic
* You can create headings with one or more hashes at the start of a line (the fewer hashes, the more important the heading)
* You can create links by putting the text you want to link in square brackets, followed immediately by the URL you want to link *to*, in normal brackets

There you go - that's it.

Edit the placeholder text in your notebook and select **File > Save** or press CTRL+S to save it - you'll be asked to give it a name.

The resulting file will end in `.Rmd`, which means RMarkdown.
