# Clickbait or not?
## EECS 349: Machine Learning, Northwestern University

Charikleia Iakovidou <br>
e-mail: chariako [at] nu [dot] northwestern [dot] edu

The goal of this project was to investigate whether it is possible to identify a “click-bait” article using Machine Learning techniques, with only the article headline is input. According to [Oxford dictionaries](https://en.oxforddictionaries.com/definition/clickbait), a click-bait is defined as “content whose main purpose is to attract attention and encourage visitors to click on a link to a particular web page”. While click-baits promise a thrilling, sensational experience, their content is usually low-quality, misleading or inaccurate. The heavy advertising combined with click-baits and the overwhelming amount of links they often contain are also matters of concern. [Some](https://www.theguardian.com/media/2016/jul/12/how-technology-disrupted-the-truth) even consider click-baits to be a serious threat to the future of journalism.

It's fairly easy for humans to distinguish click-baits from legitimate news. While one must take into account various factors to classify certain content as click-bait, the headlines by themselves are often revealing since they follow specific patterns in structure and vocabulary. To construct a dataset containing click-bait headlines, the websites [FuzzFix](http://www.fuzzfix.com/), [CooBuzz](http://www.coobuzz.com/) and [WorthyToShare](http://www.worthytoshare.com/) were crawled, while news headlines were collected using the [Guardian Open Platform](http://open-platform.theguardian.com/) and the [NYT Developers Network](https://developer.nytimes.com/). 5982 click-bait and 5620 news headlines were obtained in total. Both datasets can be visualized using [word clouds](https://www.jasondavies.com/wordcloud/):

Click-bait headline dataset:

![](http://i.imgur.com/6UOw4hw.png)

News headline dataset:

![](http://i.imgur.com/pPZoQfO.png)

Since the vocabulary sets seem to be distinct for click-baits and news, all headlines were converted to sparse vector features using a TD-IDF model. The following Machine Learning techniques were subsequently tested:

- Decision Trees (DT)
- Nearest Neighbor (NN)
- Multi-layer Perceptron (MPL)
- Naive Bayes Classifier (NBC)
- Logistic Regression (LR)
- Linear SVM (SVM)

The train/test data ratio was 80/20% in all cases. The hyperparameters were tuned using 10-fold cross validation. The 10-fold cross validation and test accuracies for all methods are shown bellow (ZR = ZeroR):

![](http://i.imgur.com/fS7LM8m.png)

MLP achieved the best accuracy on the testing set (95.22%), followed closely by SVM (95.04%) and NBC (95.00%). However, it also required significantly more training time. The DT was the worst performing classifier (89.05%). Since the number of features (12306) is much larger than the number of training examples (9282), the methods that are more robust to the "curse of dimensionality" and scale better generally achieved better performance. 

It is interesting to see how each classifier performed per output class. This is shown in the following graph:

![](http://i.imgur.com/TQDS0hV.png)

NBC is the best at identifying click-baits (97.89%), while MLP, LR and SVM achieved comparable accuracy in detecting news (~95%), with SVM performing the best. DT, NN, NBC and LR appear to be somewhat (or highly) biased, while MLP and SVM perform more or less equally well for both categories. A possible explanation lies in the characteristics of each dataset; while there are more words in the click-bait dataset in general, the news dataset contains considerably more unique words and therefore greater variation. The high variance of the news dataset might result in greater error for some techniques. A slightly greater number of click-bait examples (~300) in the training set might also cause some techniques to favor the click-bait output class.

[Download full report](https://northwestern.box.com/s/p88t74q4awrmk4mitfhzl7qst8rfh2qn)

