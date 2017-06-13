# Springboard-5.3-2
Example and Exercise with JSON based data

JSON exercise:

Using data in file 'data/world_bank_projects.json' and the techniques demonstrated above:

1. Find the 10 countries with most projects -- I achieved this by extracting the column "countryname", and then using value_counts(). I printed the top 10 using head()

2. Find the top 10 major project themes (using column 'mjtheme_namecode') -- I used json_normalize to extract the column  "mjtheme_namecode". I then found the top 10 using a similar strategy as problem 1. 

3. In 2. above you will notice that some entries have only the code and the name is missing. Create a dataframe with the missing names filled in. -- I took the dataframe that was created in problem 2, and sorted the values by code and by name, so that rows with the same code are grouped together, and rows with a blank name are also grouped together within each code. Then, I replaced each missing entry in the name column with np.nan, so that I could use fillna() with the backfill method to fill in the missing entries that correspond to each code. I then reprinted the code from Problem 2 to verify values were filled in.
