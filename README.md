#  IMDB Movies Ratings Data Analysis

### Dashboard Link: - https://app.powerbi.com/links/9oMFKQajQU?ctid=497a8a6f-e00b-4265-bf91-f1e878bb7bc8&pbi_source=linkShare

Problem Statement: 
"Analyse IMDb movie ratings data to identify trends, patterns, and factors influencing movie ratings. Explore relationships between variables such as genres, directors, release years, and budgets to understand their impact on audience reception and critical acclaim. Develop insights to help stakeholders in the film industry make informed decisions regarding investment, production, and content creation strategies for maximizing audience satisfaction and success in the competitive movie market."

### Steps Followed:
- Step 1: Load data into Power BI Desktop, dataset is a csv file.
  
- Step 2: Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.
  
- Step 3: Also, since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".
  
- Step 4: It was observed that in some column only empty and null were present. (Zero errors)
  
- Step 5: For calculating Total Gross, Avg IMDb score, Avg duration, High Budget Film & NO. of moves, Nulls values were not taken into account as only less than 3% values are empty in these columns. (i.e. Column name “Gross” “Duration” “IMDb score” “Budget”)

- Step 6: In the report view, under the view tab, theme was selected.
  
- Step 7: Since the data contains various reviews, a new visual was added using the three ellipses in the visualizations pane in report view.
  
- Step 7: Visual filters (Slicers) were added for Years named “title_year”. It was show year wise visualize data.
  
- Step 8: five card visuals were added to the canvas, one representing total gross , second representing Avg. IMDb score, third representing Avg duration, fourth representing High budget film, fifth representing No. of movies. Using visual level filter from the filters pane, basic filtering was used & null values were unselected for consideration into average calculation.
  
- Step 9: In the report view, under the insert tab, one text boxes were added to the canvas for Title name “IMDB Movies Ratings Data Analysis” was mentioned.
  
- Step 10: New measure was created to find total Gross.
  
Following DAX expression was written for the same,
Total Gross = SUM(movie_metadata[gross])

A card visual was used to represent total Gross.

- Step 11: New measure was created to find Avg of IMDb score.
Following DAX expression was written for the same,
Avg IMDb Score = AVERAGE(movie_metadata[imdb_score])

A card visual was used to represent Avg of IMDb score.

- Step 12: New measure was created to find Avg Duration.
Following DAX expression was written for the same,
Avg Duration = AVERAGE(movie_metadata[duration])

A card visual was used to represent Avg Duration.

- Step 13: New measure was created to find High Budget Film.
Following DAX expression was written for the same,
High Budget Film = MAX(movie_metadata[budget])

A card visual was used to represent High Budget Film.


- Step 13: New measure was created to find No. of movies.
Following DAX expression was written for the same,
No. Of Movies = COUNT(movie_metadata[movie_title])

A card visual was used to represent No. of movies.


### Dashboard Image :- 

![Screenshot (133)](https://github.com/Vinayrawat1/Test/assets/151543006/194803c2-d5e2-440e-b2a3-ae0e9a4d3693)


# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### [1] Total Gross = 121498745559

### [2] Avg IMDb score = 6.44

### [3] Avg Duration = 107.26

### [4] High Budget film = 12216M

### [5] No of movies = 5024

### Top 5 Popular movies by Facebook likes :

(a)	Interstellar = 349K

(b)	The Avengers = 246K

(c)	The Great Gatsby =230K

(d)	Django Unchained =199K

(e)	Batman v Superman: Dawn of Justice =197K

### Top 5 Popular Director by Facebook likes:
 
 (a)Steven Spielberg =364K
 
 (b)Martin Scorsese =340K
 
 (c)Clint Eastwood =320K
 
 (d)Woody Allen =242K
 
(e)Devid Fincher =210K

### Top 5 Favourite Actor:
(a)	Johnny Depp =1.64M

(b)	Robin Williams =1.32M

(c)	Robert De Niro =1.08M

(d)	J.K Simmons =0.74M

(e)	Jimmy Bennett =0.70M

### Max IMDb_score by Genres : 

(a)	Comedy =9.50

(b)	Crime|Drama =9.30

(c)	Drama =9.10

(d)	Action|Crime|Drama|Thriller =9.00

(e)	Action|Crime|Thriller =9.00






