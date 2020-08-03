# Section 2: Clean

Having data is just the beginning. Being confident in the stories hidden within it means being able to trust the quality of the data – and that means cleaning it.

Cleaning typically takes two forms: removing human error; and converting the data into a format that is consistent with other data you are using.

For example, datasets will often include some or all of the following: duplicate entries; empty entries; the use of default values to save time or where no information was held; incorrect formatting (e.g. words instead of numbers); corrupted entries or entries with HTML code; multiple names for the same thing (e.g. BBC and B.B.C. and British Broadcasting Corporation); missing data (e.g. constituency); mixed data in the same column; or data in the wrong shape (e.g. swapping columsn and rows). You can probably suggest others.

There are simple ways to clean up data in Excel or Google Sheets such as find and replace, sorting to find unusually high, low, or empty entries, and using filters so that only duplicate entries (i.e. those where a piece of data occurs more than once) are shown. My book [Finding Stories in Spreadsheets](https://leanpub.com/spreadsheetstories) has a number of chapters covering ways to use those techniques.

[Open Refine](https://openrefine.org/) adds a lot more power: [its ‘common transforms’ function will, for example, convert all entries to lowercase, uppercase or titlecase](https://onlinejournalismblog.com/2011/07/05/cleaning-data-using-google-refine-a-quick-guide/). It can remove HTML, remove spaces before and after entries (which you can’t see but which computers will see as different to the same data without a space), remove double spaces, join and split cells, and format them consistently. It will also ‘cluster’ entries and allow you to merge those which should be the same.

One of R's biggest strengths is its cleaning functionality - in fact the `tidyr` package is particularly focused on that. And that's what we'll cover in the following chapters.
