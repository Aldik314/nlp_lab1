# Laboratory 1 - Initial Analysis

## 1. Data preparation

The dataset was cleaned by removing empty text entries, stripping
surrounding whitespace, and removing exact duplicate headlines.

Number of headlines before cleaning: 50000
Number of headlines after cleaning: 4845

I randomly selected 20 headlines from the cleaned dataset using
random seed 42.

## 2. Initial analysis of 20 headlines

|                                     Headline                                          | My proposed topic |
|---------------------------------------------------------------------------------------|-------------------|
| 4 Top 7 paslaptys, kurias įmonės nenori, kad žinotumėte — Read more                   | clickbait         |
| 28 Coach explains new defensive tactics after the game                                | sport             |
| Top 7 paslaptys, kurias įmonės nenori, kad žinotumėte — You won't believe it (Berlin) | clickbait         |
| 88 Open-source libraries accelerate machine learning workflows analitikų teigimu      | IT                |
| 31 Local team wins national championship in overtime                                  | sport             |
| 85 Local team wins national championship in overtime                                  | sport             |
| Top 7 secrets companies don't want you to know — Number 5 is shocking (London)        | clickbait         |
| 66 Atviro kodo bibliotekos pagreitina mašininio mokymosi procesus                     | IT                |
| 79 Didelė saugumo spraga paveikė milijonus vartotojų dėl rinkos reakcijos             | IT                |
| 10 Kaip pagreitinti kompiuterį paprastais triukais                                    | IT                |
| 54 Major security breach affects millions of users worldwide po pranešimo (Paris)     | IT                |
| 93 Star player signs a multi-year contract with club                                  | sport             |
| 91 Messi įmušė įspūdingą įvartį Lygų taurėje                                          | sport             |
| 41 She did X — what happens next will shock you (Paris)                               | clickbait         |
| 62 Coach explains new defensive tactics after the game                                | sport             |
| Apple unveils a new iPhone with advanced camera and AI features (Berlin)              | IT                |
| 24 Ji padarė X — kas nutiks toliau, pribloškia                                        | clickbait         |
| 16 Treneris aiškino naują gynybos taktiką po rungtynių                                | sport             |
| Didelė saugumo spraga paveikė milijonus vartotojų — analysts say (Vilnius)            | IT                |
| You won't believe what happened next — You won't believe it (London)                  | clickbait         |

## 3. Ambiguous headlines

1: 4 Top 7 paslaptys, kurias įmonės nenori, kad žinotumėte — Read more

Explanation:
It can be either business related topic or a clickbait.

2: 79 Didelė saugumo spraga paveikė milijonus vartotojų dėl rinkos reakcijos 

Explanation:
Can be an IT and economics related topic.

## 4. Initial topic groups

From the 20 headlines, I identified several possible topic groups:

- IT
- sport
- clickbait

Randomly selected 20 topics have three topics in common, but the dataset might have one or more topics that was not included because of a random selection.

## 5. Predicted difficulties for LDA

### Difficulty 1
Some headlines may appear to refer to a topic that they do not actually belong to.

Example headline:
4 Top 7 paslaptys, kurias įmonės nenori, kad žinotumėte — Read more.

At first I thought this headline had a topic of a business area, but later I established it was a clickbait.

### Difficulty 2
Headlines are in both english and lithuanian language.

Example headline:
88 Open-source libraries accelerate machine learning workflows analitikų teigimu.

Words with the same meaning in different languages are still different tokens to a basic word-count model.