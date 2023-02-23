# twittersentimentanalysistottorikankou
I did Twitter Sentiment analysis on the subject of Tottori's Tourism and then visually plotted the results

Sentiment analysis is a very popular method of doing market research by performing data mining of opinion, then doing natural language processing and presenting or studying the results for any particular purpose, for example: Understanding the senitment of population towards a policy, product or thoughts and opinions

For this analysis I have done the following things to do analysis on Twitter's perception on Tottori Prefecture
ツイッターのユーザの鳥取観光についてどう思っているのかをセンチメント分析の方法で行います。

This is the main things done in this analysis
1) Data mining around a 1000 tweets from Twitter regarding the keyword: 鳥取観光
2) Using Google Translate packages in python to translate all the mined tweets
3) Use Natural Language processing packages such 'Roberta' by hugging face to perform Sentiment analysis
4) Visualise the result on a graph

So let's get started!

1) Mining Tweets
For the first step, we need some libraries installed to Mine tweets

![image](https://user-images.githubusercontent.com/110551323/220212618-490d7dab-410d-4ece-9bdd-dfc8e4824a57.png)

Next we mine tweets from Twitter (I have used a method where we don't need to use an API! :D) 
I used the keyword '鳥取観光' to mine the 1000 tweets from all over Twitter in the span of One year from Feb 20, 2022 to Feb 20, 2023
![image](https://user-images.githubusercontent.com/110551323/220212746-a3d3796c-74a0-4169-96e9-7aae85239f60.png)
The file will be saved in your directory

Now that we have our data, it is time to install Google Translate on python!
![image](https://user-images.githubusercontent.com/110551323/220212830-31e73dcf-b5ad-4282-a861-5e0842095dac.png)
It will take like a minute to install. 
🥵Attention! For some reason the package does not work in VSCode and always gives some error, try using Google CoLab!

Lets try doing a sample translation to see if it works.
![image](https://user-images.githubusercontent.com/110551323/220212914-a96b3399-f9ac-4912-9004-9c2ca9db08cb.png)
It works!

Now, for verification, lets check our twitter mined dataset
![image](https://user-images.githubusercontent.com/110551323/220212962-2557a83c-6df5-41e8-89eb-b25b7919bdbc.png)

Looks good to me, however, as you can see, the tweets are in Japanese and the Natural Language processing packages cannot process Japanese yet, so we will translate all the tweets to English!
![image](https://user-images.githubusercontent.com/110551323/220213062-b4b559d3-b989-4a88-8f14-b9228c7b8dd6.png)

We have successfully translated all the tweets from Japanese to english and also created a new CSV file with all the translated data in the english column.
☀️It is important to note that, since we do not translate directly and use machine translation, it might lose some level of accuracy! 

Now lets install some libraries for Sentiment analysis, I like NLTK and TRANSFORMERS

![image](https://user-images.githubusercontent.com/110551323/220213182-54703869-277e-4963-bd84-94cdd65027a1.png)
and
pip install transformers

Now lets install some essential libraries for our analysis
![image](https://user-images.githubusercontent.com/110551323/220213253-c700073b-2814-4c03-80f6-5f145e89e1eb.png)

Now its time for the difficult part, we will try to do sentiment analysis on the whole dataset and see how it goes:
![image](https://user-images.githubusercontent.com/110551323/220213305-e193ec9d-b58f-462d-a12d-c8f74e903153.png)


The final dataset with sentiment scores will look like this
![image](https://user-images.githubusercontent.com/110551323/220213331-fb587ba6-882d-4b8c-87be-ba3b0ecc9871.png)

As you can see we have 626 results now but we had 1000 tweets. It is so because, the code omitted all the duplicates and only kept the unique ones. This will help us get a more accurate average for the analysis

Checking if the dataset is alright
![image](https://user-images.githubusercontent.com/110551323/220213452-1e1dd7b2-729c-4ac6-a289-b66af92cfcc0.png)


Now we will average all the scores and check the overall probability score
![image](https://user-images.githubusercontent.com/110551323/220213492-0ffc62f9-acce-4f32-a510-84273b3a17b0.png)

THE PEOPLE OF TWITTER ARE MOSTLY POSITIVE ABOUT TOURISM IN TOTTORI! ほっとしました〜！

Now for the final Step lets visualise our results!
![image](https://user-images.githubusercontent.com/110551323/220213573-beded903-af5a-4f5f-bc2c-ad0c62875604.png)

It looks pretty nice to me! 
Thank you for reading! Lemme know of any feedback, it is always appreciated



