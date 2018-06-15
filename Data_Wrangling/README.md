# Data Wrangling
This was the Springboard assignment for wrangling a JSON file.
Manipulating JSON files to pull nested elements out to form concise and coherent Data Frames.

Question 1: Find the 10 countries with most projects
Each observation is a single project, we just need to group some column and count the number of projects. We can now pull out the 10 countries that have the most projects.

Question 2: Find the top 10 major project themes (using column 'mjtheme_namecode')
For the 2nd and 3rd part, we need to do dive into the JSON format a little further. We need to pull out the code and group name of a project's theme. 
Since JSON are essentially nested dictionaries, we had to play around with how to pull out the nested 'mjtheme_namecode' elements. Once we figure out how exactly to do that, we can create it's own dataframe and count that themes. We notice in our table that we have 122 missing group's names. These have codes, so we need to impute the name that corresponds to the code.

Question 3: In 2. above you will notice that some entries have only the code and the name is missing. Create a dataframe with the missing names filled in. 
It would seem that the easiest method of imputing these missing values would be to map a dictionary of the codes and names over the codes and impute the names into the columns. We first then have to get a dictionary of the values
For something with only 11 values, it may be easier to create a dictionary from scratch, yet for reproducibility's sake, I decided to create the dictionary from the data itself. If the world bank added a new category, we wouldn't have to add a new key-value pair to that dictionary. This code would perform it for us. We can then map the dictionary over the data frame. We can then count again, and we notice no missing values. 


