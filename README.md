# Kaggle-Toxic-Comment-Classification-Challenge
My best scripts from the Toxic Comment Classification Challenge on Kaggle. Below is a blog style post with many of the things I learned working on this competition.

I’ve been wanting to do a Kaggle competition for a while, but I kept putting it off because I wanted to learn more before I started. On a whim I checked the competition list and saw a straightforward one that fit well into the skills I have learned so far. The competition was the Toxic Comment Classification Challenge. The goal was simple: you have a comment on Wikipedia and it is labeled 0 or 1 for six different categories of negative comments. You must train a model that outputs the probabilities of being a 1 for each comment in the test set.

This seemed like a great entry point! However, the closing date was 7 days away by time I saw it. I managed to make time to start it 4 days before closing. Some of my lessons likely arose due to the feeling that I needed to rush, but at the same time if I was more careful and methodical in the beginning then I likely would have saved time (lesson 1!).

I set a couple goals: 1) learn a bunch, 2) don’t use anything I see in other Kernels without understanding it fully, and 3) try my best!

The two main tools that I got way more exposure to were Pandas and Scikit-learn. I know I’ve still barely touched the surface on Pandas but I feel I have a much stronger understanding of what is included within SKlearn even though I used only a tiny sliver.

All of my learning of ML methods have focused on using a single approach. This makes sense since it has been in coursework sort of settings, but I quickly learned that for these competitions you often want to use an ensemble of methods and have an appropriate way to merge them. I’m strictly against just using a blend of other people’s submissions, but I like the idea of using an ensemble. However, and this is still a mystery to me, my ensemble attempt did worse (barely) than my pure logistic regression approach. Much to learn still!

I always understood cross-validation (CV) when I heard about it in talks but never used it. When it came time to using it I realized I wasn’t sure if I was supposed to use one of the models from CV or do something else. I learned that you use CV to check your model/hyperparameters, and then go train on the entire dataset now that you’re more confident you built a good model.

Lastly, explore the outputs! I ran a .describe() on the outputs and things looked fine. But I was getting competition results way worse than my training results (~.65 vs ~.98). Why? I was accidentally outputting class labels and not probabilities. If I used .head() I would have immediately saw that. That felt like the most rookie of mistakes but also fixing that boosted my confidence because then my results were in line with everyone else around the high nineties.

Also, I somehow missed that I didn’t need to run my code on Kaggle’s servers, that’s a major oops. I could have managed my code and calculations better using my own set up. That maybe would have allowed me to get a few more tests in before butting up against the time limit (an issue I plan to not have next time…).

Kaggle specific, but submission time limit is a pain. I had a few ideas in the last day, but I’d 
In the end my best kernel placed me in the top 64% with a classification score of 0.9773. Certainly not impressive, but I’m happy given how much I learned and how little time I had to tackle this.


