# Laboratory 1

Name: Aidana
Date: Kadyrbay

## 1. Decisions and prediction

I chose 3 and 7 topics for comparison. From my initial analysis, I noticed several possible groups in the headlines, such as sports, IT and clickbait. However, some headlines were ambiguous and could belong to more than one group. Therefore, I wanted to compare two different numbers of topics and see which model creates more understandable and useful groups.

After running the first models, I noticed that some common Lithuanian words, such as “ir” and “su”, appeared among the important topic words. The original preprocessing removed English stopwords, but it did not remove Lithuanian stopwords.

For my preprocessing experiment, I decided to add Lithuanian stopwords to the stopword list. I predicted that this would make the topics easier to understand because common words that do not give much information would be removed. However, a possible cost is that removing more words could remove some useful information from short headlines.

## 2. Three-run comparison

| Run | Topic count | Preprocessing | Fixed settings / seed | Evidence of usefulness or problems |
| --- | --- | --- | --- | --- |
| A | | Original | | |
| B | | Original | | |
| C | Selected A/B count | One change | | |

Concrete headline evidence of the preprocessing effect, including a cost or unexpected outcome if observed:

## 3. Final model and failure analysis

Reference topic names, top words and two representative headlines per topic in an appendix.

Compare at least three of your original 20 headlines with their model outputs.

| Headline ID and text | Actual model output | Why it fails the editor's needs | Possible remedy or inherent ambiguity |
| --- | --- | --- | --- |
| | | | |
| | | | |
| | | | |

Use at least two distinct kinds of problem across these three cases.

## 4. Recommendation

Chosen model and preprocessing, evidence for the choice, accepted trade-off, and what still requires human judgement:

## 5. Sources and AI use

Sources and reused code. AI tools and purposes, how outputs were checked, and one suggestion verified/corrected/rejected; otherwise state that no AI was used. The initial interpretation and defence must be completed without AI assistance.