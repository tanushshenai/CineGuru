# CineGuru
CineGuru is a movie recommender system.  It will give a hybrid recommendation based on the description etc. of the movie entered and the predicted rating of that movie. The simple recommender allows users to specifically enter their preferred genre/ Top Movies etc. The mood-based recommender suggests movies based on the user's predicted mood.


I have developed the code with Jupyter Notebook and for the frontend, I have used the GUI library tkinter. The backend of the app incorporates a variety of techniques, including Cosine similarity, ImDB weighted rating algorithm etc.

The app has 4 features : the main recommender, the simple recommender and the mood-based recommender.

Main(Hybrid) movie recommender system : 
Input: user's tmdB ID ,a movie title
Output: It will display top 10 movies based on the description etc. of the movie entered(content-based recommendation), which means that movies with similar overview, director , actors etc. will be recommended to the user.Additionally, the movies will be recommended according to the previous ratings of other movies by the user ,the similar movies' popularity and votes (a collaborative based recommendation ). The top movies are sorted on the basis of their ImdB weighted rating.

ImdB Weighted Rating (WR) =  {[v/(v+m)]*R}+{[m/(v+m)]*C}
v is the number of votes for the movie
m is the minimum votes required to be listed in the chart(i have used 95% as minimum percentage required)
R is the average rating of the movie
C is the mean vote across the whole report

Simple movie recommender system:
Input: preferred genre/ Top Movies, number of top movies to show(n)
Output:
For top movies, a chart of top n movies (of the whole dataset) based on IMdB’s Weighted Rating system will be shown.

For genres, the top n movies of the selected genre, sorted on the basis of their ImdB weighted rating will show.

Mood-based movie recommender system:
Input: how the user's feeling (sentences or words), number of top movies to show(n)
Output: A sentiment polarity will be conducted using lexicon-based sentiment analysis.
If the score is greater than 0.2, mood is considered happy, if score is less than -0.2, mood is considered sad, else mood  is considered neutral.Then, the user will be asked to select from the genres tailored to the predicted mood(happy, sad or neutral). Then,top n movies in that genre, sorted according to their IMdB weighted rating will be displayed.
