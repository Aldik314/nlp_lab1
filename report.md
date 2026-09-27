# Laboratory 1

Name: Aidana
Date: Kadyrbay

## 1. Decisions and prediction

I chose 3 and 7 topics for comparison. From my initial analysis, I noticed several possible groups in the headlines, such as sports, IT and clickbait. However, some headlines were ambiguous and could belong to more than one group. Therefore, I wanted to compare two different numbers of topics and see which model creates more understandable and useful groups.

After running the first models, I noticed that some common Lithuanian words, such as “ir” and “su”, appeared among the important topic words. The original preprocessing removed English stopwords, but it did not remove Lithuanian stopwords.

For my preprocessing experiment, I decided to add Lithuanian stopwords to the stopword list. I predicted that this would make the topics easier to understand because common words that do not give much information would be removed. However, a possible cost is that removing more words could remove some useful information from short headlines.

## 2. Three-run comparison

| Run | Topic count |      Preprocessing      | Fixed settings / seed |         Evidence of usefulness or problems         |
| --- | ----------- | ----------------------- | --------------------- | -------------------------------------------------- |
|  A  |      3      |         Original        |   seed 42, passes 15  |           Topics were a little bit messy           |
|  B  |      7      |         Original        |   seed 42, passes 15  |             Too many topic, still messy            |
|  C  |     3/7     |   Lithuanian stopwords  |   seed 42, passes 15  | Problems with Lithuanian words, but more orginised |

So before preprocessing change, LDA model was treating Lithuanian stop words like topic examples. When stop words were removed, topics were more orginised by categories.

, but the problem is that since LDA is not familiar with lithuanian language, it is still treating lithaunian words as a separate topic category. For example the same word in english and in lithuanian can be in two different topic groups.

## 3. Final model and failure analysis

|                       Headline ID and text                                    | Actual output    | Why it fails | Possible ambiguity |
| ----------------------------------------------------------------------------- | ---------------- | ------------ | ------------------ |
|       4 Top 7 paslaptys, kurias įmonės nenori, kad žinotumėte — Read more     | Topic: 2 | lt lang |  10%  |
| Top 7 secrets companies don't want you to know — Number 5 is shocking (London)| Topic: 1 | doesn't | 13.7% |
|    Apple unveils a new iPhone with advanced camera and AI features (Berlin)   | Topic: 2 | doesn't |  8.5% |

## 4. Recommendation

Chosen model and preprocessing, evidence for the choice, accepted trade-off, and what still requires human judgement:
I recommend using the LDA model with 3 topics and the preprocessing that removes both English and Lithuanian stopwords. Removing Lithuanian stopwords improved the topics because common words such as “ir” and “su” no longer appeared among the most important topic words. However, the model still has difficulties with mixed-language and ambiguous headlines. For example, English and Lithuanian words with the same meaning are still treated as different words. Translating all headlines into one language could be tested as a possible future improvement, but translation could also introduce errors. Therefore, the model can be useful for automatically organizing headlines, but human judgement is still needed when a topic is mixed or when a headline could belong to several topics.

## 5. Sources and AI use

I used the laboratory instructions and the provided by the internet Python code examples as the main sources for this work. I also used ChatGPT to help me understand the LDA model, simplify parts of my Python code, and improve the wording of the final report. I checked the suggested code by running it in my notebook and comparing the results with the actual outputs of my trained models.