# Part 1
## Question 1) Write a regex to extract all the numbers with orange color background from the below text in italics.


{"orders":[{"id":1},{"id":2},{"id":3},{"id":4},{"id":5},{"id":6},{"id":7},{"id":8},{"id":9},{"id":10},{"id":11},{"id":648},{"id":649},{"id":650},{"id":651},{"id":652},{"id":653}],"errors":[{"code":3,"message":"[PHP Warning #2] count(): Parameter must be an array or an object that implements Countable (153)"}]}

Ans: For this created code with regex. Which will return all the values after : (colon)



## Question 2) Here’s the list of reviews of Chrome apps - scraped from Playstore.  DataSet Link

Problem statement - There are times when a user writes Good, Nice App or any other positive text, in the review and gives 1-star rating. Your goal is to identify the reviews where the semantics of review text does not match rating. 

Your goal is to identify such ratings where review text is good, but rating is negative- so that the support team can point this to users. 

Deploy it using - Flask/Streamlit etc and share the live link. 

Important
In this data app - the user will upload a csv and you would be required to display the reviews where the content doesn’t match ratings.  This csv will be in the same format as the DataSet Link

Ans: Analyzed the dataset depending on the length of the review found the below conclusions:

1)Total reviews 7204
2)1 star review 1894
3)2 star review 336
4)3 star review 451
5)4 star review 652
6)5 star review 3871

Found that 3 star rating having average reviews, so that excluded that for analysis.
1) 4 star and 5 star is considered as good review.
2) 1 star and 2 star is considered as bad review.

For 4 and 5 star rating combinely having 4523 reviews. For 1 and 2 ratings combinely having 2230. In that found the logic that if the length of the review is 10 and more than 10 having matching the review with the ratings.

For rating length of word less than 10 having some unmatching reviews.

For 4 & 5 star rating there are around 2594 reviews which are having length less than 10.
Removed the duplicate words from that, it came out to 659.
Collected the words for 659 there are 242 words which are relavent to rating rest 417 are not.
Based on that created logic.

For 1 & 2 star rating there are around 316 reviews which are having length less than 10. 
Removed the duplicate words from that, it came out to 181 unique reviews. 
Collected the words for 181 unique reviews.There are 39 words which are relavent to rating, rest 142 are not.
Based on that created logic, kindly refer shared code in github.

## Found that there are 1083 reviews are not relavent to the rating.

## Question 3) Ranking Data - Understanding the co-relation between keyword rankings with description or any other attribute. Here’s the dataset. 
## Suggested questions:
### Is there any co-relation between short description, long description and ranking? Does the placement of keyword (for example - using a keyword in the first 10 words - have any co-relation with the ranking)?

Ans: Created the dataframe df1 of 10 records, for checking the correlation of short description, long description and ranking with respect to first 10 records.
#### For first 10 records**
1) There is strong positive correlation between Short Description and long description.

2) There is strong positive correlation between Short Description and Ranking.

3) There is weak positive correlation between long Description and Ranking.

#### Conclusion:-
If the length of the description is short the ranking will be good as per first 10 records.**
Does APP ID (Also known as package name) play any role in ranking?

#### **For whole DataFrame (df) records**
1) There is strong positive correlation between Short Description and long description.

2) There is weak positive correlation between Short Description and Ranking.

3) There is positive correlation between long Description and Ranking.

#### Conclusion:-
Long description will impact on rankings. As per the whole dataframe if the length of the description is long the ranking will be good.**

# Part 2
## Question 1) Check if the sentence is Grammatically correct: Please use any pre-trained model or use text from open datasets. Once done, please evaluate the English Grammar in the text column of the below dataset. 

Ans: Taken the first 50 samples from the DataFrame to perform the analysis.
     Used "language_tool_python" library for finding the grametical mistakes.
     Got output as below:-
     Anathi Khanyile  -- Mistakes found,  2  mistakes
     Tony bahut funny hai Hill climbing racing my favourite game  -- Mistakes found,  3  mistakes
     Teturwu  -- Mistakes found,  1  mistakes
     Hoooooooooooyaaaaaaaaa what a game hooooooooooooyaaaaaaaa  -- Mistakes found,  2  mistakes
     This game is nice  -- No mistakes
     
     Added 1 column No_of_Mistakes at last in df1 dataframe. Which shows the number of gramatical mistakes, will be easy to understand.
     Kindly refer the shared code for this.
     
## More Bonus points (You can write answers to these in ReadMe)
### Question 1) Write about any difficult problem that you solved. (According to us difficult - is something which 90% of people would have only 10% probability in getting a similarly good solution). 

Ans: 1) I am woking on component engineering projects. In one project we got the task to copy and paste all the data from different BOM(Bill Of Materials) and create the database. Projected time of work was 1 week. As I am learning data science skills, I suggested "MySQL" tool to client. I have installed the MySql in client laptop with permission and completed the work in less than day.

2) As a component engineer I have to search the alternate parts for parts which are obsolete(production stopped in factory). For finding the alternate parts we use various parts distributors websites, such as DigiKey, Mouser, Arrow..etc. In that for some parts we get bulk number of alternates 20 to 200. From this we have to select best 3 to 4 parts which are exactly matching specifications. For that we have to compare each and every part with the existing one. And have to sort out which one are best suited alternates. I am preparing ML algorithm so that we have to just collect the parts from distributor website and we will directly get the best suited parts. So that we can reduce hours of efforts. We can complete the hours of work in few minutes.

3) Our team saved 102K$ of client by implementing simple method in work.For that I got extraordinary performance rating from my authority.
