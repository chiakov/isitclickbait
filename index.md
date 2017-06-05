# Clickbait or not?
## EECS 349: Machine Learning, Northwestern University

Charikleia Iakovidou <br>
e-mail: chariako [at] nu [dot] northwestern [dot] edu

The goal of this project was to investigate whether it is possible to identify a “click-bait” article using Machine Learning techniques, with only the article headline is input. According to [Oxford dictionaries](https://en.oxforddictionaries.com/definition/clickbait), a click-bait is defined as “content whose main purpose is to attract attention and encourage visitors to click on a link to a particular web page”. While click-baits promise a thrilling, sensational experience, their content is usually low-quality, misleading or inaccurate. The heavy advertising combined with click-baits and the overwhelming amount of links they often contain are also concerning. [Some](https://www.theguardian.com/media/2016/jul/12/how-technology-disrupted-the-truth) even consider click-baits to be a serious threat to the future of journalism.

It's fairly easy for humans to distinguish click-baits from legitimate news. While one must take into account various factors to classify certain content as click-bait, the headlines by themselves are often revealing since they follow specific patterns in structure and vocabulary. The click-bait headline dataset was constructed by crawling [FuzzFix](http://www.fuzzfix.com/), [CooBuzz](http://www.coobuzz.com/) and [WorthyToShare](http://www.worthytoshare.com/), while the news headlines were collected using the [Guardian Open Platform](http://open-platform.theguardian.com/) and the [NYT Developers Network](https://developer.nytimes.com/). Both datasets can be visualized using [word clouds](https://www.jasondavies.com/wordcloud/):

Click-bait headline dataset:

![](http://i.imgur.com/6UOw4hw.png)

News headline dataset:

![](http://i.imgur.com/pPZoQfO.png)

Since the vocabulary sets seem to be distinct for click-bait and news, all headlines were converted to features using a TD-IDF model. The following Machine Learning techniques were subsequently tested:

- Decision Trees
- Nearest Neighbor
- Multi-layer Perceptron
- Naive Bayes Classifier
- Logistic Regression

The 10-fold cross validation accuracy and test accuracy are shown in the table bellow:

Table

Results blabla
Figures blabla

[Download full report](https://www.youtube.com/watch?v=nSc5-RkndnQ)

