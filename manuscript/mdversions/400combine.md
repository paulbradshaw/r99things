# Section 4: Combine

Good stories can be found in a single dataset, but often you will need to combine two together. After all, given the choice between a single-source story and a multiple-source one, which would you prefer?

The classic combination is the maps mashup: taking one dataset and combining it with map data to provide an instant visualisation of how something is distributed in space: where are the cuts hitting hardest? Which schools are performing best? What are [the most talked-about topics around the world on Twitter right now?](https://www.trendsmap.com/)

This is so common (largely because the Google Maps API was one of the first journalistically useful APIs) it has almost become a cliche. But still, cliches are often – if not always – effective.

A more mundane combination is to combine two or more datasets with a common data point. That might be a politican’s name, for example, or a school, or a location.

This often means ensuring that the particular data point is formatted in the same name across each dataset.

In one, for example, the first and last names might have separate columns, but not in the other (you can concatenate or split cells to solve this).

Or you might have local authority names in one, but local authority codes in another.

One might use latitude and longitude; another postcodes, or easting and northing ([a postcodes API and Open Refine can help](https://onlinejournalismblog.com/2010/12/16/adding-geographical-information-to-a-spreadsheet-based-on-postcodes-google-refine-and-apis/)). But once you’ve got them formatted right, you may find some interesting stories or leads for further questions to ask.
