# LA_job
This project was given to me as part of the interview in a job in LA

PDF file link: https://drive.google.com/file/d/0BwCbo8muBqPnZVBYVktLcE9kQlk/view?usp=sharing

Update: First, I started analyzing the data (manually in order to know what it looks like and get familiar with it, try to find patterns...etc.) and here's what I did so far: 

1) The PDF file that contains the data has over 7400 pages in which there are 44 contracts. 

2) It was hard for me to know where the contracts start and end even manually using search tool (Ctrl + F). 


3) I ended up finding a keyword that gave me 44 occurrences which was the closest that I could get so I decided that it was enough for me to start from here. 

4) I read a little about how to load and extract text from a pdf file into Jupyter then I did it, but the data was all messy and HUGE (about 7400 pages of data).

5) I had the idea to load the data into a dictionary where each key correspond to the page number and its value is the corresponding text.

6) I cleaned a little bit the data (join split on space and lower casing...etc.).

7) After that I performed a search (similar to the manual one that I did before. But instead of having 44 matches I only got 41. The reason is that 2 of the missing ones were scanned images and not a text format so they were not decoded while loading the PDF and the last one was because of the split function, it, somehow, interpreted a \n as a space so I got a space in a word which is supposed to be one word (the word was used for the search). 

8) Since there were only 3 missing values, rather than wasting time and trying to fix them I just added them manually (added the number of missing pages).

9) After a bit of pythonic magic I used that information to load each contract in a dictionary with its corresponding key (for example, the text of contract 1 is the value of key 1 so I ended up with a dictionary of 44 keys, values) .

Issues: I stopped here and I'm going to continue tomorrow but here's what I noticed so far. The contracts don't have a specific format or same pattern, for example there are 2 different table contents (meaning, different sections and subsections), and even for the contracts with the same kind of table contents, the sections aren't always the same, even the format is different, sometimes it's a table not just a text. 

To Do: I'll try to see how to deal with each contract and divide it into sections and sub sections.

PS: Once the project is finished I will share what was requested.
