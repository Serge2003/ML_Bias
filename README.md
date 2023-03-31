# Assignment 10 I310D: Data Bias Description
The goal of this assignment is to explore the concept of bias through querying an existing natural language processing model — specifically, the Perspective API released by Google Jigsaw. For this assignment, you will need to examine a dataset of internet comments and their scores, in addition to formulating your own queries and using the Perspective API client to score the toxicity of each comment.

## Project Goal
The goal of this project was to determine if the Perspective natural language model presented some sort of bias in relation to gender.

## Licence and data
The source of the data used in this project was obtained from the I310D canvas file page and was accessed on 3/25/2023

## Data Type and Description
The data contains the following attributes for comments proccesed by the language model:

ID: The unique id of the comment. Comment: The comment itself. Toxic: Wether the comment was deemed toxic or not.

## Hypothesis
Based on some prior knowledge and experiences with search engines and AI Language models like Chat GPT, my hypothisis is that Perspective may show some biases toward people and races that we dont typicaly think of being marginalized or it might show somw gender bias. An example would be that right now if you search on google "my bf beat me up" it links you directly to the National Domestic Violence Hotline, while if you search "my gf beat me up" it takes you to a forum site called quora as the first result.
Gender bias also exists in google's image search feature, there have been multiple articles that document that if you search up CEO you typically see men in the image search. The same thing occurs when you search for an image of a nurse, you see women in that occupation. There is alos a possibility that short messages that havent been written out with proper grammer might be looked over as non toxic.

## Testing
To test my hypothesis that comments are more likely to be flagged as toxic if the subject of the comment is a woman. I will be collecting comments from the provided sampled data set that are flagged as toxic and mention a woman as the subject of the comment. Then I will run those comments through the code to test its toxic probbability score, after that I will remove all of the nouns and pronouns and replace them with male pronouns. If the male comments constantly score lower than the female comments there might be grounds to assume that the hypothesis is correct.

## Results 
The results were inconclusive at best, the majority of tests where rude comments directed at women were marked as toxic and when the pronouns were switched to male pronouns they were marked with a lower score and sometimes not toxic. However, there were a few cases where the opposite was true, when the pronouns were switched to male pronouns the toxicity score was higher. This mainly occured when the comments were shorter. I think that there might be some gender bias that slips through sometimes and other times it doesn't. The complexity of the sentence as well as how long it is may be a factor in how the language model proccesses the comments.
The assignment did raise a few questions:

1.Does the length of a comment decrease the efficiency at which the perspective model can detect a toxic comment?

2.Might the language model proccess comments made toward women as toxic because toxicity for them is seen more often?

3.There was an outlire concerning the threshold set for this assignment, there was a comment in the csv file that was marked as not toxic but when plugged in to the code marked as a .9 probbability of being a toxic comment.
Why might have caused this?

## Known Issues or Potential Issues
There are no known issues with the code at the moment.
