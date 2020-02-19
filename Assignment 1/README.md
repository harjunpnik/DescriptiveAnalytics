# Introduction to NLP: Assignment 1 

### Description of Assignment 1

This assignment relates to Theme Basic NLP of the introduction to NLP (courses Deskriptiv analytik / Machine learning for descriptive problems), and will focus on basic text processing methods on Python.

The assignment is handed in as a Jupyter notebook containing the code used to solve the problem, output presenting the results, and, most importantly, notes that present the students' conclusions and answer questions posed in the assignment. 

**Assignment steps/Questions:**

Download and extract data package from here [http://dl.turkunlp.org/intro-to-nlp.tar.gz](http://dl.turkunlp.org/intro-to-nlp.tar.gz). Gzipped file intro-to-nlp/english-tweets-sample.jsonl.gz includes 10,000 English tweets downloaded from the Twiter API. The file is compressed and in JSON Lines format ([http://jsonlines.org/](http://jsonlines.org/)), i.e. one json per line.

Note: If processing the whole fiel takes too long, it's okay to read just a subset of the data, for example only 2,000 tweets...

1. Read tweets in Python 
2. Extract the actual text fields from the tweet jsons, discard all metadata at this point. Note that sometimes the text may be truncated to fit the old character limit. In these cases, is it possible to get the full text?
3. Segment each tweet using both UDPipe machine learned model (can be found from the same data package) and a heuristic method. What can you tell about the segmentation performance on tweets when manually inspecting few examples?
4. Count a word frequency list (how many times each word appears and how many unique words there are). Which are the most commmon words appearing in the data? What kind of words these are?
5. Calculate **idf** weight for each word appearing in the data (one tweet = one document), and print top 20 words with lowest and highest idf values. Why **tf** not really matter when processing tweets?
6. Find duplicate or near duplicate tweets (in terms of text field only) in the data using any method you see fit. What kind of techniques you considered using and/or tested, and how many duplicate or near duplicate did you find?